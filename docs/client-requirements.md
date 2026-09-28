# Taung Boxing Club – Client Requirements

## 1. Client Information

| Item | Details |
|--------|--------|
| Client ID | CLI-118 |
| Organisation | Taung Boxing Club (Taung) |
| Industry | Sports |
| Project | CMPG325 Computer Networks |
| Assigned Address Block | 172.30.78.0/23 |
| Assigned Networking Challenge | EtherChannel |
| Change Request | CR15 – Second Internet Connection |

---

## 2. Project Background

Taung Boxing Club requires a reliable, scalable and secure computer network to support administrative operations, staff communication, member activities and guest connectivity.

The network solution will be designed and implemented using Cisco Packet Tracer in accordance with the requirements specified in the CMPG325 project brief.

The design must support current operational requirements while providing sufficient capacity for future expansion and growth.

---

## 3. Network Requirements

The network must:

- Provide reliable connectivity between all authorised devices.
- Support communication between users and network services.
- Provide secure and organised network segmentation.
- Use the assigned address block of 172.30.78.0/23.
- Provide inter-VLAN communication where required.
- Support appropriate network services.
- Support wireless connectivity for guest users.
- Be fully implemented and tested using Cisco Packet Tracer.
- Support future organisational growth.
- Provide resilience through a secondary Internet connection.

---

## 4. VLAN Requirements

The network will use VLANs to separate users and services into logical groups.

| VLAN | Name | Purpose |
|--------|--------|--------|
| 10 | MANAGEMENT | Administrative and management devices |
| 20 | STAFF | Staff and coaching personnel |
| 30 | TRAINING | Training and member devices |
| 40 | GUEST | Guest users and wireless clients |
| 50 | SERVERS | Servers and network services |
| 99 | NATIVE | Native VLAN for trunk links |

### Benefits of VLAN Segmentation

- Improved security
- Reduced broadcast traffic
- Better network performance
- Easier administration
- Improved scalability

---

## 5. Addressing Requirements

The assigned IP address block for the project is:

```text
172.30.78.0/23
```

The addressing plan must:

- Use only the assigned address block.
- Provide separate subnets for each VLAN.
- Support current and future devices.
- Reserve address space for growth.
- Use VLSM to improve address utilisation.

The network must support an expected growth of approximately 40% within three years.

---

## 6. Assigned Networking Challenge

### EtherChannel (Link Aggregation)

The assigned networking challenge for this project is EtherChannel.

EtherChannel combines multiple physical connections between switches into a single logical connection.

The implementation uses:

- Link Aggregation Control Protocol (LACP)
- Multiple physical switch links
- Logical Port-Channels
- Trunk connections carrying multiple VLANs

### Benefits of EtherChannel

- Increased bandwidth
- Redundancy
- Improved reliability
- Load balancing
- Simplified management

### Verification Commands

EtherChannel operation will be verified using:

```bash
show etherchannel summary
```

```bash
show interfaces trunk
```

Successful EtherChannel operation is indicated by:

```text
Po1(SU)
Po2(SU)
```

Where:

- S = Layer 2 EtherChannel
- U = EtherChannel in use

---

## 7. Change Request CR15 – Second Internet Connection

The client has requested a second Internet connection to improve network availability and resilience.

The final design must therefore include:

- Primary Internet connection
- Secondary Internet connection
- Appropriate routing configuration
- Alternative connectivity path
- Connectivity testing and failover verification

This ensures that Internet access remains available if the primary connection becomes unavailable.

---

## 8. Scalability Requirement

The network must support:

```text
40% user growth within three years
```

The design must therefore:

- Allow additional users to be added.
- Support future devices.
- Reserve IP address space.
- Avoid requiring a complete redesign.

---

## 9. Physical Network Requirements

The implementation must include:

### Network Infrastructure

- Core Layer 3 Switch
- Access Layer Switches
- Primary Router
- Secondary Router
- Wireless Router / Access Point

### End Devices

- Management PC
- Staff PCs
- Guest PCs

### Network Features

- VLANs
- Trunk Links
- EtherChannel
- Inter-VLAN Routing
- Internet Connectivity

---

## 10. Testing Requirements

The completed network must be tested to verify correct operation.

### Connectivity Testing

- Device-to-device connectivity
- Device-to-gateway connectivity
- Inter-VLAN communication
- End-to-end connectivity

### Configuration Verification

- VLAN verification
- Trunk verification
- EtherChannel verification
- Routing verification

### Verification Commands

```bash
show vlan brief
```

```bash
show interfaces trunk
```

```bash
show etherchannel summary
```

```bash
show ip interface brief
```

Screenshots and command outputs will be collected as evidence for the GitHub portfolio and final submission.

---

## 11. Project Deliverables

### Milestone 1 – Client Design Review

- Client Requirements
- Physical Topology
- Logical Topology
- IP Addressing Plan
- Initial GitHub Repository

### Milestone 2 – Client Implementation Review

- Packet Tracer Implementation
- EtherChannel Implementation
- Testing Evidence
- Updated GitHub Portfolio

### Final Submission

- Final Packet Tracer File
- GitHub Portfolio
- Technical Documentation
- Video Demonstration
- Supporting Evidence

---

## 12. Project Scope

This project is specifically developed for:

**Taung Boxing Club (Taung)**

**Client ID: CLI-118**

The solution follows the assigned addressing block, networking challenge and change request provided in the CMPG325 project brief.

No additional features will be introduced unless required to support the stated project requirements.

---

## 13. Conclusion

The proposed network provides a secure, scalable and reliable solution for Taung Boxing Club.

The design incorporates VLAN segmentation, EtherChannel implementation, inter-VLAN routing, future growth planning and support for a secondary Internet connection while remaining aligned with the project requirements and assessment criteria.
