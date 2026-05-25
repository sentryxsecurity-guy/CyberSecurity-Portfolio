# Security Policy

## Overview

This is a public personal learning portfolio. While it's open source, we maintain security best practices to protect sensitive information and ensure code quality.

## Sensitive Information

### DO NOT COMMIT

- ✅ **Credentials**: Passwords, SSH keys, access tokens, API keys
- ✅ **Personal Information**: Phone numbers, addresses, email addresses (when sensitive)
- ✅ **Configuration Files**: Local `.env` files, `secrets.json`, etc.
- ✅ **Lab Outputs**: Hashed passwords, captured network traffic with sensitive data
- ✅ **Certificates**: Private SSL/TLS certificates, security keys

### Safe to Commit

- ✅ Study notes and documentation
- ✅ Code examples and scripts (sanitized)
- ✅ Configuration templates
- ✅ Publicly available resources and references
- ✅ Lab setup instructions (without credentials)

## Security Practices

### For Scripts and Code

```python
# ❌ BAD: Hardcoded credentials
password = "MySecurePassword123!"
api_key = "sk-1234567890"

# ✅ GOOD: Use environment variables
import os
password = os.getenv('DB_PASSWORD')
api_key = os.getenv('API_KEY')
```

### Environment Configuration

1. Create `.env.example` with template variables:
   ```
   DB_PASSWORD=your_password_here
   API_KEY=your_api_key_here
   ```

2. Create local `.env` file (Git ignored):
   ```
   DB_PASSWORD=actual_password
   API_KEY=actual_key
   ```

3. Load in code:
   ```python
   from dotenv import load_dotenv
   load_dotenv()
   ```

## Lab Security

When documenting labs:

1. **Sanitize Output**: Remove/redact:
   - Real IP addresses (use 192.168.x.x, 10.0.0.x)
   - Real hostnames
   - Real credentials or hashes

2. **Use Examples**: Replace with:
   - Example data
   - Common defaults
   - Placeholder values

3. **Documentation**: Include:
   - Setup requirements
   - Tool versions used
   - Expected behavior
   - Troubleshooting tips

## Reporting Security Issues

If you discover a security vulnerability in this repository:

1. **DO NOT** open a public issue
2. **DO NOT** commit any exploit code
3. **Contact**: sentryxsecurity@gmail.com
4. Include:
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact
   - Suggested fix (if any)

## Repository Settings

### Current Configuration

- **Visibility**: Public (educational content)
- **Branch Protection**: Disabled on `main` (personal repo)
- **Merge Commits**: Allowed
- **Force Push**: Not allowed
- **Deletion**: Allowed for merged branches

### Recommended for Teams

If this becomes collaborative:
- Enable branch protection on `main`
- Require pull request reviews
- Require status checks to pass
- Dismiss stale PR approvals
- Require code owners review

## Secrets Scanning

GitHub's native secrets scanning is enabled. Additional protection:

1. **Local Check**: Run before committing
   ```bash
   git diff HEAD -- | grep -i "password\|api\|key\|secret"
   ```

2. **Pre-commit Hooks**: (Optional setup)
   ```bash
   pip install pre-commit
   pre-commit run --all-files
   ```

## Dependency Security

When adding Python packages:

1. Use virtual environments
2. Pin versions in `requirements.txt`
3. Run security checks:
   ```bash
   pip install safety
   safety check
   ```
4. Keep dependencies updated

## Educational Content Safety

### Malware/Exploit Code

- Educational examples are acceptable
- Always provide context and warnings
- Never include fully functional exploits without clear educational purpose
- Include disclaimers about legal and ethical use

### Ethical Hacking Labs

- Only use authorized environments (own systems, dedicated labs)
- Document systems tested on
- Include proper warnings
- Explain legal implications

## Access Control

- Repository is public by design (educational)
- All content is meant for learning
- No secrets stored in commits
- No sensitive personal information

## Compliance

This repository follows:
- GitHub Security Best Practices
- OWASP Guidelines
- Cybersecurity Ethical Standards

---

**Questions?** Contact: sentryxsecurity@gmail.com

*Last Updated: 2026-05-25*
