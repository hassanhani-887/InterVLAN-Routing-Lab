# InterVLAN-Routing-Lab
This project demonstrates Inter-VLAN Routing using the Router-on-a-Stick method in Cisco Packet Tracer. A central router (CORP) is configured with subinterfaces to provide routing between VLANs, while Layer 2 switches handle VLAN segmentation. An ISP router is also connected via a serial WAN link to simulate external connectivity. 
## 🔹 Features Implemented
- **Router-on-a-Stick** on CORP Router (`g0/0.1`, `.10`, `.20`, `.30`)  
- **VLANs**:  
  - VLAN 1 → Native VLAN (192.168.1.0/24)  
  - VLAN 10 → Sales (192.168.10.0/24)  
  - VLAN 20 → Engineering (192.168.20.0/24)  
  - VLAN 30 → Marketing (192.168.30.0/24)  
- **Trunking** between CORP Router and switches (802.1Q encapsulation)  
- **Serial WAN link** between CORP Router and ISP Router (`172.31.7.4/30`)  
- **EIGRP 10** as the routing protocol for internal and external networks  
- **PCs assigned to different VLANs** and using the Router-on-a-Stick subinterfaces as their default gateways  

---

## 🔹 IP Addressing Scheme

| Device/Interface        | IP Address        | Subnet Mask       | Description       |
|--------------------------|------------------|------------------|------------------|
| CORP Router g0/0.1      | 192.168.1.1      | 255.255.255.0    | VLAN 1 (Native)  |
| CORP Router g0/0.10     | 192.168.10.1     | 255.255.255.0    | VLAN 10 (Sales)  |
| CORP Router g0/0.20     | 192.168.20.1     | 255.255.255.0    | VLAN 20 (Eng)    |
| CORP Router g0/0.30     | 192.168.30.1     | 255.255.255.0    | VLAN 30 (Mkt)    |
| CORP Router s0/1/0      | 192.31.7.6       | 255.255.255.252  | WAN to ISP       |
| ISP Router s0/1/0       | 192.31.7.5       | 255.255.255.252  | WAN to CORP      |
| ISP Router Lo0          | 198.133.219.1    | 255.255.255.0    | Internet Sim.    |
| L3Switch0 g0/1          | 172.31.1.6       | 255.255.255.252  | Link to CORP     |
| CORP Router g0/1        | 172.31.1.5       | 255.255.255.252  | Link to L3Switch |

