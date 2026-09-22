# IP Addressing Table

## VLAN Networks

| VLAN | Department | Network | Subnet Mask | Default Gateway |
|------|------------|---------|-------------|-----------------|
| 10 | HR | 192.168.10.0/24 | 255.255.255.0 | 192.168.10.1 |
| 20 | IT | 192.168.20.0/24 | 255.255.255.0 | 192.168.20.1 |

## End Devices

| Device | Department | IP Address | Subnet Mask | Default Gateway |
|--------|------------|------------|-------------|-----------------|
| HR-PC | HR | 192.168.10.2 | 255.255.255.0 | 192.168.10.1 |
| IT-PC | IT | 192.168.20.2 | 255.255.255.0 | 192.168.20.1 |

## Layer 3 Switch SVIs

| Interface | VLAN | IP Address |
|-----------|------|------------|
| Vlan10 | 10 | 192.168.10.1 |
| Vlan20 | 20 | 192.168.20.1 |
