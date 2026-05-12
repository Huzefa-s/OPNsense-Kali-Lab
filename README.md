# Home Lab Project: Virtualized Security Stack (OPNsense & Kali)

## 📌 Project Overview
This project involves building a multi-zone virtualized network environment to study enterprise-grade networking and security. By using a Type-2 hypervisor, I have simulated a real-world architecture featuring a dedicated firewall, a management network, and an isolated security testing zone.

## Network Topology
The lab is structured into three distinct zones:
1. **WAN (Wide Area Network):** Bridged connection to the physical internet.
2. **LAN (Management):** A Host-Only network allowing secure access from the host machine.
3. **Lab-NET (Internal):** A fully isolated virtual network for security testing.

[Image of your network diagram here]

## Tools & Technologies
- **Hypervisor:** VirtualBox 7.2.8
- **Firewall/Router:** OPNsense (FreeBSD-based)
- **Security Testing:** Kali Linux
- **Traffic Analysis:** Wireshark

## Setup & Configuration

### 1. Firewall Configuration (OPNsense)
- **Adapter 1:** Bridged (WAN)
- **Adapter 2:** Host-Only (LAN)
- **Adapter 3:** Internal Network 'LabNet' (OPT1)

### 2. Security Testing Zone
- Deployment of Kali Linux on the `LabNet` internal network.
- Configuration of Firewall Rules to prevent 'LabNet' from accessing the local home network.

## Security Exercises Conducted
- [ ] **Phase 1:** Initial firewall installation and rule configuration.
- [ ] **Phase 2:** Implementing an Intrusion Detection System (IDS) using Suricata.
- [ ] **Phase 3:** Vulnerability scanning with Nmap and Metasploit.

## 📈 Learning Outcomes
- Understanding of **NAT (Network Address Translation)** and DHCP.
- Experience with **Access Control Lists (ACLs)** and zone-based firewalling.
- Proficiency in virtual network interface management.

