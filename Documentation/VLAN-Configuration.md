# VLAN Configuration

## VLAN Overview

The network is segmented into separate VLANs to logically isolate departmental traffic and reduce the broadcast domain.

| VLAN ID | VLAN Name | Department |
|---------|-----------|------------|
| 10 | HR | Human Resources |
| 20 | IT | Information Technology |

## HR VLAN

- VLAN ID: 10
- VLAN Name: HR
- Network: 192.168.10.0/24
- Gateway: 192.168.10.1
- Access ports: Fa0/1, Fa0/2 on HR Switch

## IT VLAN

- VLAN ID: 20
- VLAN Name: IT
- Network: 192.168.20.0/24
- Gateway: 192.168.20.1
- Access ports: Fa0/1, Fa0/2 on IT Switch

## VLAN Verification

The following command was used to verify VLAN creation and port assignment:

```text
show vlan brief
