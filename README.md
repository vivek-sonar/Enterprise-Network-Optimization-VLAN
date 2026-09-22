# Enterprise Network Optimization using VLAN Segmentation and Inter-VLAN Routing

## Project Overview

This project demonstrates the design and implementation of a segmented enterprise network using Cisco Packet Tracer.

The network separates HR and IT departments using VLANs and enables communication between different VLANs using Layer 3 Inter-VLAN Routing.

## Network Topology

The topology consists of:

- Cisco Catalyst 2960 HR Access Switch
- Cisco Catalyst 3560 Multilayer Switch
- Cisco Catalyst 2960 IT Access Switch
- HR end devices
- IT end devices
- Trunk links between access switches and the Layer 3 switch

## Technologies Used

- Cisco Packet Tracer
- Cisco Catalyst 2960
- Cisco Catalyst 3560 Multilayer Switch
- VLAN
- 802.1Q Trunking
- Inter-VLAN Routing
- IPv4 Addressing
- Subnetting
- ICMP
- Network Troubleshooting

## VLAN Configuration

| VLAN ID | Department | Network | Default Gateway |
|---------|------------|---------|-----------------|
| 10 | HR | 192.168.10.0/24 | 192.168.10.1 |
| 20 | IT | 192.168.20.0/24 | 192.168.20.1 |

## IP Addressing

| Device | Department | IP Address | Subnet Mask | Gateway |
|--------|------------|------------|-------------|---------|
| HR-PC | HR | 192.168.10.2 | 255.255.255.0 | 192.168.10.1 |
| IT-PC | IT | 192.168.20.2 | 255.255.255.0 | 192.168.20.1 |

## Access and Trunk Configuration

HR and IT end devices are connected to access ports assigned to their respective VLANs.

The access switches are connected to the Layer 3 switch using 802.1Q trunk links.

### Trunk Links

- HR Switch Fa0/24 → L3 Switch Fa0/1
- IT Switch Fa0/24 → L3 Switch Fa0/2

## Inter-VLAN Routing

Inter-VLAN routing is implemented on the Cisco 3560 Multilayer Switch.

IP routing is enabled using:

```text
ip routing



VLAN 10 Gateway
interface Vlan10
 ip address 192.168.10.1 255.255.255.0
 no shutdown

VLAN 20 Gateway
interface Vlan20
 ip address 192.168.20.1 255.255.255.0
 no shutdown

Verification
The following commands were used to verify the network configuration:
show vlan brief
show interfaces trunk
show ip interface brief
show running-config

Connectivity Testing
End-to-end connectivity was tested between the HR and IT networks using ICMP.
Example:
ping 192.168.20.2
Successful replies confirmed communication between the different VLANs through the Layer 3 switch.

Troubleshooting
The project included verification of:

VLAN assignment
Access port configuration
Trunk status
VLAN SVI status
Default gateway configuration
Inter-VLAN routing
End-to-end connectivity

Project Structure

Enterprise-Network-Optimization-VLAN/
│
├── Packet-Tracer/
│   ├── Enterprise-Network-Optimization.pkt
│   └── README.md
│
├── Configuration/
│   ├── HR-Switch.txt
│   ├── L3-Switch.txt
│   └── IT-Switch.txt
│
├── Documentation/
│   ├── IP-Addressing-Table.md
│   ├── VLAN-Configuration.md
│   ├── Trunk-Configuration.md
│   ├── Inter-VLAN-Routing.md
│   └── Troubleshooting.md
│
└── Screenshots/
    ├── topology.png
    ├── vlan-configuration.png
    ├── trunk-configuration.png
    ├── inter-vlan-routing.png
    ├── connectivity-test.png
    └── README.md

Learning Outcomes
Through this project, I gained practical experience in:

Enterprise network design
VLAN segmentation
Access and trunk port configuration
Layer 3 switching
Inter-VLAN routing
IPv4 addressing and subnetting
Network troubleshooting
End-to-end connectivity verification

Project Files
The complete Cisco Packet Tracer project file and supporting documentation are available in this repository.

Author
Vivek Sonar
Network Engineer | CCNA Certified
