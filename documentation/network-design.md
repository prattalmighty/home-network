## Network Architecture

The network follows a centralized architecture in which the ISP connection terminates at the modem and is passed to the primary router. Wired network connections are distributed through a central switch and patch panel to individual network drops throughout the home.

The architecture was designed to separate core networking functions from endpoint devices and provide a scalable foundation for future expansion.

![Logical Network Diagram](<../diagrams/Logical Network Diagram.jpg>)

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

![Network Floor Plan](<../diagrams/Structured cabling plan.jpeg>)

The existing low voltage cabinet was in the master bedroom. I decided the new location should be in the guest closet. This is where the ISP wanted to place the gateway so the rack being close to it made the most sense. The guest bed

## Device Connectivity

Wired Devices
 - Desktop computers
 - Printers
 - Gaming/entertainment devices
 - Network infrastructure
 - Other stationary/high-bandwidth devices

Wireless Devices
 - Mobile devices
 - IoT devices
 - Smart-home devices
 - Guest devices

Stationary devices with predictable locations were prioritized for wired connectivity where practical, reducing dependence on wireless bandwidth and improving connection consistency.

## Design Considerations

Scalability

I wanted to build in headroom and future-proof the physical infrastructure. In high-density media areas like the living room, relying solely on downstream desktop switches creates single points of failure and bandwidth bottlenecks. While supply constraints limited that location to a 2-drop run (supplemented by a switch for now), areas like the office/guest room were wired with 3 dedicated drops to cleanly isolate high-bandwidth endpoints (PC, gaming console) while leaving dedicated capacity for peripheral equipment. Planning network capacity around growth rather than immediate need avoids costly re-cabling down the road.

Reliability

Layer 1 reliability directly impacts overall network performance. For high-throughput and latency-sensitive applications—such as media streaming, gaming, and content delivery—Ethernet eliminates RF interference, channel congestion, and packet loss inherent to Wi-Fi. Hardwiring static endpoints frees up wireless spectrum for mobile devices and ensures predictable, low-latency performance across the board.

Performance

Cat6A ensures the structured cabling won't become an infrastructure bottleneck for the foreseeable future. Supporting 10Gbps speeds at full 100-meter distances with enhanced cross-talk mitigation, it provides the physical bandwidth necessary to handle high-volume local traffic, concurrent streaming, and future 10GbE network upgrades without needing in-wall overhauls.

Security

I wanted to put security concepts from my bootcamp into practice using the hardware I had on hand. While I plan to implement full VLAN segmentation down the road, I leveraged my router’s Guest Network (with AP isolation) to segregate untrusted endpoints today.

IoT devices are notorious for unpatched vulnerabilities, so placing them on the guest network prevents them from communicating laterally with my primary PCs, Xbox, and home lab devices. As a bonus, I generated a quick-scan QR code for guests. Giving visitors seamless internet access while keeping my primary LAN completely hidden and secure.

Maintainability

A centralized star topology with a patch panel simplifies administration, troubleshooting, and cable management. Terminating all structured runs next to the demarc and core switching gear keeps the physical layer clean, eliminates scattered point-to-point runs across the building, and allows for quick re-patching or port reconfigurations.

Future Expansion

The current architecture is built to support a phased upgrade roadmap:

Perimeter Security: Deploying a dedicated hardware firewall to enforce strict ingress/egress rules and intrusion detection.

Storage & Compute: Integrating a dedicated NAS for centralized backups/media storage and converting a legacy tower into a home lab hypervisor for self-hosted services.

Ecosystem Upgrade: Transitioning to a unified Ubiquiti ecosystem (managed switches, access points, and UniFi Protect cameras) for centralized management and full-stack visibility.
