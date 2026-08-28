# Taung Boxing Club – Client Requirements

## 1. Client Information

| Item | Details |
|---|---|
| Client ID | CLI-118 |
| Organisation | Taung Boxing Club (Taung) |
| Industry | Sports |
| Project | CMPG325 Computer Networks |
| Assigned Addressing Block | 172.30.78.0/23 |

## 2. Client Background

Taung Boxing Club is the assigned client organisation for this CMPG325
Computer Networks project. The network solution is designed specifically
for Taung Boxing Club and follows the requirements, constraints,
addressing block, networking challenge and change request provided in the
project brief.

The solution must provide appropriate network connectivity and services
for the organisation while allowing for future growth.

## 3. Network Requirements

The Taung Boxing Club network must:

- Provide reliable connectivity between appropriate network devices.
- Support communication between users and network services.
- Provide appropriate network services for the organisation.
- Use the assigned IP addressing block of 172.30.78.0/23.
- Use an appropriate physical and logical network topology.
- Use VLANs to separate different areas of the organisation's network.
- Provide inter-VLAN communication where required.
- Be implemented and simulated using Cisco Packet Tracer.
- Be fully testable using connectivity and configuration tests.
- Allow the network to accommodate expected user growth.

## 4. VLAN Requirements

The proposed network separates users and services using VLANs:

| VLAN | Name | Purpose |
|---|---|---|
| 10 | ADMIN | Administration users |
| 20 | STAFF | Boxing club staff |
| 30 | MEMBERS | Club members and member devices |
| 40 | GUESTS | Guest network access |
| 50 | SERVERS | Network servers and services |
| 99 | MANAGEMENT | Network device management |

VLAN separation improves network organisation and allows different groups
of devices to be managed separately.

## 5. Addressing Requirement

The assigned addressing block is:

**172.30.78.0/23**

The addressing plan is designed using subnetting/VLSM to provide suitable
address space for the different VLANs while allowing for future growth.

The network must accommodate an expected **40% user growth within three
years**.

## 6. Networking Challenge

### EtherChannel (Link Aggregation)

The assigned networking challenge for this project is:

**EtherChannel (Link Aggregation)**

The network must configure, verify and demonstrate EtherChannel.

The implementation uses multiple physical links between the switches as
one logical link. LACP is used to negotiate and maintain the EtherChannel.

The EtherChannel provides:

- Increased link capacity.
- Redundancy between the switches.
- Improved availability.
- A logical trunk connection between the switches.

The EtherChannel configuration will be verified using Cisco IOS commands
such as:

`show etherchannel summary`

and

`show interfaces trunk`

## 7. Change Request – CR15

The client has requested that a **second Internet connection** be added
for resilience.

The final network must accommodate this change request by providing a
secondary Internet path.

The design will therefore include:

- A primary Internet connection.
- A secondary Internet connection.
- Appropriate routing between the network and Internet connections.
- Testing to demonstrate that the network can use the alternative
  connection when the primary connection is unavailable.

## 8. Design Constraint

The main design constraint is:

**Expected 40% user growth within three years.**

The network addressing and topology must therefore provide sufficient
capacity for future users and devices without requiring a complete redesign
of the network.

## 9. Implementation Requirements

The network will be designed and simulated using **Cisco Packet Tracer**.

The implementation must include appropriate:

- Routers
- Switches
- End devices
- VLANs
- Trunk links
- IP addressing
- Inter-VLAN routing
- EtherChannel
- Internet connections
- Routing and resilience configuration

## 10. Testing Requirements

The completed network must be tested to confirm that it operates as
required.

Testing will include:

- Testing connectivity between devices.
- Testing VLAN gateway connectivity.
- Testing inter-VLAN communication.
- Verifying VLAN configuration.
- Verifying trunk links.
- Verifying EtherChannel operation.
- Testing the second Internet connection.
- Testing resilience/failover where applicable.
- Recording troubleshooting performed during implementation.

Screenshots and command outputs will be collected as evidence.

## 11. Project Deliverables

The project requires:

1. Client requirements documentation.
2. Physical topology.
3. Logical topology.
4. IP addressing plan.
5. Cisco Packet Tracer implementation.
6. Configuration and testing evidence.
7. Individual GitHub portfolio.
8. Final Packet Tracer file.
9. Technical documentation.
10. Individual 15–20 minute video demonstration with an inset webcam view.

## 12. Scope

This project remains specific to **Taung Boxing Club (Taung), Client ID
CLI-118**.

The solution follows the assigned addressing block, design constraint,
EtherChannel networking challenge and CR15 change request. Additional
features will not be introduced unless they are required to implement or
support the specified project requirements.
