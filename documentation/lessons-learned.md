# Lessons Learned

## Overview

Building the home network provided an opportunity to apply concepts from my cybersecurity training to a real-world environment.

Unlike a lab environment, the network had to support the day-to-day needs of a household while also being reliable enough to remain operational as additional devices and projects were introduced.

The project reinforced that successful IT infrastructure is not simply about making something work. It also requires planning, documentation, validation, troubleshooting, maintainability, and consideration of future requirements.

---

## Plan for Growth, Not Just the Current Requirement

One of the biggest lessons from the project was the importance of planning for future requirements.

It would have been possible to install only enough network drops for the devices that existed at the time.

Instead, cable runs were planned around both current and anticipated device requirements.

This resulted in additional network capacity in areas where multiple devices were likely to be installed.

### Lesson

When physical infrastructure is difficult or expensive to modify later, it is worth considering future requirements during the initial installation.

Adding an additional cable run during construction is considerably easier than discovering later that another dedicated connection is required.

---

## The Existing Wiring Infrastructure Was an Asset

The house already contained a structured wiring panel with existing telephone and coaxial connections.

Initially, this appeared to be the natural location for the network equipment.

However, the location had several limitations:

- Limited physical space
- Poor accessibility
- Limited ventilation
- Restricted room for future expansion
- Located in an inconvenient area of the house

Rather than treating the existing panel as the permanent network location, I separated the structured wiring function from the primary network infrastructure.

The existing cables were re-terminated and connected to a switch within the original panel.

A single uplink was then used to connect that location back to the primary network infrastructure.

### Lesson

Existing infrastructure does not necessarily dictate the final architecture.

The better solution was to reuse the useful parts of the existing installation while moving the primary network equipment to a more suitable location.

---

## Physical Infrastructure Matters

The project reinforced the importance of Layer 1 when troubleshooting network problems.

A network configuration can be correct while a physical connection remains faulty.

Installing the Cat6A cabling required:

- Planning cable routes
- Pulling cable through the attic
- Creating room drops
- Terminating wall outlets
- Terminating the patch panel
- Creating patch cables
- Testing individual connections

Cable testing was used to verify that individual connections were correctly terminated.

### Lesson

Troubleshooting should begin with the fundamentals.

Before assuming that a router, switch, operating system, or application is responsible for a connectivity problem, the physical connection should be verified.

---

## Centralization Improved Maintainability

The use of a central patch panel and network switch created a predictable physical topology.

Instead of having individual cables running directly between rooms and networking equipment, room drops terminate at the patch panel.

This makes it possible to change which switch port serves a room without modifying the permanent cabling.

### Lesson

A network should be designed so that common changes can be made without rebuilding the underlying infrastructure.

Centralization also makes troubleshooting easier because the physical connection path is known and documented.

---

## Wired vs. Wireless Connectivity

The project reinforced that wireless connectivity is not always the best solution for stationary devices.

Devices such as desktop computers, gaming equipment, and other high-bandwidth stationary equipment benefit from wired Ethernet because it provides a predictable physical connection without relying on wireless spectrum.

Wireless remains useful for mobile devices, IoT devices, and equipment where physical cabling would provide little benefit.

### Lesson

The goal is not to eliminate wireless networking.

The goal is to use the appropriate connectivity method for the device and its requirements.

---

## Network Segmentation Is a Process

The network currently uses separate wireless networks and guest-network isolation to provide a degree of separation between trusted and untrusted devices.

However, the project also demonstrated the limitations of relying solely on consumer router features.

Full VLAN-based segmentation would provide more granular control over different device categories.

### Lesson

Security should be implemented according to both risk and available capabilities.

The current network provides a reasonable improvement over placing every device on a single unrestricted network, while leaving a clear path toward more advanced segmentation.

---

## Security vs. Convenience

The guest network presented a practical example of balancing security with usability.

Guests should be able to access the Internet without being given the credentials for the primary household network.

A separate guest network provides that separation while a QR code makes onboarding simple.

### Lesson

Security controls are more likely to be used consistently when they do not create unnecessary friction.

A technically secure solution that nobody wants to use is not necessarily a successful solution.

---

## Troubleshooting Through Layers

The project reinforced the value of troubleshooting from the bottom of the technology stack upward.

For a connectivity problem, the troubleshooting process can begin with:

1. Physical connection
2. Link status
3. Switch connectivity
4. IP address
5. DHCP
6. DNS
7. Routing
8. Firewall or access controls
9. Application or service

This layered approach reduces the likelihood of making unnecessary configuration changes before establishing where the failure actually occurs.

### Lesson

Good troubleshooting is a process of elimination.

The objective is not to guess the solution quickly.

The objective is to identify the failure point, gather evidence, make the smallest appropriate change, and verify the result.

---

## Documentation Became Part of the Solution

Documenting the network forced me to think about the infrastructure differently.

Creating diagrams and written documentation made it easier to understand:

- Where cables terminate
- How devices connect
- Why equipment was placed where it was
- Which decisions were intentional
- Which areas could be improved
- How future upgrades could be introduced

### Lesson

Documentation is not just something created after an IT project.

Creating documentation during the project can expose design problems and make future troubleshooting significantly easier.

---

## What I Would Do Differently

If I were rebuilding the network today, I would consider several improvements.

### More Network Drops

Where practical, I would install additional dedicated Ethernet runs in areas with multiple high-bandwidth devices.

### More Advanced Segmentation

I would design VLANs for categories such as:

- Trusted clients
- IoT devices
- Guest devices
- Home-lab systems
- Network infrastructure

### Dedicated Firewall

A dedicated firewall would provide more granular control over traffic entering and leaving the network.

### Centralized Monitoring

I would add centralized monitoring and logging to make it easier to identify connectivity problems and unusual network activity.

### Dedicated Wireless Access Points

As the network grows, dedicated access points would provide greater flexibility than relying on the wireless functionality built into the primary router.

---

## What Surprised Me

One of the biggest takeaways from the project was how many problems can be created or solved before a network packet ever reaches a router.

Cable routing, termination, labeling, physical accessibility, and equipment placement all affect the reliability and maintainability of the final network.

The project also demonstrated how seemingly small infrastructure decisions can have long-term consequences.

---

## Skills Reinforced

This project provided practical experience with:

- Network design
- Structured cabling
- Cat6A installation
- Ethernet termination
- Patch panels
- Network switches
- Router configuration
- DHCP
- DNS
- Wireless networking
- Guest network configuration
- Network segmentation concepts
- Network troubleshooting
- Physical-layer validation
- Documentation
- Technical decision-making
- Infrastructure planning

---

## Final Takeaway

The most important lesson from the project was that reliable IT infrastructure is built through a combination of planning, implementation, testing, documentation, and continuous improvement.

The network works today, but the design also gives me a foundation that can be expanded as my technical skills and home-lab requirements grow.

Rather than treating the project as finished once devices could connect to the Internet, I treat it as an ongoing infrastructure project that can be measured, documented, improved, and used as a platform for learning.
