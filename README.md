# Enterprise Multi-Switch VLAN Network

> A Cisco Packet Tracer project demonstrating Enterprise Network Design using VLANs, IEEE 802.1Q Trunking, and Router-on-a-Stick.

---

##  Project Overview

This project demonstrates the design and implementation of a small enterprise network using Cisco Packet Tracer. The network follows a hierarchical architecture with one Core Switch, two Access Switches, and one Cisco Router.

Multiple departments are separated using VLANs, and communication between VLANs is achieved through **Router-on-a-Stick** using IEEE 802.1Q trunking.

This project helped strengthen my understanding of Layer 2 Switching, Layer 3 Routing, VLAN segmentation, and Enterprise Network Design.

---



## Project Demonstration



(https://drive.google.com/file/d/1KecvE-i-n2_8ectHUyp61adYlVpIrK9t/view)
# Network Topology

```
                     Cisco 2911 Router (R1)
                             |
                     802.1Q Trunk Link
                             |
                    Core Switch (SW1-Core)
                      /               \
              Trunk Link           Trunk Link
                  |                    |
          SW2-Access              SW3-Access
          |         |             |         |
      HR-PC01  SALES-PC01     IT-PC01  ADMIN-PC01
```

---

#  Objectives

- Build an enterprise-style network
- Configure VLANs
- Configure Access Ports
- Configure Trunk Links
- Configure Router-on-a-Stick
- Configure Static IP Addressing
- Enable Inter-VLAN Routing
- Verify Connectivity

---

#  Devices Used

| Device | Model | Quantity |
|---------|--------|----------|
| Router | Cisco 2911 | 1 |
| Core Switch | Cisco 2960 | 1 |
| Access Switch | Cisco 2960 | 2 |
| PC | PC-PT | 4 |

---

#  VLAN Configuration

| VLAN | Name | Network |
|------|------|----------------|
|10|HR|192.168.10.0/24|
|20|SALES|192.168.20.0/24|
|30|IT|192.168.30.0/24|
|40|ADMIN|192.168.40.0/24|
|50|SERVER|192.168.50.0/24 *(Reserved)*|
|60|WIFI|192.168.60.0/24 *(Reserved)*|
|99|MGMT|192.168.99.0/24 *(Reserved)*|

---

#  IP Addressing

| Device | IP Address | Default Gateway |
|---------|------------|----------------|
|HR-PC01|192.168.10.10|192.168.10.1|
|SALES-PC01|192.168.20.10|192.168.20.1|
|IT-PC01|192.168.30.10|192.168.30.1|
|ADMIN-PC01|192.168.40.10|192.168.40.1|

---

#  Technologies Implemented

- Cisco Packet Tracer
- Cisco IOS CLI
- VLAN Configuration
- IEEE 802.1Q Trunking
- Access Ports
- Router-on-a-Stick
- Static IP Addressing
- Inter-VLAN Routing
- Enterprise Network Design
- Network Verification

---

#  Repository Structure

```
Enterprise-MultiSwitch-VLAN/
│
├── README.md
├── LAB-GUIDE.md
├── Enterprise-MultiSwitch-VLAN.pkt
├── router-config.txt
├── SW1-Core.txt
├── SW2-Access.txt
├── SW3-Access.txt
├── topology.png
│
└── screenshots/
      ├── vlan-brief.png
      ├── trunk.png
      ├── router-interfaces.png
      ├── ping-test.png
      └── video-thumbnail.png
```

---

#  Verification

The following verification steps were successfully completed:

- ✔ VLAN Creation
- ✔ VLAN Assignment
- ✔ Access Port Configuration
- ✔ Trunk Configuration
- ✔ Router Subinterface Configuration
- ✔ Static IP Configuration
- ✔ Successful Inter-VLAN Communication
- ✔ End-to-End Connectivity

---

#  Skills Demonstrated

- Enterprise Network Design
- Cisco IOS CLI
- Layer 2 Switching
- Layer 3 Routing
- VLAN Segmentation
- Router-on-a-Stick
- Enterprise Troubleshooting
- Network Documentation

---

#  Future Enhancements

This project will be extended by implementing:

- DHCP
- DNS
- Web Server
- FTP Server
- SSH
- ACLs
- NAT/PAT
- Wireless Network
- OSPF Routing



GitHub:
https://github.com/divakar-45
