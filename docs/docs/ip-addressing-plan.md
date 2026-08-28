# Taung Boxing Club – IP Addressing Plan

## 1. Assigned Addressing Block

The addressing block assigned to Taung Boxing Club is:

**172.30.78.0/23**

The /23 network provides a total of 512 IPv4 addresses, with 510
usable host addresses.

The address range is:

**172.30.78.0 – 172.30.79.255**

VLSM is used to divide the addressing block into smaller networks for the
different VLANs.

The addressing plan has been designed to provide suitable capacity for
the current network and the expected 40% user growth over the next three
years.

## 2. VLAN Addressing Plan

| VLAN | Name | Network Address | Prefix | Subnet Mask | Default Gateway | Usable Host Range |
|---|---|---|---|---|---|---|
| 10 | ADMIN | 172.30.78.0 | /26 | 255.255.255.192 | 172.30.78.1 | 172.30.78.1 – 172.30.78.62 |
| 20 | STAFF | 172.30.78.64 | /26 | 255.255.255.192 | 172.30.78.65 | 172.30.78.65 – 172.30.78.126 |
| 30 | MEMBERS | 172.30.78.128 | /25 | 255.255.255.128 | 172.30.78.129 | 172.30.78.129 – 172.30.78.254 |
| 40 | GUESTS | 172.30.79.0 | /26 | 255.255.255.192 | 172.30.79.1 | 172.30.79.1 – 172.30.79.62 |
| 50 | SERVERS | 172.30.79.64 | /27 | 255.255.255.224 | 172.30.79.65 | 172.30.79.65 – 172.30.79.94 |
| 99 | MANAGEMENT | 172.30.79.96 | /28 | 255.255.255.240 | 172.30.79.97 | 172.30.79.97 – 172.30.79.110 |

## 3. Subnet Allocation

### VLAN 10 – ADMIN

- Network: 172.30.78.0/26
- Gateway: 172.30.78.1
- Usable addresses: 172.30.78.1 – 172.30.78.62
- Broadcast: 172.30.78.63

This subnet provides 62 usable host addresses for administration
devices.

### VLAN 20 – STAFF

- Network: 172.30.78.64/26
- Gateway: 172.30.78.65
- Usable addresses: 172.30.78.65 – 172.30.78.126
- Broadcast: 172.30.78.127

This subnet provides 62 usable host addresses for staff devices.

### VLAN 30 – MEMBERS

- Network: 172.30.78.128/25
- Gateway: 172.30.78.129
- Usable addresses: 172.30.78.129 – 172.30.78.254
- Broadcast: 172.30.78.255

This is the largest user subnet because the membership network is expected
to contain the greatest number of devices and provides additional
capacity for future growth.

### VLAN 40 – GUESTS

- Network: 172.30.79.0/26
- Gateway: 172.30.79.1
- Usable addresses: 172.30.79.1 – 172.30.79.62
- Broadcast: 172.30.79.63

This subnet provides 62 usable host addresses for guest devices.

### VLAN 50 – SERVERS

- Network: 172.30.79.64/27
- Gateway: 172.30.79.65
- Usable addresses: 172.30.79.65 – 172.30.79.94
- Broadcast: 172.30.79.95

This subnet provides 30 usable host addresses for servers and network
services.

### VLAN 99 – MANAGEMENT

- Network: 172.30.79.96/28
- Gateway: 172.30.79.97
- Usable addresses: 172.30.79.97 – 172.30.79.110
- Broadcast: 172.30.79.111

This subnet provides 14 usable host addresses for network management
interfaces.

## 4. Reserved Address Space

The remaining addresses in the assigned /23 block are reserved for
future expansion.

This supports the client's requirement for approximately 40% user growth
within three years and allows additional network devices or subnets to be
introduced without immediately redesigning the entire addressing scheme.

## 5. Network Device Addressing

The first usable address in each VLAN is reserved for the default gateway
on the router.

For example:

- VLAN 10 gateway: 172.30.78.1
- VLAN 20 gateway: 172.30.78.65
- VLAN 30 gateway: 172.30.78.129
- VLAN 40 gateway: 172.30.79.1
- VLAN 50 gateway: 172.30.79.65
- VLAN 99 gateway: 172.30.79.97

End devices will use addresses from the corresponding VLAN subnet.

## 6. Design Considerations

VLSM was selected because different departments and network services have
different addressing requirements.

The MEMBERS VLAN receives the largest subnet because it is expected to
support more devices.

The ADMIN, STAFF and GUESTS VLANs receive /26 networks, while the SERVERS
and MANAGEMENT VLANs receive smaller networks appropriate to their
expected number of devices.

The design also leaves unused address space within the assigned /23 block
for future expansion.

## 7. Summary

The IP addressing design:

- Uses only the assigned 172.30.78.0/23 address block.
- Separates users and services into VLANs.
- Provides dedicated default gateways.
- Uses VLSM to allocate addresses efficiently.
- Allows for future network growth.
- Supports the Taung Boxing Club network topology.
