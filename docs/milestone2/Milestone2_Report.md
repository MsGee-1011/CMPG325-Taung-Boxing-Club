# Milestone 2 – Client Implementation Review
 
## Introduction
 
This milestone focused on implementing the approved network design for Taung Boxing Club using Cisco Packet Tracer.
 
## Working Packet Tracer Implementation
 
The following devices were implemented:
 
- Core-SW (Cisco 3560 Layer 3 Switch)
- Access-SW1
- Access-SW2
- Router-Primary
- Router-Backup
- WRT300N Wireless Router
- Management PC
- Staff PCs
- Guest PCs
 
## Assigned Networking Challenge
 
### EtherChannel (LACP)
 
The assigned networking challenge was EtherChannel.
 
The following Port-Channels were successfully implemented:
 
#### Port-Channel 1
 
Core-SW Gi0/1-2 ↔ Access-SW1 Gi0/1-2
 
#### Port-Channel 2
 
Core-SW Fa0/23-24 ↔ Access-SW2 Fa0/23-24
 
### Verification
 
Verification was completed using:
 
```bash
show etherchannel summary
```
 
Results:
 
```text
Po1(SU)
Po2(SU)
```
 
## Testing Evidence
 
The following connectivity tests were completed successfully:
 
### Test 1
 
Staff-PC1 → VLAN 20 Gateway
 
```bash
ping 172.30.78.65
```
 
Result: Successful
 
### Test 2
 
Staff-PC1 → Management-PC
 
```bash
ping 172.30.78.2
```
 
Result: Successful
 
### Test 3
 
Staff-PC1 → Guest-PC1
 
```bash
ping 172.30.78.194
```
 
Result: Successful
 
## Verification Commands
 
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
 
## Conclusion
 
The Packet Tracer implementation was successfully completed.
 
The EtherChannel networking challenge was implemented and verified using LACP.
 
Connectivity testing confirmed successful communication between VLANs and devices.