# Troubleshooting

## Issue 1: VLAN Connectivity Problem

### Checks Performed

```text
show vlan brief

Verified that VLAN 10 (HR) and VLAN 20 (IT) were active and the correct access ports were assigned.

Issue 2: Trunk Link Verification
Checks Performed
show interfaces trunk
Verified that the required switch interfaces were operating as 802.1Q trunk links and carrying the required VLANs.

Issue 3: Inter-VLAN Communication
Checks Performed
show ip interface brief

Verified that the VLAN 10 and VLAN 20 SVIs were up/up with the correct gateway IP addresses.
The Layer 3 switch was also configured with:
ip routing

Issue 4: End-to-End Connectivity
Connectivity was tested between the HR and IT end devices using ICMP ping.
The configured default gateways were verified on both end devices.
