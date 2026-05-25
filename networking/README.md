# Networking Fundamentals

Core networking concepts essential for cybersecurity professionals.

## Overview

This section covers TCP/IP fundamentals, network design, and packet analysis.

## Contents

- [TCP/IP](./tcp-ip/) - Protocol suite and networking layers
- [Subnetting](./subnetting/) - IP addressing and network segmentation
- [Wireshark](./wireshark/) - Packet analysis and network troubleshooting

## Learning Objectives

### TCP/IP Fundamentals
- [ ] Understand OSI and TCP/IP models
- [ ] Know protocol functions
- [ ] Recognize packet structure
- [ ] Understand addressing
- [ ] Work with different protocols

### Subnetting
- [ ] Calculate subnets
- [ ] Assign IP addresses
- [ ] Plan networks
- [ ] Understand CIDR notation
- [ ] Design networks efficiently

### Packet Analysis
- [ ] Capture network traffic
- [ ] Analyze protocols
- [ ] Identify issues
- [ ] Understand flow
- [ ] Debug problems

## Network Models

### OSI Model (7 Layers)
1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

### TCP/IP Model (4 Layers)
1. Link Layer
2. Internet Layer
3. Transport Layer
4. Application Layer

## Common Protocols

### Layer 3 (Network)
- IP (IPv4, IPv6)
- ICMP
- IGMP

### Layer 4 (Transport)
- TCP
- UDP
- SCTP

### Layer 7 (Application)
- HTTP/HTTPS
- DNS
- SMTP
- SSH
- FTP
- Telnet

## IP Addressing

### IPv4
- 32-bit address
- Dotted decimal notation (192.168.1.1)
- Three classes: A, B, C

### IPv6
- 128-bit address
- Colon hexadecimal notation
- Larger address space

## Key Topics

### Network Basics
- [ ] Network types and topologies
- [ ] Devices and their functions
- [ ] Cabling and media
- [ ] Speed and bandwidth

### Routing
- [ ] Static routing
- [ ] Dynamic routing
- [ ] Routing protocols
- [ ] Route selection

### Security
- [ ] Firewalls
- [ ] VPNs
- [ ] Encryption
- [ ] Access control

## Hands-on Practice

### Packet Capture
```bash
# Capture packets with tcpdump
sudo tcpdump -i eth0 -w capture.pcap

# Analyze with Wireshark
wireshark capture.pcap
```

### Subnetting Practice
- Divide networks into subnets
- Calculate host addresses
- Plan addressing schemes
- Optimize subnet allocation

### Network Simulation
- Use network simulators
- Create test networks
- Simulate issues
- Practice troubleshooting

## Resources

- [RFC 791](https://tools.ietf.org/html/rfc791) - IPv4
- [RFC 1918](https://tools.ietf.org/html/rfc1918) - Private IP
- [Wireshark Documentation](https://www.wireshark.org/docs/)
- Section-specific resources

## Tips for Mastery

- Understand concepts deeply
- Practice calculations
- Analyze real traffic
- Set up lab networks
- Read RFCs
- Troubleshoot problems
- Study packet flows

---

*Last Updated: 2026-05-25*
