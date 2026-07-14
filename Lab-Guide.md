# Enterprise Multi-Switch VLAN Network

## Lab Objective

Design and configure an enterprise-style network using Cisco Packet Tracer. The network demonstrates VLAN implementation, IEEE 802.1Q trunking, and Inter-VLAN Routing using Router-on-a-Stick.

---

# Network Topology

```
                     Cisco 2911 Router
                             |
                     802.1Q Trunk
                             |
                     SW1-Core (2960)
                      /             \
                SW2-Access      SW3-Access
                 |       |       |       |
              HR-PC   SALES   IT-PC   ADMIN-PC
```

---

# Devices Used

- Cisco 2911 Router
- Cisco 2960 Core Switch
- Cisco 2960 Access Switch (2)
- Four PCs

---

# Phase 1 – Basic Device Configuration

Configured on all routers and switches:

- Hostname
- Enable Secret
- Console Password
- MOTD Banner
- Password Encryption
- Saved Running Configuration

Verification:

```
show running-config
```

---

# Phase 2 – VLAN Configuration

Created VLANs:

| VLAN | Name |
|------|------|
|10|HR|
|20|SALES|
|30|IT|
|40|ADMIN|
|50|SERVER|
|60|WIFI|
|99|MGMT|

Verification:

```
show vlan brief
```

---

# Phase 3 – Access Port Configuration

Configured Access Ports:

| Switch | Interface | VLAN |
|---------|-----------|------|
|SW2|Fa0/1|10|
|SW2|Fa0/2|20|
|SW3|Fa0/1|30|
|SW3|Fa0/2|40|

Verification:

```
show vlan brief
```

---

# Phase 4 – Trunk Configuration

Configured Trunk Links:

- SW1-Core ↔ SW2-Access
- SW1-Core ↔ SW3-Access
- SW1-Core ↔ Router

Verification:

```
show interfaces trunk
```

---

# Phase 5 – Router-on-a-Stick

Configured Router Subinterfaces:

| Interface | VLAN |
|-----------|------|
|G0/0.10|HR|
|G0/0.20|SALES|
|G0/0.30|IT|
|G0/0.40|ADMIN|
|G0/0.50|SERVER|
|G0/0.60|WIFI|
|G0/0.99|MGMT|

Verification:

```
show ip interface brief
```

---

# Phase 6 – Static IP Configuration

Configured:

| Device | IP Address | Gateway |
|---------|------------|----------|
|HR-PC01|192.168.10.10|192.168.10.1|
|SALES-PC01|192.168.20.10|192.168.20.1|
|IT-PC01|192.168.30.10|192.168.30.1|
|ADMIN-PC01|192.168.40.10|192.168.40.1|

---

# Phase 7 – Connectivity Testing

Verified communication using:

```
ping
```

Tests Performed:

- HR → SALES
- HR → IT
- HR → ADMIN
- SALES → HR
- IT → ADMIN

Result:

✔ Successful Inter-VLAN Routing

---

# Learning Outcomes

This project provided practical experience with:

- Enterprise Network Design
- VLAN Segmentation
- Broadcast Domains
- Access Ports
- IEEE 802.1Q Trunking
- Router-on-a-Stick
- Static IP Addressing
- Default Gateway
- Inter-VLAN Routing
- Cisco IOS CLI
- Network Verification
- Troubleshooting

---

# Conclusion

This project demonstrates how enterprise networks logically separate departments using VLANs while enabling secure communication through Router-on-a-Stick.

The project serves as a strong foundation for future enterprise networking labs involving DHCP, DNS, ACLs, NAT/PAT, Wireless LAN, SSH, and dynamic routing protocols.
