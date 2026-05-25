# Contributing Guidelines

## Code of Conduct

This repository is a personal learning portfolio. Please maintain professional and respectful standards.

## Contribution Guidelines

### Commits
- Use clear, descriptive commit messages
- Format: `[section] Description` (e.g., `[CompTIA A+] Add hardware components notes`)
- Keep commits focused on single topics
- Never commit sensitive information (credentials, API keys, etc.)

### Branch Naming
- Use lowercase with hyphens: `feature/topic-name`
- Examples: `feature/networking-notes`, `fix/typo-in-readme`

### Pull Requests
- Reference relevant issues when applicable
- Provide clear descriptions of changes
- Request review before merging to main
- Delete feature branches after merge

## Content Standards

### Documentation
- Use Markdown for all documentation
- Include clear headings and organization
- Add examples where applicable
- Link to external resources with proper attribution

### Code
- Python scripts: Follow PEP 8 style guide
- Add comments for complex logic
- Include docstrings for functions and classes
- Test code before committing

### Security
- **NEVER** commit credentials, passwords, or API keys
- Use `.env` files for sensitive configuration (ignored by .gitignore)
- Review code for hardcoded secrets before committing
- Use proper authentication methods in scripts

## Repository Organization

Each section should maintain:
```
section/
├── README.md          # Section overview and guide
├── notes/             # Study notes and documentation
├── projects/          # Hands-on projects
└── resources/         # Links and reference materials
```

## Reporting Issues

When creating issues:
- Use descriptive titles
- Include relevant labels (bug, enhancement, documentation, etc.)
- Provide context and examples when possible
- Link related issues

---

*Last Updated: 2026-05-25*
