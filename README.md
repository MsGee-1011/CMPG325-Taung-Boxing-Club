# CMPG 325 – Computer Networks Project

## Taung Boxing Club – Taung

**Client ID:** CLI-118
**Organisation:** Taung Boxing Club
**Industry:** Sports
**Location:** Taung

---

## Project Overview

This project focuses on the analysis, design, simulation and testing of a computer network for **Taung Boxing Club** in Taung.

The network will be designed and implemented using **Cisco Packet Tracer**. The solution will provide appropriate network connectivity and services while considering scalability, reliability and the client's specific networking requirements.

The project uses the assigned addressing block **172.30.78.0/23**.

---

## Client Requirements

The network design must:

* Provide appropriate connectivity for Taung Boxing Club.
* Provide appropriate network services.
* Use the assigned `172.30.78.0/23` addressing block.
* Accommodate an expected **40% user growth within three years**.
* Provide a scalable network design.
* Implement and demonstrate **EtherChannel (link aggregation)**.
* Accommodate **CR 15 – Second Internet Connection** for resilience.
* Provide successful end-to-end connectivity.
* Be implemented and tested using Cisco Packet Tracer.

---

## Network Design

The proposed network will use routers, switches and end devices to provide connectivity throughout the organisation.

The network will use VLANs to logically separate different categories of users and network services.

### Proposed VLANs

| VLAN    | Purpose            |
| ------- | ------------------ |
| VLAN 10 | Administration     |
| VLAN 20 | Coaches/Staff      |
| VLAN 30 | Members            |
| VLAN 40 | Guests             |
| VLAN 50 | Servers            |
| VLAN 99 | Network Management |

---

## Assigned Networking Challenge

### EtherChannel

The assigned networking challenge for this project is **EtherChannel (Link Aggregation)**.

Multiple physical links between the switches will be configured as a single logical EtherChannel connection.

The implementation will be configured, verified and tested in Cisco Packet Tracer.

---

## Client Change Request

### CR 15 – Second Internet Connection

The client has requested a second Internet connection for resilience.

The final network design will therefore incorporate two Internet connections and provide an alternative Internet path if the primary connection becomes unavailable.

---

## IP Addressing

The assigned addressing block is:

`172.30.78.0/23`

The address block will be subnetted according to the requirements of the different VLANs and network segments.

The addressing plan will also reserve sufficient address space to support the required **40% user growth within three years**.

---

## Project Evidence

The GitHub portfolio will contain evidence of:

* Client requirements analysis
* Physical network topology
* Logical network topology
* IP addressing plan
* Cisco Packet Tracer implementation
* Device configuration
* EtherChannel configuration and verification
* Second Internet connection implementation
* Connectivity testing
* Troubleshooting
* Screenshots and supporting evidence
* Project reflection

---

## Project Milestones

### Milestone 1 – Client Design Review

* [x] Client requirements identified
* [ ] Physical topology
* [ ] Logical topology
* [ ] IP addressing plan
* [x] Initial GitHub repository

### Milestone 2 – Client Implementation Review

* [ ] Packet Tracer implementation
* [ ] Assigned feature implemented
* [ ] Testing completed
* [ ] Evidence collected

### Final Submission

* [ ] Final Packet Tracer file
* [ ] GitHub portfolio
* [ ] Technical report
* [ ] 15–20 minute individual video demonstration
* [ ] Additional evidence as required

---

## Project Scope

This project is specifically designed for **Taung Boxing Club (Taung)** and follows the assigned client scenario, addressing block, networking challenge and change request provided for CMPG 325.

The project will be developed and documented as an individual project, with evidence showing the development, configuration, testing and troubleshooting process.
