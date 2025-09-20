# 🔐 HQ–Branch Secure Network Lab (Cisco ASA, OSPF, IPSec VPN)

This repository contains a **Cisco Packet Tracer** lab simulating a secure HQ–Branch enterprise environment:

- 🔹 **Cisco ASA firewalls** (HQ & Branch)
- 🔹 **OSPF area 0** dynamic routing
- 🔹 **HSRP** core redundancy
- 🔹 **Spanning Tree Protocol (Rapid-PVST)** for loop prevention
- 🔹 **DMZ** at HQ with public servers
- 🔹 **NAT & ACL** policies
- 🔹 **Site-to-Site IPSec VPN**
- 🔹 **Dedicated DHCP servers** (HQ & Branch)
- 🔹 **SSH restricted to Management VLANs**

---

## 📂 Repository structure
- `topology/` – Network diagram (.png) and Packet Tracer file (.pkt)
- `documentation/` – Detailed technical docs (IP plan, NAT, ACL, OSPF, VPN, tests)

---

## 🗺️ Topology
![HQ-Branch Topology](topology/hq-branch-topology.png)

---

## 🚀 Key Features
- HQ & Branch with **redundancy and security**
- **NAT/PAT** for Internet access
- **Static NAT + ACL** for DMZ servers
- **VPN IPSec IKEv1** between HQ & Branch
- **HSRP** on all VLANs (.1 virtual gateway)
- **SSH** allowed only from VLAN60 (Management)
- **Centralized DHCP** (HQ & Branch)
- **STP Enhancements**: Rapid-PVST, BPDU Guard, Root Guard

---

## 🔒 Security Features Implemented
- 📛 MOTD Banner for unauthorized access warning  
- 🔒 SSH as the only remote access method (Telnet disabled)  
- 🌐 ACLs for traffic filtering and access restriction  
- 🔄 DHCP Snooping on switches to prevent rogue DHCP attacks  
- 🎭 Dynamic ARP Inspection (DAI) to protect against ARP spoofing  
- 🛡 Port Security on access interfaces (MAC address limitation)  
- 🔀 Storm Control to protect against excessive broadcast/multicast traffic  
- 🔗 Spanning Tree Security: BPDU Guard & Root Guard  
- 🧱 NAT & PAT on ASA to hide internal networks and control traffic flows  
- 🔑 AAA (Authentication, Authorization, Accounting) with local users on ASA  

---

## ✅ Validation
- Ping HQ VLAN20 → Internet (8.8.8.8)
- VPN HQ ↔ Branch tests (`show crypto isakmp sa`, `show crypto ipsec sa`)
- Internet access from internal VLANs
- Public access to DMZ servers
- NAT/ACL validation (`show xlate`, `show access-list`)
- OSPF & HSRP neighbor checks
- DHCP relay tests on HQ & Branch VLANs
- STP loop-prevention and security checks

---

## 📜 License
MIT – free to use and adapt.
