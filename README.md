 Company Branch Network Design

Project Overview
XYZ Company is a fast-growing organization based in Eastern Australia with over 2 million global customers.  
This project focuses on designing and implementing a **branch office network** near Bonalbo village, operating independently from the headquarters (HQ) network.

The goal is to design a secure, scalable, and well-structured Cisco network that meets business and technical requirements.

Project Requirements
- Use Cisco devices only
- One Router and one Switch
- Three departments:
  - Admin / IT
  - Finance / HR
  - Customer Service / Reception
- Each department must:
  - Be in a separate VLAN
  - Have wireless network access
- Hosts must obtain IPv4 addresses automatically (DHCP)
- Base network provided by ISP: 192.168.1.0
- Branch network operates separately from HQ

 Subnetting & IP Addressing

Given:
- Base Network: `192.168.1.0`
- Required Subnets: `3`
- Borrowed bits:
  
Subnet Mask:
- Binary: `11111111.11111111.11111111.11000000`
- Decimal: **255.255.255.192 (/26)**
- Block size: **64**

 Subnet 1 – Admin / IT
- Network ID: `192.168.1.0`
- Broadcast ID: `192.168.1.63`
- Valid Host Range: `192.168.1.1 – 192.168.1.62`

Subnet 2 – Finance / HR
- Network ID: `192.168.1.64`
- Broadcast ID: `192.168.1.127`
- Valid Host Range: `192.168.1.65 – 192.168.1.126`

Subnet 3 – Customer Service / Reception
- Network ID: `192.168.1.128`
- Broadcast ID: `192.168.1.191`
- Valid Host Range: `192.168.1.129 – 192.168.1.190`

 Devices & Technologies Used
- Cisco Router
- Cisco Switch
- Wireless Access Points
- VLANs
- DHCP
- IPv4 Addressing
- Inter-VLAN Routing
- Cisco Packet Tracer

 Network Design & Configuration
- Each department is assigned:
  - A unique VLAN
  - A dedicated subnet
  - A wireless access point
- Router-on-a-Stick configuration is used for **Inter-VLAN Routing**
- DHCP is configured on the router to dynamically assign:
  - IP address
  - Subnet mask
  - Default gateway
- Switch ports are configured as:
  - Access ports for end devices
  - Trunk link between switch and router

 Wireless Networking
- Each department has its own wireless network
- Wireless clients connect via Access Points
- IP addressing is automatically assigned using DHCP

