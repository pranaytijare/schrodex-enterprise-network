# Schrodex Technologies – Packet Tracer Project

This directory contains the Cisco Packet Tracer implementation of the Schrodex Technologies Enterprise Network.

## Project File

**`Schrodex_Network.pkt`**

The Packet Tracer file contains the complete simulated enterprise network, including the Head Office (Pune), Branch Office (Mumbai), and ISP connectivity.

## Network Architecture

The network consists of:
- **Head Office (HQ):** VLAN-based departmental segmentation.
- **Branch Office:** Separate departmental VLANs and centralized services.
- **ISP Network:** Simulated external network connectivity.
- **Centralized Servers:** DHCP, DNS and HTTP services.

## Technologies Implemented

- VLANs and Inter-VLAN Routing
- Router-on-a-Stick
- IEEE 802.1Q Trunking
- EtherChannel (LACP)
- Spanning Tree Protocol (STP)
- OSPF Dynamic Routing
- DHCP and DHCP Relay
- DNS and Internal Web Hosting
- NAT/PAT
- Access Control Lists (ACLs)
- Port Security with Sticky MAC
- SSH Remote Management

## Directory Structure

- **Configurations/** – Device configuration files.
- **Documentation/Screenshots/** – Network topology and configuration verification screenshots.
- **Schrodex_Network.pkt** – Complete Cisco Packet Tracer project.

## Verification

The network was tested for:
- Inter-VLAN connectivity
- Communication between HQ and Branch
- DHCP address allocation
- DNS name resolution
- Internal website accessibility
- External connectivity through NAT/PAT
- ACL-based traffic restrictions
- Port Security violation detection
- OSPF neighbor and routing verification

## How to Open

1. Download `Schrodex_Network.pkt`.
2. Open Cisco Packet Tracer.
3. Open the downloaded project file.
4. Explore the topology and device configurations.

**Project:** Schrodex Technologies – Connecting Possibilities.
