# Home Network Design & Implementation

## Project Overview

I designed and implemented a structured home network to gain hands-on experience with enterprise networking concepts while replacing the home's original wiring with modern Cat6A infrastructure. The project involved network planning, structured cabling, hardware installation, device configuration, DNS filtering, and documentation.

My objective was to build a reliable, scalable network while developing practical skills directly applicable to IT Support, Systems Administration, and Cybersecurity roles.

---

# Objectives

- Replace aging network infrastructure with structured Cat6A cabling
- Centralize all network connections using a patch panel
- Build a reliable, maintainable home network
- Configure separate wireless networks for different use cases
- Implement network-wide DNS filtering
- Gain practical experience with networking hardware and infrastructure
- Practice documenting an IT implementation from planning through deployment

---

# Project Scope

This project included:

- Planning structured cable routes throughout the home
- Pulling Cat6A cable through the attic
- Installing low-voltage wall boxes
- Terminating keystone jacks
- Installing and wiring a centralized patch panel
- Building and organizing a network rack
- Configuring router and switching hardware
- Deploying Raspberry Pi running Pi-hole
- Configuring static IP addressing
- Creating multiple wireless networks
- Implementing secure guest Wi-Fi access
- Providing UPS battery backup for network equipment
- Documenting the completed implementation

---

# Planning & Design

This section documents the planning process before installation.

## Planning Documentation

- Floor plan showing Ethernet drop locations
- Cable routing plan
- Device placement
- Network rack layout
- Structured cabling plan

*(Planning diagrams will be added here.)*

---

# Network Topology

This section documents the logical network architecture.

Internet

↓

ISP Gateway (Bridge Mode)

↓

Netgear Router

↓

24-Port Gigabit Switch

↓

Patch Panel

↓

Wall Drops

↓

Connected Devices

*(Detailed network diagram will be added here.)*

---

# Infrastructure Implementation

## Structured Cabling

Completed installation of structured Cat6A cabling throughout the home, including:

- Pulling cable through attic spaces
- Installing low-voltage mounting brackets
- Terminating Cat6A keystone jacks
- Punching all cable runs into a centralized patch panel
- Testing and verifying cable connectivity
- Building custom Ethernet patch cables where required

## Network Rack

Installed and organized a centralized network cabinet containing:

- Router
- Managed network switch
- Patch panel
- Raspberry Pi
- UPS battery backup

*(Photos will be added here.)*

---

# Network Configuration

Current configuration includes:

- ISP gateway operating in Bridge Mode
- Static IP assignments for infrastructure devices
- Separate 2.4 GHz and 5 GHz wireless networks
- Dedicated Guest Wi-Fi network
- QR-code guest Wi-Fi onboarding
- Raspberry Pi running Pi-hole for DNS filtering
- DHCP reservations for critical devices

---

# Security Considerations

This project follows basic operational security (OPSEC) practices.

To avoid exposing sensitive information, this repository intentionally excludes:

- Public IP addresses
- Internal IP addressing
- Wireless SSIDs
- Passwords
- MAC addresses
- Device serial numbers
- Firmware versions
- Sensitive configuration files

Security measures currently implemented include:

- WPA2/WPA3 wireless security
- Guest network isolation
- Static addressing for infrastructure devices
- Network-wide DNS filtering using Pi-hole

Future improvements include VLAN segmentation and enhanced network monitoring.

---

# Challenges & Troubleshooting

During this project I encountered several real-world challenges including:

- Planning efficient cable routes through the attic
- Selecting optimal Ethernet drop locations
- Troubleshooting failed cable terminations
- Re-punching keystone jacks
- Testing cable continuity
- Configuring router bridge mode
- Organizing and documenting cable management

These experiences provided valuable troubleshooting practice similar to issues encountered in IT support environments.

---

# Lessons Learned

This project strengthened my understanding of:

- Structured cabling standards
- Physical network infrastructure
- Ethernet termination
- Router and switch deployment
- TCP/IP networking
- DHCP and static IP management
- Wireless network design
- Technical documentation
- Systematic troubleshooting

It also reinforced the importance of planning, documentation, and testing throughout an IT implementation.

---

# Future Improvements

Planned enhancements include:

- Migration to a UniFi network ecosystem
- VLAN implementation
- Centralized network monitoring
- Syslog server
- VPN implementation
- Network Attached Storage (NAS)
- Active Directory lab integration
- Additional automation and monitoring

---

# Technologies & Skills Demonstrated

## Networking

- TCP/IP
- DHCP
- Static IP Addressing
- DNS
- Wireless Networking
- Network Topology
- Ethernet
- Structured Cabling

## Hardware

- Router Configuration
- Switch Deployment
- Patch Panel Installation
- Keystone Termination
- UPS Installation
- Raspberry Pi

## IT Support

- Network Troubleshooting
- Hardware Installation
- Cable Testing
- Documentation
- Root Cause Analysis
- Preventative Maintenance

## Security

- Pi-hole DNS Filtering
- Guest Network Isolation
- Secure Wireless Configuration
- Basic Operational Security (OPSEC)
- Infrastructure Documentation

---

# Repository Roadmap

This repository is part of my ongoing hands-on IT and Cybersecurity portfolio. Future repositories will document additional projects, including:

- Active Directory Administration
- Windows Administration
- Linux Administration
- Networking Labs
- Azure Security Labs
- Splunk SIEM
- Security Onion
- Python Projects
- Digital Forensics

Security Considerations

This repository intentionally omits sensitive configuration details such as internal IP addressing, wireless SSIDs, MAC addresses, serial numbers, and firmware versions. The focus is on documenting the technical concepts, implementation, and lessons learned while following good operational security (OPSEC) practices.
