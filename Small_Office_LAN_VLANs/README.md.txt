-- Small Office LAN with VLANs

Project Overview

Designed and configured a small office network using Cisco Packet Tracer. The project uses VLANs to separate departments, inter-VLAN routing to enable communication between permitted networks, DHCP for automatic IP assignment, and Access Control Lists (ACLs) to improve network security.

-- Network Topology

- 1 Cisco 2911 Router
- 3 Cisco 2960 Switches
- 6 End-user PCs
- One central switch connecting the router and two access switches

-- VLAN Configuration

| VLAN ID | Department | Network | Default Gateway |
|---|---|---|---|
| 10 | HR | 192.168.10.0/24 | 192.168.10.1 |
| 20 | Sales | 192.168.20.0/24 | 192.168.20.1 |
| 30 | IT | 192.168.30.0/24 | 192.168.30.1 |

-- Technologies and Concepts Used

- Cisco Packet Tracer
- VLAN Configuration
- Access and Trunk Ports
- IEEE 802.1Q Trunking
- Router-on-a-Stick
- Inter-VLAN Routing
- DHCP Configuration
- Extended Access Control Lists (ACLs)
- Network Connectivity Testing

-- Implementation

1. Created the physical network topology.
2. Configured VLAN 10, VLAN 20, and VLAN 30.
3. Configured trunk links between switches and the router.
4. Implemented inter-VLAN routing using router subinterfaces.
5. Configured DHCP pools for automatic IP assignment.
6. Applied an extended ACL to block traffic from Sales VLAN to IT VLAN while permitting other IP traffic.
7. Tested network connectivity between departments.

- Security Configuration

An extended ACL named `BLOCK_SALES_TO_IT` was configured on the Sales VLAN router subinterface.

- Blocks communication from Sales (192.168.20.0/24) to IT (192.168.30.0/24).
- Allows other IP traffic through the `permit ip any any` rule.

-- Testing and Results

| Test | Expected Result |
|---|---|
| DHCP assignment to all six PCs | Successful |
| HR to HR communication | Successful |
| Sales to Sales communication | Successful |
| HR to IT communication | Successful |
| Sales to IT communication | Blocked |

-- Project Files

- Small_Office_LAN_VLANs.pkt – Packet Tracer project file.
- configurations/ – Router and switch configurations.
- screenshots/ – Network configuration and connectivity test screenshots.

-- Learning Outcomes

- Understanding VLAN-based network segmentation.
- Configuring trunk links and inter-VLAN routing.
- Implementing DHCP services.
- Applying ACL rules for network access control.
- Troubleshooting and testing network connectivity.

## Conclusion

Successfully designed and configured a small office LAN with department-based VLAN segmentation, automatic IP addressing, inter-VLAN routing, and access control to restrict communication between selected departments.