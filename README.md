# Small Office Network — Cisco Packet Tracer

A small office LAN built to practise Cisco switch and router configuration, IP addressing and connectivity testing.

## Topology

- 3 office PCs
- 1 Cisco 2960 switch
- 1 Cisco 1941 router
- 1 setup laptop for console access
- Ethernet connections for network traffic
- Console cable for device configuration

## IP address plan

Network: **192.168.10.0/29**  
Subnet mask: **255.255.255.248**  
Usable addresses: **192.168.10.1–192.168.10.6**  
Broadcast: **192.168.10.7**

A /29 provides six usable addresses: enough for the three PCs, switch management interface and router LAN interface, with one spare.

| Device | Interface | IP address | Default gateway |
|---|---|---|---|
| Office-R1 | GigabitEthernet0/0 | 192.168.10.1 | — |
| Office-SW1 | VLAN 1 | 192.168.10.2 | 192.168.10.1 |
| PC0 | FastEthernet0 | 192.168.10.3 | 192.168.10.1 |
| PC1 | FastEthernet0 | 192.168.10.4 | 192.168.10.1 |
| PC2 | FastEthernet0 | 192.168.10.5 | 192.168.10.1 |

The setup laptop uses a console connection and does not need an IP address for that connection.

## Configuration practised

- Accessed switch and router command lines through a console connection.
- Configured device hostnames.
- Set enable secrets and console passwords.
- Required console password authentication using `login`.
- Enabled `service password-encryption`.
- Assigned the switch management IP and default gateway.
- Assigned and enabled the router LAN interface.
- Manually configured PC addresses, masks and gateways.
- Saved running configurations to startup configurations.

## Testing completed

- Successful ping tests between office PCs.
- Successful ping tests from all three PCs to the router.

These tests demonstrate connectivity within the local subnet. This lab does not include internet access or routing between different subnets.

## What I learned

- How to move between user EXEC, privileged EXEC and configuration modes.
- The difference between `exit` and `end`.
- The difference between a console password and an enable secret.
- How to choose a subnet with enough usable addresses.
- The difference between a device's own IP address and its default gateway.

## Lab credentials

Practice credentials only:

- Switch enable secret: `Office123`
- Router enable secret: `Router123`
- Console password on both devices: `Console123`

`service password-encryption` provides weak password obfuscation. This is a learning lab; production networks require additional security measures.

## Open the lab

Download `small-office-network.pkt` and open it in Cisco Packet Tracer.
