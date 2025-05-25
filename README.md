# 🏥 Enterprise Healthcare Network Infrastructure Design

This project presents a **secure, scalable, and robust enterprise-level network** designed for a modern healthcare diagnostics provider. Built in **Cisco Packet Tracer**, the network supports multiple floors and departments, ensuring high availability, data integrity, and seamless communication across the organization.

---

## 🧠 Project Objective

As the appointed **Network Security Engineer**, your role is to design and implement a reliable and secure ICT infrastructure that supports:

- Core healthcare operations (labs, doctors, internal systems)
- Business departments (HR, Finance, Procurement)
- Technical teams (IT Support, Developers, Cybersecurity, Cloud Engineering)
- External access (guests, auditors, cloud service users)
- Scalable architecture that supports doubling user capacity by 2025

---

## 🏗️ Network Design Overview

The enterprise operates across **three corporate floors** with departments like labs, reception, consultancy, internal audit, IT, and corporate operations. The network was designed based on **Cisco’s hierarchical model**, ensuring modularity, redundancy, and scalability.

> ⚠️ **Security Disclaimer**: The network employs multiple defense mechanisms (firewall zones, VLANs, ACLs) to protect sensitive health data and ensure regulatory compliance. Each user group is segmented and monitored.

---

## 🧩 Components & Technologies Used

### 🌐 Connectivity & Routing

- **ISP Provider**: Airtel (simulated)
- **Edge Security**: Cisco ASA 5500-X Firewall
- **WAN Router**: Cisco 2811 (also configured for VoIP gateway)
- **Routing Protocol**: OSPF for dynamic routing
- **Static Routes**: Configured for firewall and DMZ access

### 🖧 Switching & VLANs

- **Core & Access Switches**:
  - 2× Cisco Catalyst 3850 (48-Port)
  - 8× Catalyst 2960 (48-Port)
  - 2× Catalyst 2960 (24-Port)
- **VLANs**:
  - VLAN 10 → LAN users  
  - VLAN 50 → WLAN users  
  - VLAN 99 → VoIP devices

- **EtherChannel**: Implemented using **LACP**
- **STP Enhancements**: PortFast and BPDU Guard enabled

### 🔐 Network Segmentation & IP Schema

| Segment | VLAN | IP Range           |
|---------|------|--------------------|
| LAN     | 10   | `192.168.0.0/20`   |
| WLAN    | 50   | `10.10.0.0/16`     |
| VOIP    | 99   | `172.16.0.0/20`    |
| DMZ     | N/A  | `10.20.20.0/26`    |
| Public  | N/A  | `197.200.100.0/24` |

---

## 🧾 Core Infrastructure & Services

### ☁️ Cloud & Remote Access

- **AWS Cloud Integration**:
  - External access for clients and remote teams
  - Cloud developers consume multiple cloud services
- **Security Zoning** on Cisco ASA Firewall for cloud, LAN, DMZ, and guests

---

## 📞 Voice & Wireless Infrastructure

- **Cisco Voice Gateway**: For enterprise VoIP support
- **IP Phones**: Configured in all departments
- **Dial Plan**: Format (3...)
- **Cisco WLC** + **10 LAPs**: Centralized wireless control
- **Wireless Access Points**: Installed floor-wide for guests and employees

---

## 🔐 Security & Access Control

- **ACLs**:
  - SSH access restricted to Security Engineer PC only
  - ACLs applied to VTY lines
- **Firewall Policies**:
  - Static routes and security levels
  - Inspection policies for inter-zone traffic
- **Inter-VLAN Routing**: Configured on Multilayer Switch
- **DHCP**: Managed by AD Server (excluding VoIP phones)

---

## ⚙️ Configuration Highlights

- **Device Naming & Banners**
- **Password Encryption & Console Access Security**
- **Domain Lookup Disabled**
- **HSRP**: Configured for failover and load balancing on routers
- **Subnetting**: Optimized for each segment and department

---

## 🧪 Final Testing & Validation

- ✔️ Successful inter-VLAN communication
- ✔️ Internet access for all authorized users
- ✔️ Guest and WLAN zones isolated
- ✔️ Server redundancy and DHCP lease allocation validated

---

## 📁 Project Files

📁 project-root/

┣ 📄 README.md ← Project overview and documentation

┣ 📁 HOSPITAL.pkt ← Cisco Packet Tracer file (network implementation)


---

## ✅ Outcome

This project demonstrates how to implement a full-scale, real-life enterprise network with **virtualization**, **voice**, **cloud integration**, **wireless infrastructure**, and **security-first architecture** using Cisco technologies. Designed to scale with organizational growth, the network ensures **confidentiality**, **integrity**, and **availability** of critical systems and data.

---

## 📌 Notes

- The project simulates a **realistic healthcare ICT environment**.
- All data and configurations are **fictional and intended for educational purposes only**.
