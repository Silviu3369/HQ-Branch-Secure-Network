# 🔐 HQ–Branch Secure Network Lab (Cisco ASA, OSPF, IPSec VPN)

This repository contains a **Cisco Packet Tracer** lab simulating a secure HQ–Branch enterprise environment:

- 🔹 **Cisco ASA firewalls** (HQ & Branch)
- 🔹 **OSPF area 0** dynamic routing
- 🔹 **HSRP** core redundancy
- 🔹 **DMZ** at HQ with public servers
- 🔹 **NAT & ACL** policies
- 🔹 **Site-to-Site IPSec VPN**
- 🔹 **Dedicated DHCP servers** (HQ & Branch)
- 🔹 **SSH restricted to Management VLANs**

---

## 📂 Repository structure
- `topology/` – Network diagram (.png) and Packet Tracer file (.pkt)
- `configs/` – Running-configs (ASA, Core switches)
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

---

## ✅ Validation
- Ping HQ VLAN20 → Internet (8.8.8.8)
- VPN HQ ↔ Branch tests (`show crypto isakmp/ipsec sa`)
- Internet access from internal VLANs
- Public access to DMZ servers
- NAT/ACL validation (`show xlate`, `show access-list`)
- OSPF & HSRP neighbor checks

---

## 📜 License
MIT – free to use and adapt.

