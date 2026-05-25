# Python Programming

Python programming for cybersecurity, from beginner to intermediate level.

## Overview

This section covers Python fundamentals and cybersecurity-focused programming projects.

## Contents

- [Beginner Projects](./beginner-projects/) - Foundational programming projects
- [Notes](./notes/) - Learning materials and references
- [Scripts](./scripts/) - Utility scripts and tools

## Learning Objectives

### Python Fundamentals
- [ ] Understand variables and data types
- [ ] Work with control flow
- [ ] Create and use functions
- [ ] Handle files and exceptions
- [ ] Use standard library modules
- [ ] Understand OOP concepts

### Cybersecurity Applications
- [ ] Parse network traffic
- [ ] Automate tasks
- [ ] Analyze logs
- [ ] Create security tools
- [ ] Work with APIs
- [ ] Handle data securely

## Prerequisites

- Basic computer literacy
- No programming experience required
- Access to Python 3.8+

## Installation

### Windows
```bash
# Download from https://www.python.org/
# Run installer and enable "Add Python to PATH"
python --version
```

### macOS
```bash
brew install python3
python3 --version
```

### Linux
```bash
sudo apt-get update
sudo apt-get install python3 python3-pip
python3 --version
```

## Getting Started

### Hello World
```python
print("Hello, World!")
```

### Run a Script
```bash
python3 script_name.py
```

### Interactive Shell
```bash
python3
```

## Virtual Environment

```bash
# Create virtual environment
python3 -m venv venv

# Activate (Linux/macOS)
source venv/bin/activate

# Activate (Windows)
venv\Scripts\activate

# Install packages
pip install package_name

# Deactivate
deactivate
```

## Project Structure

```
project/
├── venv/                    # Virtual environment
├── src/                     # Source code
│   └── main.py
├── tests/                   # Unit tests
├── requirements.txt         # Dependencies
├── README.md
└── .env                     # Configuration (git ignored)
```

## Common Packages for Cybersecurity

```bash
pip install requests        # HTTP library
pip install beautifulsoup4  # HTML parsing
pip install scapy           # Packet manipulation
pip install pycryptodome    # Cryptography
pip install paramiko        # SSH client
pip install django          # Web framework
pip install sqlalchemy      # Database ORM
```

## Code Style

Following PEP 8:

```python
# Good: Clear naming and formatting
def calculate_fibonacci(n):
    """Calculate Fibonacci number at position n."""
    if n <= 1:
        return n
    return calculate_fibonacci(n - 1) + calculate_fibonacci(n - 2)

# Bad: Unclear and hard to read
def fib(n):
    if n<=1:return n
    return fib(n-1)+fib(n-2)
```

## Projects

### Beginner
1. Calculator program
2. To-do list manager
3. File organizer
4. Password generator
5. Web scraper

### Intermediate
1. Port scanner
2. Network monitor
3. Log analyzer
4. Encryption tool
5. API client

## Resources

- [Python Official Documentation](https://docs.python.org/3/)
- [PEP 8 Style Guide](https://www.python.org/dev/peps/pep-0008/)
- [Real Python](https://realpython.com/)
- Notes and projects in respective directories

## Tips for Success

- Start with fundamentals
- Practice coding daily
- Read others' code
- Debug systematically
- Use meaningful variable names
- Write documentation
- Build projects
- Share your work

---

*Last Updated: 2026-05-25*
