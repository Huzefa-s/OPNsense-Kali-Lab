# Project Aegis: Virtualized Security Stack

## Project Overview
This project involves building a multi-zone virtualized network environment to study enterprise-grade networking and security. By using VirtualBox on a Windows host, I have simulated a real-world architecture featuring a dedicated firewall, a management network, and an isolated security testing zone.

## Network Topology
The lab is structured into three distinct zones to simulate a "Defense-in-Depth" strategy:[cite: 1]
1. **WAN (Wide Area Network):** Bridged connection to the physical internet via the host Wi-Fi/Ethernet[cite: 1].
2. **LAN (Management):** A private Host-Only network (192.168.56.x) allowing secure web GUI access from the Windows host[cite: 1].
3. **Lab-NET (Internal):** A fully isolated virtual network (LabNet) for security testing, preventing any "blast radius" from reaching the host machine[cite: 1].

> [!TIP]
> **Network Diagram**
> ![Network Topology](images/topology-diagram.png)

---

## Technical Specifications

### Host Machine (Windows)
- **OS:** Windows 10/11[cite: 1]
- **Virtualization:** AMD-V / Intel VT-x Enabled[cite: 1]
- **Hypervisor:** VirtualBox 7.2.8 + Extension Pack[cite: 1]

### Virtual Firewall (OPNsense)
- **OS Base:** FreeBSD 14 (HardenedBSD)[cite: 1]
- **Resources:** 2 vCPUs, 2GB RAM[cite: 1]
- **Storage:** 20GB VDI (ZFS File System)[cite: 1]
- **Network Adapters:**
  - **Adapter 1:** Bridged (WAN)[cite: 1]
  - **Adapter 2:** Host-Only (LAN Management)[cite: 1]
  - **Adapter 3:** Internal Network (Isolated Lab)[cite: 1]

---

## Installation and Progress Log

### Phase 1: Infrastructure and Firewall Deployment
- [x] **Hypervisor Setup:** Installed VirtualBox 7.2.8 and configured Host-Only Virtual Switch[cite: 1].
- [x] **VM Provisioning:** Created the OPNsense shell with 2GB RAM and 3-interface mapping[cite: 1].
- [ ] **OS Installation:** Booting from ISO and installing OPNsense to virtual disk (ZFS).
- [ ] **Interface Assignment:** Mapping em0, em1, and em2 to WAN, LAN, and OPT1.

**Proof of Configuration:**
![VirtualBox Settings](images/vbox-settings.png)

---

## Security Roadmap
- **Phase 2:** Deployment of Kali Linux on the LabNet internal network[cite: 1].
- **Phase 3:** Implementing Suricata IDS/IPS to monitor and block malicious traffic patterns[cite: 1].
- **Phase 4:** Conducting Nmap Reconnaissance and Vulnerability Scanning against target VMs[cite: 1].

## Learning Outcomes
- **Network Segmentation:** Experience in creating isolated subnets to protect critical infrastructure[cite: 1].
- **NAT and Routing:** Understanding how a firewall handles traffic between public and private IPs[cite: 1].
- **Stateful Packet Inspection (SPI):** Learning how OPNsense tracks conversations to prevent unauthorized entry[cite: 1].

---
*Created by Huzefa Soni - May 12, 2026*

