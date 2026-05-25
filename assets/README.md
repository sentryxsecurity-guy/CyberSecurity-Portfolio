# Assets Directory

Central location for all media, images, and visual resources used throughout the portfolio.

## Structure

```
assets/
├── screenshots/          # Application and system screenshots
├── diagrams/            # Network diagrams, architecture, flowcharts
├── images/              # General images and visual resources
└── README.md            # This file
```

## Usage Guidelines

### Screenshots
- **Location**: `assets/screenshots/`
- **Naming**: `[section]-[topic]-[description].png`
- **Examples**:
  - `comptia-a-plus-motherboard-components.png`
  - `linux-terminal-file-permissions.png`
  - `wireshark-tcp-handshake-capture.png`

### Diagrams
- **Location**: `assets/diagrams/`
- **Naming**: `[section]-[type]-[description].png`
- **Examples**:
  - `networking-osi-model-layers.png`
  - `linux-file-system-hierarchy.png`
  - `python-data-types-flowchart.png`

### Images
- **Location**: `assets/images/`
- **Naming**: `[purpose]-[description].png`
- **Examples**:
  - `icon-security.png`
  - `banner-comptia-a-plus.png`
  - `badge-completed.png`

## File Format Standards

### Screenshots
- **Format**: PNG (preferred) or JPG
- **Resolution**: 1920x1080 or higher
- **Quality**: Full quality (no compression artifacts)
- **Size Limit**: 5MB per file

### Diagrams
- **Format**: PNG (for images) or SVG (for scalable graphics)
- **Tools**: Draw.io, Lucidchart, OmniGraffle, or similar
- **Style**: Consistent color scheme and formatting
- **Size Limit**: 10MB per file

### General Images
- **Format**: PNG or JPG
- **Resolution**: Appropriate for web (72-150 DPI)
- **Size Limit**: 2MB per file

## Linking in Documentation

### Markdown Image Syntax
```markdown
![Alt text description](../assets/screenshots/image-name.png)
![Network Diagram](../assets/diagrams/network-architecture.png)
```

### Example Usage
```markdown
## System Architecture

![System Architecture Diagram](../assets/diagrams/system-architecture.png)

This diagram shows the main components...
```

## Privacy & Security

### DO NOT INCLUDE
- Real IP addresses (use examples: 192.168.x.x)
- Real hostnames or domain names
- Credentials or sensitive data
- Personal information
- Real API keys or tokens
- Unencrypted passwords
- Confidential content

### SANITIZATION STEPS
1. Remove or redact sensitive information
2. Replace with placeholder values
3. Add annotations to highlight redacted areas
4. Include note: "Sanitized for security"

## Organization by Section

### CompTIA A+
```
assets/
├── screenshots/
│   ├── comptia-a-plus-bios-settings.png
│   ├── comptia-a-plus-device-manager.png
│   └── comptia-a-plus-motherboard-diagram.png
└── diagrams/
    ├── comptia-a-plus-hardware-hierarchy.png
    └── comptia-a-plus-boot-process.png
```

### Linux
```
assets/
├── screenshots/
│   ├── linux-terminal-file-listing.png
│   └── linux-permission-breakdown.png
└── diagrams/
    ├── linux-file-system-tree.png
    └── linux-permission-structure.png
```

### Python
```
assets/
├── screenshots/
│   ├── python-ide-project.png
│   └── python-code-execution.png
└── diagrams/
    └── python-execution-flow.png
```

### Networking
```
assets/
├── screenshots/
│   ├── networking-wireshark-capture.png
│   └── networking-ping-output.png
└── diagrams/
    ├── networking-osi-model.png
    ├── networking-tcp-ip-model.png
    ├── networking-subnet-mask.png
    └── networking-tcp-handshake.png
```

### Labs
```
assets/
├── screenshots/
│   ├── labs-vm-setup.png
│   ├── labs-kali-desktop.png
│   └── labs-network-diagram.png
└── diagrams/
    ├── labs-network-topology.png
    └── labs-vm-architecture.png
```

## Tool Recommendations

### Screenshot Tools
- **Windows**: Snagit, ShareX, Windows Screenshot
- **macOS**: Screenshot (built-in), Skitch
- **Linux**: Flameshot, GNOME Screenshot

### Diagram Tools
- **Online**: Draw.io, Lucidchart, Miro
- **Desktop**: OmniGraffle, Visio, Graphviz
- **Open Source**: Dia, Inkscape, yEd

### Image Editing
- **Simple**: Paint, Preview (macOS)
- **Intermediate**: GIMP, Photopea
- **Advanced**: Photoshop, Affinity Photo

## Image Optimization

### Before Committing
```bash
# Install ImageMagick
sudo apt-get install imagemagick  # Linux
brew install imagemagick          # macOS

# Optimize PNG
convert input.png -quality 85 -strip output.png

# Reduce JPEG quality
convert input.jpg -quality 75 -strip output.jpg

# Resize if too large
convert input.png -resize 1920x1080 output.png
```

## Version Control

### Git LFS (Large File Storage)
For large image files (>5MB):

```bash
# Install Git LFS
git lfs install

# Track large files
git lfs track "assets/**/*.png"
git lfs track "assets/**/*.jpg"

# Commit as normal
git add .gitattributes
git add assets/
git commit -m "[Assets] Add large media files"
```

## Commit Standards

### Image Commits
```bash
# Single image
git commit -m "[Assets] Add CompTIA A+ motherboard diagram"

# Multiple related images
git commit -m "[Assets] Add networking OSI model screenshots and diagrams"

# Update/replace image
git commit -m "[Assets] Update Linux file system diagram with clarifications"
```

## Organizing New Assets

### Step-by-step Process
1. Create/capture the asset
2. Sanitize (remove sensitive info)
3. Optimize for web
4. Name following conventions
5. Place in appropriate subdirectory
6. Link in relevant markdown files
7. Commit with descriptive message

## Backup and Archival

### Current Assets
- Stored in version control
- Accessible via GitHub
- Backed up with each commit

### Source Files
- Consider storing originals locally
- Keep editable versions (XCF, PSD, etc.)
- Backup important sources separately

## Tips for Quality Assets

✅ **Good Practices**
- Keep consistent visual style
- Use clear, readable fonts
- Maintain consistent color schemes
- Add descriptive captions
- Include context in surrounding text
- Test links work correctly
- Compress before committing

❌ **Avoid**
- Low resolution/blurry images
- Inconsistent styling
- Missing alt text
- Broken links
- Oversized files
- Watermarks (unless intentional)
- Sensitive information

## Accessibility

### Alt Text
Always include descriptive alt text:

```markdown
![Diagram showing OSI model with 7 layers: Physical, Data Link, Network, Transport, Session, Presentation, and Application](../assets/diagrams/osi-model.png)
```

### Captions
For complex images, add captions:

```markdown
![Network Architecture](../assets/diagrams/network-architecture.png)
*Figure 1: Complete network architecture showing all main components and their connections*
```

## Troubleshooting

### Image Not Displaying
- Check relative path is correct
- Verify file name matches exactly (case-sensitive)
- Ensure file exists in assets directory
- Check image format is supported

### File Size Issues
- Compress with ImageMagick
- Use PNG for diagrams
- Use JPG for photographs
- Consider SVG for scalable graphics

## Future Enhancements

- [ ] Add video tutorials
- [ ] Create interactive diagrams
- [ ] Build image gallery
- [ ] Add animation examples
- [ ] Create printable study guides

---

**Last Updated**: 2026-05-25
