# Repository Structure Guide

## Overview

This document provides a detailed guide to the repository organization, naming conventions, and structure standards.

## Directory Structure

```
CyberSecurity-Portfolio/
├── .github/                          # GitHub configuration
│   ├── ISSUE_TEMPLATE/              # Issue templates
│   │   ├── bug_report.md
│   │   └── feature_request.md
│   └── PULL_REQUEST_TEMPLATE.md     # PR template
│
├── comptia-a-plus/                  # CompTIA A+ Certification
│   ├── README.md                    # Section overview
│   ├── hardware/
│   │   ├── README.md
│   │   ├── notes/
│   │   ├── diagrams/
│   │   └── resources.md
│   ├── networking/
│   ├── troubleshooting/
│   ├── ports/
│   └── practice-quizzes/
│
├── linux/                           # Linux Training
│   ├── README.md
│   ├── command-line/
│   │   ├── README.md
│   │   ├── basic-commands.md
│   │   ├── advanced-commands.md
│   │   └── cheat-sheet.md
│   ├── bash/
│   │   ├── README.md
│   │   ├── scripts/
│   │   └── tutorials/
│   └── lab-notes/
│
├── python/                          # Python Programming
│   ├── README.md
│   ├── beginner-projects/
│   │   ├── project-1/
│   │   └── project-2/
│   ├── notes/
│   └── scripts/
│
├── networking/                      # Network Fundamentals
│   ├── README.md
│   ├── tcp-ip/
│   ├── subnetting/
│   └── wireshark/
│
├── labs/                            # Hands-on Labs
│   ├── README.md
│   ├── kali-linux/
│   │   ├── setup.md
│   │   ├── exercises/
│   │   └── notes/
│   ├── ubuntu/
│   └── virtualbox/
│       └── setup-guide.md
│
├── daily-checkins/                  # Daily Progress
│   ├── README.md
│   └── 2026/
│       └── may/
│           └── 2026-05-25.md
│
├── .gitignore                       # Git ignore rules
├── LICENSE                          # MIT License
├── README.md                        # Main repository README
├── CONTRIBUTING.md                  # Contribution guidelines
├── SECURITY.md                      # Security policy
└── REPO_STRUCTURE.md               # This file
```

## Naming Conventions

### Files

**Documentation Files**
- Use lowercase with hyphens: `file-name.md`
- Examples: `advanced-commands.md`, `setup-guide.md`

**Python Scripts**
- Use lowercase with underscores: `script_name.py`
- Examples: `port_scanner.py`, `network_monitor.py`

**Bash Scripts**
- Use lowercase with hyphens or underscores: `script-name.sh`
- Examples: `system-backup.sh`, `log_analyzer.sh`

**Directories**
- Use lowercase with hyphens: `directory-name/`
- Examples: `beginner-projects/`, `tcp-ip/`
- Use plural forms: `scripts/`, `notes/`, `exercises/`

### Sections

**Main Sections** (Top-level directories)
1. `comptia-a-plus/` - Certification prep
2. `linux/` - Linux training
3. `python/` - Python programming
4. `networking/` - Network fundamentals
5. `labs/` - Hands-on exercises
6. `daily-checkins/` - Progress tracking

**Subsections** (Topic-specific)
- Follow same naming: lowercase, hyphens
- Be descriptive but concise

## Content Standards

### README Files

Each directory should have a `README.md` with:

```markdown
# Section Title

Brief description of the section content.

## Overview

What will you learn here?

## Contents

- [Topic 1](./topic-1.md)
- [Topic 2](./topic-2.md)
- [Project: Description](./projects/project-name/)

## Learning Objectives

- Objective 1
- Objective 2
- Objective 3

## Resources

- [External Resource 1](https://example.com)
- [External Resource 2](https://example.com)

## Projects

### Project Name
Brief description and link

## Notes

Any additional information
```

### Study Notes

Organize notes by topic:

```markdown
# Topic Name

## Key Concepts

### Concept 1
Definition and explanation

### Concept 2
Definition and explanation

## Examples

```code
example code
```

## Common Mistakes

- Mistake 1
- Mistake 2

## Practice Questions

1. Question 1?
2. Question 2?

## Resources

- [Link](https://example.com)
```

### Code Files

Include headers and documentation:

```python
#!/usr/bin/env python3
"""
Script Name

Brief description of what the script does.

Author: sentryxsecurity-guy
Date: 2026-05-25
Version: 1.0

Usage:
    python script_name.py [arguments]

Requirements:
    - Python 3.8+
    - Package names (if any)
"""

import os
import sys

def main():
    """Main function."""
    pass

if __name__ == "__main__":
    main()
```

## Daily Check-ins

Organize by date:

```
daily-checkins/
└── 2026/
    ├── january/
    │   ├── 2026-01-01.md
    │   └── 2026-01-02.md
    ├── may/
    │   ├── 2026-05-24.md
    │   └── 2026-05-25.md
    └── ...
```

**Check-in Format**:

```markdown
# Daily Check-in: May 25, 2026

## Today's Focus
- Topic 1
- Topic 2

## Completed
- [ ] Task 1
- [ ] Task 2
- [ ] Task 3

## Learning Summary

Brief summary of what was learned.

## Time Spent
- CompTIA A+: 1.5 hours
- Linux: 1 hour
- Python: 0.5 hours

## Tomorrow's Goals
- Goal 1
- Goal 2

## Notes
Any additional observations or insights.
```

## Git Workflow

### Commits

**Format**: `[SECTION] Description`

**Examples**:
```
[CompTIA A+] Add motherboard components guide
[Linux] Create bash script examples collection
[Python] Implement port scanner project
[Labs] Document Ubuntu VM setup process
[Daily] Check-in for May 25, 2026
```

### Branches

**Main Branch**: `main`
- Always production-ready
- No direct commits (use PRs)
- Protected from force-push

**Feature Branches**: `feature/description`
- Example: `feature/network-fundamentals`
- Created from `main`
- Merged back to `main` via PR

### Pull Requests

**Checklist**:
- [ ] Descriptive title and description
- [ ] Proper section labeled
- [ ] No sensitive information
- [ ] Content is accurate
- [ ] Markdown formatted correctly
- [ ] Links verified
- [ ] Related issues linked

## Organization Best Practices

### DO

✅ Use consistent naming conventions
✅ Create README.md for each major section
✅ Keep related content together
✅ Link related topics
✅ Include proper attribution for resources
✅ Use descriptive file and folder names
✅ Organize chronologically where appropriate
✅ Include metadata (date, author, version)

### DON'T

❌ Mix different naming styles
❌ Create deeply nested directories (max 3-4 levels)
❌ Use special characters in file names
❌ Leave empty directories (use .gitkeep if needed)
❌ Commit large files (>50MB)
❌ Create duplicate content in multiple locations
❌ Use confusing abbreviations

## Size Guidelines

### File Size
- Markdown files: < 10 KB typical
- Keep individual files focused
- Split large files into topics

### Directory Depth
- Maximum 4 levels deep
- Shallow hierarchy preferred
- Make navigation intuitive

## Search and Navigation

### Searchability
- Use descriptive headings
- Include keywords in filenames
- Link between related content
- Maintain index files

### Cross-referencing
- Link related topics
- Use consistent anchor formatting
- Keep links up-to-date

## Maintenance

### Regular Tasks
- Review and update outdated content
- Fix broken links
- Add missing resources
- Update daily check-ins
- Review and merge PRs

### Quarterly Review
- Reorganize if needed
- Update documentation
- Archive completed sections
- Add new topics

---

**Questions?** Check CONTRIBUTING.md or open an issue.

*Last Updated: 2026-05-25*
