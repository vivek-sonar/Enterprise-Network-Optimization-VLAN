# Trunk Configuration

## Overview

Trunk links are used to carry traffic from multiple VLANs between the access switches and the Layer 3 multilayer switch.

The network uses IEEE 802.1Q trunking.

## Trunk Links

| Device | Interface | Connected To | Mode |
|--------|-----------|--------------|------|
| HR Switch | Fa0/24 | L3 Switch | Trunk |
| L3 Switch | Fa0/1 | HR Switch | Trunk |
| L3 Switch | Fa0/2 | IT Switch | Trunk |
| IT Switch | Fa0/24 | L3 Switch | Trunk |

## Allowed VLANs

The active VLANs carried across the trunk links are:

- VLAN 10 – HR
- VLAN 20 – IT

## Verification

The following command was used to verify trunk operation:

```text
show interfaces trunk
