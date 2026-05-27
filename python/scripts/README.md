# Python Scripts
"""
Simple File Type Identifier
----------------------------

This tool identifies file types using magic byte signatures
(file headers) instead of relying only on file extensions.

Useful for:
- Cybersecurity learning
- Digital forensics basics
- File validation
- Malware analysis concepts

This was after learning the basic 
#Python writing files (.txt, .json, .csv)
#txt_data = "I like pizza"
#file_ path = "output.txt"
#with open(file_path, "w") as file:
    #file.write(txt_data)
    #print(f"text file '{file_path}' was created")
Then I began to really dive in and figure out how to identify files 
Author: Trenton H
"""
    
import os

# Dictionary mapping magic numbers (bytes) to file information
FILE_SIGNATURES = {
    b'\x89PNG\r\n\x1a\n': {'ext': 'png', 'mime': 'image/png'},
    b'\xff\xd8\xff': {'ext': 'jpg', 'mime': 'image/jpeg'},
    b'GIF87a': {'ext': 'gif', 'mime': 'image/gif'},
    b'GIF89a': {'ext': 'gif', 'mime': 'image/gif'},
    b'%PDF-': {'ext': 'pdf', 'mime': 'application/pdf'},
    b'PK\x03\x04': {'ext': 'zip', 'mime': 'application/zip'},  # Also applies to modern docx/xlsx
    b'\x50\x4b\x05\x06': {'ext': 'zip', 'mime': 'application/zip'}, # Empty archive
    b'MZ': {'ext': 'exe', 'mime': 'application/x-msdownload'},
    b'\x1f\x8b': {'ext': 'gz', 'mime': 'application/gzip'},
}

def identify_file_type(file_path):
    """Identifies file types using magic byte signatures."""
    if not os.path.exists(file_path):
        return "Error: File does not exist."
        
    # Read the maximum amount of bytes needed for our signature list
    max_read_len = max(len(sig) for sig in FILE_SIGNATURES)
    
    try:
        with open(file_path, 'rb') as f:
            file_header = f.read(max_read_len)
    except Exception as e:
        return f"Error reading file: {e}"

    # Search for matching signature
    for signature, info in FILE_SIGNATURES.items():
        if file_header.startswith(signature):
            return f"Extension: .{info['ext']} | MIME Type: {info['mime']}"
            
    # Fallback to plain text checking if no binary headers match
    try:
        with open(file_path, 'r', encoding='utf-8') as f:
            f.read(100)
            return "Extension: .txt | MIME Type: text/plain"
    except UnicodeDecodeError:
        return "Extension: Unknown | MIME Type: application/octet-stream"

# Example Usage:
# print(identify_file_type("example.jpg"))
