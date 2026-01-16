# Inter-Network Communication in Cisco Packet Tracer

## Overview
This simole beginner project demonstrates IPv4 communication between two different networks
using a Cisco 2911 router and multiple switches in Cisco Packet Tracer.

- Routing via GigabitEthernet interfaces

<img width="1353" height="424" alt="image" src="https://github.com/user-attachments/assets/97595528-7756-40cc-afc4-f6a626b19bb0" />

## Network Status
All router interfaces are operational and configured correctly:

- GigabitEthernet0/0 → 192.168.10.1 (UP/UP)
- GigabitEthernet0/1 → 192.168.11.1 (UP/UP)

All hosts use correct IP addressing, subnet masks, and default gateways.

## Issue Observed During Testing
During ICMP testing, one host intermittently failed to reach remote hosts
after reopening the simulation, while other hosts continued to work normally.

## Analysis
Because routing, addressing, and switching were verified to be correct,
the issue was isolated to host-level behavior rather than network design.

This behavior is attributed to ARP cache persistence and NIC state artifacts
within Cisco Packet Tracer, which may occur after saving and reopening projects.

## Resolution
The issue was resolved by:
- Clearing the ARP cache on the affected host
- Resetting the host’s network interface
- Replacing the host with a newly added PC

After applying these steps, ICMP connectivity worked as expected.

## Key Learning
This project highlights the importance of structured troubleshooting and the
difference between real networking behavior and simulation environments.

> Note: This issue was observed in the simulation environment only and does not
> reflect behavior of real Cisco networking devices.

