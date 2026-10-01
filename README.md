# CMPG325 – Computer Networks Project

# Taung Boxing Club – Taung

**Client ID:** CLI-118
**Organisation:** Taung Boxing Club
**Industry:** Sports
**Location:** Taung, South Africa

---

# Milestone 2 – Client Implementation Review

## 1. Project Overview

This project focuses on the analysis, design, implementation and testing of a computer network for Taung Boxing Club in Taung.

The network was implemented using Cisco Packet Tracer and provides:

* VLAN segmentation
* Inter-VLAN routing
* EtherChannel link aggregation
* Trunking
* Connectivity testing
* Scalability for future growth

The project also considers the CR15 requirement for a second Internet connection for improved resilience. Any redundancy features are documented separately where implemented and tested.

---

## 2. Working Packet Tracer Implementation

The following devices were implemented in Cisco Packet Tracer:

### Core Layer

* Core-SW (Cisco 3560 Layer 3 Switch)

### Access Layer

* Access-SW1
* Access-SW2

### Routing Infrastructure

* Router-Primary
* Router-Backup

### Wireless Infrastructure

* WRT300N Wireless Router

### End Devices

* Management PC
* Staff PCs
* Guest PCs

The completed Packet Tracer file has been uploaded to the repository as evidence of the network implementation.

---

## 3. VLAN Design

| VLAN | Name       | Purpose                               | Network          | Gateway       |
| ---- | ---------- | ------------------------------------- | ---------------- | ------------- |
| 10   | MANAGEMENT | Management and administration devices | 172.30.78.0/26   | 172.30.78.1   |
| 20   | STAFF      | Staff workstations                    | 172.30.78.64/26  | 172.30.78.65  |
| 30   | TRAINING   | Training and member devices           | 172.30.78.128/26 | 172.30.78.129 |
| 40   | GUEST      | Guest and visitor devices             | 172.30.78.192/27 | 172.30.78.193 |
| 99   | NATIVE     | Native VLAN for trunk links           | N/A              | N/A           |

---

## 4. IP Addressing

The assigned address block for the project is:

```text
172.30.78.0/23
```

VLSM was used to divide the address block into smaller subnets to support the network requirements and future growth.

### SVI Gateways

* VLAN 10: `172.30.78.1`
* VLAN 20: `172.30.78.65`
* VLAN 30: `172.30.78.129`
* VLAN 40: `172.30.78.193`

VLAN 99 is used as the Native VLAN and therefore does not require an SVI.

---

## 5. Assigned Networking Challenge

### EtherChannel (LACP)

The assigned networking challenge for this project was EtherChannel.

EtherChannel was configured using LACP to logically combine multiple physical links between switches.

### Port-Channel 1

Core-SW ↔ Access-SW1

```text
Gi0/1 + Gi0/2
```

### Port-Channel 2

Core-SW ↔ Access-SW2

```text
Fa0/23 + Fa0/24
```

### EtherChannel Verification

Verification command:

```bash
show etherchannel summary
```

The verification showed:

```text
Po1(SU)
Po2(SU)
```

Meaning:

* **S** = Layer 2 EtherChannel
* **U** = EtherChannel in use

The results confirm that the EtherChannel interfaces were operational.

---

## 6. Trunk Configuration

The EtherChannel interfaces were configured as IEEE 802.1Q trunk ports.

### Native VLAN

```text
VLAN 99
```

### Active VLANs

```text
1, 10, 20, 30, 40, 99
```

Verification command:

```bash
show interfaces trunk
```

The verification confirmed trunk operation between the Core Switch and Access Switches.

---

## 7. Inter-VLAN Routing

Inter-VLAN routing was configured on the Core Layer 3 Switch using Switched Virtual Interfaces (SVIs).

Verification command:

```bash
show ip interface brief
```

### Verified VLAN Interfaces

| VLAN    | IP Address    | Status |
| ------- | ------------- | ------ |
| VLAN 10 | 172.30.78.1   | Up/Up  |
| VLAN 20 | 172.30.78.65  | Up/Up  |
| VLAN 30 | 172.30.78.129 | Up/Up  |
| VLAN 40 | 172.30.78.193 | Up/Up  |

---

## 8. Testing Evidence

The implementation was tested using Cisco Packet Tracer verification commands and connectivity tests.

### VLAN Verification

Command:

```bash
show vlan brief
```

The required VLANs were successfully created and active.

The verified VLANs were:

* VLAN 10 – MANAGEMENT
* VLAN 20 – STAFF
* VLAN 30 – TRAINING
* VLAN 40 – GUEST
* VLAN 99 – NATIVE

---

### SVI Verification

Command:

```bash
show ip interface brief
```

The configured SVIs were verified as **up/up** for VLANs 10, 20, 30 and 40.

---

### EtherChannel Verification

Command:

```bash
show etherchannel summary
```

The Core Switch showed active Port-Channels:

```text
Po1(SU)
Po2(SU)
```

---

### Trunk Verification

Command:

```bash
show interfaces trunk
```

The trunks were verified using Native VLAN 99 with the required VLANs active and forwarding.

---

### Connectivity Testing

#### Test 1: Staff PC → Staff VLAN Gateway

```bash
ping 172.30.78.65
```

Result:

```text
4 packets sent
4 packets received
0% packet loss
```

**Result: Successful**

This confirms connectivity from the Staff PC to the VLAN 20 default gateway.

---

#### Test 2: Management PC → Management VLAN Gateway

```bash
ping 172.30.78.1
```

Result:

```text
4 packets sent
4 packets received
0% packet loss
```

**Result: Successful**

This confirms connectivity from the Management PC to the VLAN 10 gateway.

---

#### Test 3: Guest PC → Guest VLAN Gateway

```bash
ping 172.30.78.193
```

Result:

```text
4 packets sent
4 packets received
0% packet loss
```

**Result: Successful**

This confirms connectivity from the Guest PC to the VLAN 40 default gateway.

---

## 9. Evidence Included in Repository

The following evidence has been collected for the Client Implementation Review.

### EtherChannel Verification

* `EtherChannel_CoreSW.png`

### VLAN Verification

* `VLAN_Verification.png`

### Trunk Verification

* `Trunk_Verification.png`

### SVI Verification

* `SVI_Verification.png`

### Connectivity Testing

* `Ping_Gateway.png`
* `Ping_Management.png`
* `Ping_Guest.png`

### Documentation

* `Milestone2_Report.md`

### Packet Tracer Implementation

* `CMPG325_CLI118_Milestone2.pkt`

---

## 10. Milestone 2 Deliverables

The following Client Implementation Review requirements have been addressed:

* Working Packet Tracer implementation
* Assigned networking challenge implemented using EtherChannel
* VLAN configuration completed
* Trunk configuration completed
* Inter-VLAN routing configured
* Connectivity testing completed
* Testing and verification evidence collected
* GitHub repository updated

---

## 11. Conclusion

The Taung Boxing Club network was implemented and tested using Cisco Packet Tracer.

The assigned networking challenge, EtherChannel using LACP, was configured and verified. VLAN segmentation, trunking, Inter-VLAN routing and gateway connectivity were also configured and tested.

The collected screenshots and Packet Tracer file provide evidence of the implemented network and its verification for the Milestone 2 Client Implementation Review.
