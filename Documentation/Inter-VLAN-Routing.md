# Inter-VLAN Routing

## Overview

Inter-VLAN routing allows devices in different VLANs to communicate with each other.

In this project, Inter-VLAN routing is implemented using the Layer 3 Cisco 3560 Multilayer Switch.

## Layer 3 Switch Configuration

IP routing is enabled on the multilayer switch:

```text
ip routing

VLAN 10 – HR
interface Vlan10
 ip address 192.168.10.1 255.255.255.0
 no shutdown

VLAN 20 – IT
interface Vlan20
 ip address 192.168.20.1 255.255.255.0
 no shutdown

Traffic Flow
HR PC → HR Switch → Trunk Link → Layer 3 Switch → Trunk Link → IT Switch → IT PC

Verification
show ip interface brief
show running-config
