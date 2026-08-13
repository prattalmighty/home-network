# Home Network Infrastructure

## Overview

I designed and implemented a structured home network to replace and expand the home's original networking infrastructure.

The project included planning the network topology, installing new Cat6A cable runs throughout the home, re-terminating existing cabling, building a centralized patch-panel and switching infrastructure, configuring the network, and validating the completed cable runs.

The project was designed with future expansion, reliability, security, and maintainability in mind.

## Objectives

- Replace aging and limited network infrastructure
- Establish a centralized network distribution point
- Provide wired network connectivity to key rooms
- Install Cat6A cabling to support future network upgrades
- Improve network organization and maintainability
- Separate trusted and guest wireless access
- Build a foundation for future network expansion

## Project Scope

- Network planning and topology design
- Structured Cat6A cabling
- Patch panel installation
- Keystone termination
- Custom patch cable fabrication
- Network switch configuration
- Router configuration
- Wireless network configuration
- Guest network implementation
- Static IP configuration
- Cable testing and validation
- Network documentation

## Network Design

### Network Topology

[View Network Diagram](../diagrams/network-topology.png)

### Physical Layout

[View Floor Plan](../diagrams/floor-plan.png)

The floor plan was used during planning to identify device locations and determine the required network drops throughout the home.

## Infrastructure

The project included a centralized network rack as well as the repurposing of the home's original structured wiring panel.

The original panel contained existing telephone and coaxial cabling. Because the panel was small, enclosed, and poorly suited for future expansion, it was not selected as the primary network location.

Existing cabling was re-terminated and connected to a switch, allowing the existing room runs to be brought back to the primary network infrastructure using a single uplink.

## Structured Cabling

New Cat6A runs were pulled through the attic to provide wired connectivity to multiple rooms.

Wall connections were terminated using keystone jacks, while the centralized connections were terminated directly into a patch panel.

Custom patch cables were also fabricated as needed.

## Network Configuration

The network includes:

- Wired Ethernet
- 2.4 GHz wireless
- 5 GHz wireless
- Guest wireless network
- Static IP assignments
- Secure guest network access
- Network switching
- Router-based network management

A QR code was created to simplify guest access to the designated guest network without exposing the primary network.

## Validation

Completed cable runs were tested to verify continuity and correct pair mapping before being placed into service.

[View cable testing documentation](documentation/validation-testing.md)

## Security Considerations

Security considerations during the project included:

- Separate guest network
- Restricted guest access
- Secure wireless configuration
- Avoiding unnecessary exposure of internal network information
- Planning for future network segmentation

## Documentation

Detailed implementation documentation is available in the [`documentation`](documentation/) directory.

## Future Improvements

Planned future improvements include:

- Expanded network segmentation
- Additional monitoring
- Improved centralized management
- Further network automation
- Additional infrastructure as the network grows

