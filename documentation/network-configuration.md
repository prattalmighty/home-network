# Network Configuration

## Overview

This document describes the configuration of the network after the physical infrastructure and equipment were installed.

The configuration was designed to provide reliable wired and wireless connectivity while separating the ISP-provided gateway from the primary home network, providing dedicated wireless networks for different use cases, and establishing a foundation for future network security and home-lab expansion.

The configuration was performed using the ISP-provided gateway and a personal wireless router as the primary routing device.

---

## ISP Gateway Configuration

The ISP-provided gateway was retained as the connection point to the ISP but was configured for bridge mode.

### Configuration

- ISP gateway placed into bridge mode.
- Primary routing and local network functions moved to the personal router.
- ISP gateway no longer functions as the primary LAN router.
- Personal router receives the WAN connection from the ISP gateway.
- Network administration and local device configuration are performed through the personal router.

### Design Rationale

The goal of using bridge mode was to avoid having two devices performing routing and NAT functions on the same network.

This provides a cleaner network architecture:

Internet
↓
ISP Gateway
↓
Primary Router
↓
Switching Infrastructure
↓
Wired / Wireless Clients

This also provides a clear separation between the ISP equipment and the equipment under my control.

---

## Primary Router Configuration

The personal router serves as the primary routing and wireless networking device.

Configuration responsibilities include:

- WAN connectivity
- DHCP
- Local IP addressing
- DNS configuration
- Wireless network configuration
- Guest network configuration
- Basic network security
- Device connectivity management

The router provides the primary Layer 3 boundary between the Internet and the home LAN.

---

## IP Addressing

The network uses private IPv4 addressing for devices on the local network.

The router provides DHCP services for clients that do not require manually assigned addresses.

Devices that benefit from predictable addressing can be assigned static IP addresses or DHCP reservations.

### Static IP Considerations

Static or predictable addresses are useful for infrastructure and devices that need to be consistently reachable.

Examples include:

- Network infrastructure
- Home-lab systems
- Servers
- Network services
- Other devices requiring predictable addressing

Sensitive addressing information is intentionally omitted from this public documentation.

---

## DNS Configuration

The network DNS configuration was changed from the ISP-provided DNS service to Google's public DNS service.

### DNS Servers

- Google Public DNS: `8.8.8.8`
- Google Public DNS: `8.8.4.4`

### Rationale

Using a known public DNS provider provides an alternative to relying on the ISP's default DNS infrastructure and gives the network a predictable external DNS service.

DNS configuration is also an area that can be changed independently from the physical network infrastructure.

---

## Wireless Configuration

Wireless connectivity was configured to support different device requirements and trust levels.

Multiple SSIDs were created rather than placing every wireless device onto a single wireless network.

### Wireless Networks

#### Primary Wireless Network

Used for trusted household devices.

Typical devices include:

- Personal computers
- Mobile devices
- Gaming devices
- Trusted smart-home devices

#### 2.4 GHz Wireless Network

A dedicated 2.4 GHz network was maintained for devices that require or perform better using the 2.4 GHz band.

This is particularly useful for older devices and some IoT equipment.

#### Guest Wireless Network

A separate guest network was configured for visitors and other devices that should not have direct access to the primary network.

Guest network isolation helps reduce the risk of an untrusted device communicating directly with trusted devices on the primary LAN.

---

## Guest Network Access

A QR code was created to simplify guest wireless onboarding.

The goal was to make connecting to the guest network easy without requiring guests to manually enter credentials.

This also avoids sharing the credentials for the primary household network.

### Security Consideration

The guest network is intended to provide Internet access without exposing the primary network to guest devices.

The current implementation uses the router's built-in guest networking and isolation capabilities.

Full VLAN-based segmentation is identified as a future improvement rather than being represented as part of the current configuration.

---

## Wired Network Configuration

Wired connectivity is distributed through the central network infrastructure.

The logical path for wired clients is:

ISP
↓
ISP Gateway
↓
Primary Router
↓
Core Switch
↓
Patch Panel
↓
Structured Cabling
↓
Room Network Drop
↓
Endpoint

The patch panel provides a physical termination point for the structured cabling while the network switch provides connectivity to active network ports.

This separation makes it possible to reconfigure physical connections without modifying the in-wall cabling.

---

## Network Device Connectivity

Stationary devices were prioritized for wired Ethernet connections where practical.

Examples include:

- Desktop computers
- Gaming equipment
- Entertainment devices
- Printers
- Home-lab equipment
- Other stationary devices

Wireless connectivity is primarily used for mobile devices, IoT devices, and devices where a physical Ethernet connection is unnecessary.

---

## Network Security Configuration

Security decisions were incorporated into the network configuration based on the capabilities of the available equipment.

Current controls include:

- ISP gateway operating in bridge mode
- Primary routing performed by a personally controlled router
- Separate guest wireless network
- Guest network isolation
- Separate wireless connectivity for different device requirements
- Private IPv4 addressing behind the router
- Wireless authentication
- Non-public documentation of internal addressing and configuration details

The current network does not yet implement full VLAN segmentation.

Instead, the available guest-network isolation functionality provides an initial level of separation while allowing the network to operate with the existing equipment.

---

## Configuration Validation

Configuration changes were validated through normal network operation and connectivity testing.

Validation included confirming:

- Internet connectivity through the primary router
- Wired client connectivity
- Wireless client connectivity
- Guest wireless connectivity
- DHCP address assignment
- DNS resolution
- Connectivity between networked devices where appropriate
- Physical network connections using cable testing

Additional physical-layer validation is documented separately in:

[Validation & Testing](validation-testing.md)

---

## Configuration Management

Configuration changes were made incrementally rather than changing the entire network simultaneously.

This made it easier to identify the source of problems when changes were introduced.

The physical infrastructure was separated from logical configuration so that:

- Cabling can remain in place while networking equipment changes.
- Switches and routers can be upgraded independently.
- Wireless configuration can change without re-cabling the house.
- Future VLANs and additional network security controls can be introduced without rebuilding the physical infrastructure.

---

## Current State

The network currently provides:

- ISP gateway operating in bridge mode
- Dedicated primary router
- Central switching infrastructure
- Structured Cat6A cabling
- Central patch panel
- Wired network drops throughout the home
- Multiple wireless SSIDs
- Separate guest wireless network
- Guest network isolation
- DHCP-based client addressing
- Static/predictable addressing where required
- Google Public DNS
- Physical-layer cable validation

The architecture intentionally leaves room for future improvements.

---

## Future Configuration Improvements

Potential future improvements include:

- VLAN-based network segmentation
- Dedicated firewall
- IDS/IPS capabilities
- Centralized network monitoring
- DNS filtering
- Network logging
- Dedicated wireless access points
- Managed switching
- More granular IoT isolation
- Home-lab network segmentation
- Centralized authentication and access controls

These improvements will be implemented as the network and home-lab environment expand.
