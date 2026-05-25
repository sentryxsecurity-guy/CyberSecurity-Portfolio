# Hands-on Labs

Practical exercises and lab environments for cybersecurity learning.

## Overview

This section contains setup guides and exercises for virtual lab environments using Kali Linux, Ubuntu, and VirtualBox.

## Contents

- [Kali Linux](./kali-linux/) - Penetration testing platform
- [Ubuntu](./ubuntu/) - General-purpose Linux system
- [VirtualBox](./virtualbox/) - Virtualization platform setup

## Lab Environment Setup

### Requirements

- **Host Machine**
  - Minimum 8GB RAM
  - 50GB free disk space
  - Multi-core processor
  - Virtualization support (VT-x/AMD-V)

- **Software**
  - VirtualBox 6.1+
  - ISO files for operating systems
  - Adequate network configuration

### Initial Setup

1. Enable virtualization in BIOS
2. Install VirtualBox
3. Create virtual machines
4. Allocate resources appropriately
5. Install operating systems
6. Configure networking
7. Take snapshots
8. Install tools

## Virtual Machines

### Kali Linux
- **Purpose**: Penetration testing and security tools
- **When to use**: Security testing, tool practice
- **Tools**: Metasploit, Burp Suite, Wireshark, etc.
- **Setup Guide**: [kali-linux/](./kali-linux/)

### Ubuntu
- **Purpose**: General Linux training and server setup
- **When to use**: Linux learning, server administration
- **Tools**: Standard development and system tools
- **Setup Guide**: [ubuntu/](./ubuntu/)

## Best Practices

### Snapshots
```bash
# Take a snapshot before major changes
# Allows rollback if something breaks
# Name snapshots descriptively
# Keep multiple restore points
```

### Networking
- Use NAT for isolated testing
- Bridge network for inter-VM communication
- Host-only for secure isolated labs
- Document network layout

### Performance
- Allocate only needed resources
- Close unused VMs
- Monitor host system resources
- Use SSD for better performance

### Security
- Use strong passwords
- Keep systems updated
- Enable firewall
- Isolate sensitive testing
- Document changes

## Exercise Categories

### Linux Fundamentals
- Command-line basics
- File system navigation
- User management
- Permissions
- Shell scripting

### System Administration
- Service management
- Package installation
- Log management
- Backup procedures
- Performance tuning

### Security Practice
- Vulnerability assessment
- Penetration testing
- Log analysis
- Threat hunting
- Incident response

### Networking
- Network configuration
- Packet capture
- Protocol analysis
- Network troubleshooting
- VPN setup

## Lab Workflow

1. **Preparation**
   - Read exercise description
   - Review prerequisites
   - Prepare environment
   - Create snapshot

2. **Execution**
   - Follow steps carefully
   - Take notes
   - Document findings
   - Troubleshoot issues

3. **Documentation**
   - Write summary
   - Include screenshots
   - Note challenges
   - Record solutions

4. **Review**
   - Compare with examples
   - Identify improvements
   - Plan next steps
   - Restore snapshot

## Exercises

Exercises organized by difficulty:
- Beginner: Basic setup and commands
- Intermediate: Advanced administration
- Advanced: Security and optimization

Each exercise includes:
- Objectives
- Prerequisites
- Step-by-step guide
- Expected results
- Troubleshooting tips
- Further learning

## Documentation

For each lab session:
- Date and time spent
- Objectives achieved
- Commands used
- Issues encountered
- Solutions applied
- Key learnings
- Next steps

## Safety and Ethics

- Use labs for learning only
- Don't attack external systems
- Follow ethical guidelines
- Respect legal boundaries
- Document testing with permission
- Clean up after yourself
- Share knowledge responsibly

## Troubleshooting

### Common Issues

**VM Won't Start**
- Enable VT-x in BIOS
- Check disk space
- Verify ISO integrity

**Network Not Working**
- Check network adapter settings
- Verify bridge/NAT configuration
- Test connectivity from host

**Performance Issues**
- Allocate more RAM
- Use SSD storage
- Close other applications
- Reduce VM count

## Resources

- [VirtualBox Documentation](https://www.virtualbox.org/manual/)
- [Kali Linux Docs](https://www.kali.org/)
- [Ubuntu Documentation](https://ubuntu.com/support/community-support)
- Setup guides in respective directories

## Tips for Success

- Start simple, build complexity
- Document everything
- Take snapshots often
- Practice regularly
- Join communities
- Share experiences
- Help others learn

---

*Last Updated: 2026-05-25*
