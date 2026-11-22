# Schrodex Technologies
### Connecting Possibilities.

**Enterprise Network Design, Implementation and Security Using Cisco Packet Tracer**

## 1. Project Overview

Schrodex Technologies is a simulated IT services company with its Head Office in Pune and Branch Office in Mumbai.

This project demonstrates the design, implementation and verification of a multi-site enterprise network using Cisco Packet Tracer. The two sites are connected through a WAN link, with a simulated ISP network for external connectivity testing.

The project focuses on practical routing, switching, network services and infrastructure security.

## 2. Network Architecture

The simulated network contains three main sections:

- **Head Office – Pune:** Departmental VLANs, centralized servers and network management.
- **Branch Office – Mumbai:** Separate departmental VLANs connected to the Head Office over a WAN link.
- **ISP Network:** Simulated external connectivity for NAT/PAT testing.

The topology includes Cisco routers, Layer 2 switches, client PCs and centralized DHCP, DNS and HTTP servers.

## 3. IP Addressing and VLAN Design

### Head Office – Pune

| VLAN | Department | Network | Default Gateway |
|---|---|---|---|
| 10 | Sales | 192.168.10.0/24 | 192.168.10.1 |
| 20 | HR | 192.168.20.0/24 | 192.168.20.1 |
| 30 | IT | 192.168.30.0/24 | 192.168.30.1 |
| 50 | Servers | 192.168.50.0/24 | 192.168.50.1 |
| 99 | Management | 192.168.99.0/24 | 192.168.99.1 |
| 999 | Native / Unused | — | — |

### Branch Office – Mumbai

| VLAN | Department | Network | Default Gateway |
|---|---|---|---|
| 110 | Sales | 192.168.110.0/24 | 192.168.110.1 |
| 120 | HR | 192.168.120.0/24 | 192.168.120.1 |
| 130 | IT | 192.168.130.0/24 | 192.168.130.1 |
| 99 | Management | 192.168.199.0/24 | 192.168.199.1 |
| 999 | Native / Unused | — | — |

### WAN and ISP Addressing

| Connection | Network | Interface Addresses |
|---|---|---|
| HQ–Branch WAN | 10.0.0.0/30 | HQ: 10.0.0.1, Branch: 10.0.0.2 |
| HQ–ISP | 203.0.113.0/30 | HQ: 203.0.113.1, ISP: 203.0.113.2 |
| ISP External LAN | 198.51.100.0/24 | ISP gateway: 198.51.100.1 |

## 4. Technologies Implemented

| Technology | Implementation |
|---|---|
| VLANs | Departmental network segmentation |
| Inter-VLAN Routing | Router-on-a-Stick |
| 802.1Q | VLAN trunking |
| EtherChannel | LACP link aggregation |
| STP | Root bridge selection and Layer 2 loop prevention |
| OSPF | Dynamic routing between sites |
| DHCP | Centralized IP address allocation |
| DHCP Relay | Forwarding DHCP requests from remote VLANs |
| DNS | Internal hostname resolution |
| HTTP | Internal intranet web hosting |
| NAT/PAT | Translation for external connectivity |
| ACLs | Restrictions on HR-to-IT communication |
| Port Security | Sticky MAC learning and violation shutdown |
| SSH | Secure remote device management |

## 5. Network Services

Centralized services are hosted at the Head Office:

| Service | IP Address | Purpose |
|---|---|---|
| DHCP Server | 192.168.50.10 | Dynamic IP address allocation |
| DNS Server | 192.168.50.11 | Internal name resolution |
| HTTP Server | 192.168.50.12 | Internal intranet website |

**Internal website:** `intranet.schrodex.local`

DHCP relay is configured so Branch Office clients can obtain addresses from the centralized DHCP server.

## 6. Network Security

The following security controls are implemented:

- **Access Control Lists:** Restrict HR-to-IT communication at both sites.
- **Port Security:** Sticky MAC learning, a maximum of one secure MAC address per access port, and shutdown on violation.
- **SSH:** Secure remote management of network devices.
- **VLAN Segmentation:** Separates departmental traffic.
- **STP:** Helps prevent Layer 2 switching loops.

## 7. Testing and Verification

The following functions were tested in the Packet Tracer simulation:

- Inter-VLAN communication.
- Connectivity between the Head Office and Branch Office.
- DHCP address allocation across all six departmental networks.
- Internal DNS name resolution.
- Internal website accessibility from client PCs.
- External server connectivity through NAT/PAT.
- ACL-based HR-to-IT traffic restrictions.
- Port Security violation detection.
- OSPF neighbor formation and route exchange.
- EtherChannel and trunk operation.

## 8. Repository Structure

```text
schrodex-enterprise-network/
├── README.md
└── Packet-Tracer/
    ├── README.md
    ├── Schrodex_Network.pkt
    ├── Configurations/
    └── Documentation/
        └── Screenshots/
```

## 9. How to Run the Project

1. Clone or download this repository.
2. Install Cisco Packet Tracer.
3. Open `Packet-Tracer/Schrodex_Network.pkt`.
4. Explore the topology and device configurations.
5. Refer to the configuration files and screenshots for implementation and verification details.

---

**Project:** Schrodex Technologies  
**Tagline:** Connecting Possibilities.
