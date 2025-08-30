# InterVLAN-Routing-Lab
This project demonstrates Inter-VLAN Routing using the Router-on-a-Stick method in Cisco Packet Tracer and SVI method. 
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


