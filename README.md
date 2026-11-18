# CCNA Campus Network Design and Implementation

## Project Overview
Designed and implemented a multi-layer campus network using Cisco Packet Tracer. The project demonstrates practical networking concepts, network segmentation, dynamic routing, network security, and simulated external connectivity.

## Technologies Used
- Cisco Packet Tracer
- VLANs
- DHCP
- Inter-VLAN Routing
- OSPF (Area 0)
- EtherChannel (LACP)
- NAT/PAT
- Extended Access Control Lists (ACLs)
- Switch Port Security

## Network Architecture
The network follows a hierarchical design consisting of:
- Core Layer
- Distribution Layer
- Access Layer
- Routers and a simulated ISP

## VLAN and IP Addressing

| VLAN | Department | Network | Default Gateway |
| 10 | HR | 192.168.10.0/24 | 192.168.10.1 |
| 20 | Management | 192.168.20.0/24 | 192.168.20.1 |
| 30 | Sales | 192.168.30.0/24 | 192.168.30.1 |
| 40 | IT | 192.168.40.0/24 | 192.168.40.1 |
| 50 | Finance | 192.168.50.0/24 | 192.168.50.1 |
| 60 | Guest | 192.168.60.0/24 | 192.168.60.1 |

## Key Implementations

### 1. VLAN and DHCP
Created separate VLANs for different departments and configured DHCP to assign IP addresses automatically to client devices. VLAN 50 uses no DHCP pool.

### 2. Inter-VLAN Routing
Configured Layer 3 routing to enable communication between authorized departmental networks.

### 3. OSPF Dynamic Routing
Configured OSPF in Area 0 to exchange routing information between network devices.

### 4. EtherChannel
Implemented LACP EtherChannel to combine multiple physical links into logical port-channel links.

### 5. NAT/PAT
Configured NAT overload to provide simulated external network connectivity through the ISP router.

### 6. Guest Network Security
Configured an Extended ACL named GUEST-BLOCK to restrict Guest VLAN access to internal departmental networks while permitting other traffic.

### 7. Switch Port Security
Configured Sticky MAC address learning, maximum one secure MAC address per access port, and shutdown violation mode to prevent unauthorized device access.

## Testing and Verification
- Verified DHCP address assignment.
- Tested inter-VLAN connectivity.
- Verified OSPF neighbor relationships and routing tables.
- Tested EtherChannel operation.
- Verified NAT translations.
- Tested Guest VLAN access restrictions.
- Tested internet connectivity to the simulated ISP endpoint.
- Tested Port Security by connecting an unauthorized PC and verifying that the switch port was disabled.

## Project File
The Cisco Packet Tracer project file (`.pkt`) is included in this repository.

## Learning Outcomes
Gained practical experience in campus network design, routing and switching, network segmentation, troubleshooting, and network security.

## Tools
Cisco Packet Tracer
