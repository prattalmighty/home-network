# Network Design

## Project Overview
This project documents the design and implementation of a residential network built to provide reliable wired and wireless connectivity, support a growing number of connected devices, and provide a foundation for future home-lab and cybersecurity projects.

The network was designed with an emphasis on reliability, security, maintainability, and future expansion. The project included physical network cabling, network equipment installation, wireless configuration, network segmentation, and validation of installed connections.

## Objectives

- Replace/upgrade existing residential network cabling.
- Establish dedicated wired network drops throughout the home.
- Use Cat6A cabling to provide additional bandwidth capability and future-proof the physical infrastructure.
- Centralize network connections through a patch panel and managed switch.
- Provide wired connectivity for high-bandwidth or stationary devices.
- Provide wireless connectivity for mobile and IoT devices.
- Establish separate wireless networks for different trust levels and use cases.
- Provide reliable connectivity throughout the home.
- Create a foundation that can support future home-lab and cybersecurity projects.
- Document and validate the physical network installation.

## Network Architecture

The network follows a centralized architecture in which the ISP connection terminates at the modem and is passed to the primary router. Wired network connections are distributed through a central switch and patch panel to individual network drops throughout the home.

The architecture was designed to separate core networking functions from endpoint devices and provide a scalable foundation for future expansion.

![Network Architecture](../diagrams/network-architecture.png)

Internet
   ↓
ISP Modem
   ↓
Router / Wireless Access Point
   ↓
Network Switch
   ↓
Patch Panel
   ↓
Wired Network Drops
   ↓
Endpoint Devices

## Physical Network Design
The physical network was designed around a centralized network location with structured cabling distributed to key areas of the home. Existing copper cabling was replaced where appropriate, and new Cat6A cable runs were installed between the network location and designated rooms.

Cable drops were planned based on current device requirements as well as anticipated future needs. The resulting design provides wired connectivity to areas containing computers, entertainment devices, and other network-dependent equipment.

## Wireless Network Design
Wireless connectivity was designed using separate networks for different device and trust requirements. Separate SSIDs were established for 5 GHz, 2.4 GHz, and guest connectivity to accommodate device compatibility, performance requirements, and guest access.

A dedicated guest network was configured to prevent guest devices from being placed directly on the primary network. A QR code was created to simplify guest onboarding while allowing the primary network credentials to remain private.

## Device Connectivity

Wired Devices
Desktop computers
Printers
Gaming/entertainment devices
Network infrastructure
Other stationary/high-bandwidth devices

Wireless Devices
Mobile devices
IoT devices
Smart-home devices
Guest devices

Stationary devices with predictable locations were prioritized for wired connectivity where practical, reducing dependence on wireless bandwidth and improving connection consistency.

## Design Considerations

Scalability

Why did you install more drops than you immediately needed?

Reliability

Why did you favor wired connections for certain devices?

Performance

Why Cat6A?

Security

Why separate networks?

Maintainability

Why a centralized patch panel?

Future Expansion

What are you planning to add later?

## Future Improvements

Potential future improvements include:

- Expansion of network segmentation
- Additional network monitoring capabilities
- Expansion of the home-lab environment
- Additional managed networking equipment
- Centralized network monitoring and logging
- Integration with home automation and security monitoring
