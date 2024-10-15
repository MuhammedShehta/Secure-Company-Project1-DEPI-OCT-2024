# Design and Implementation of a Secure Company Network System
## 1. Introduction
This document outlines the design and implementation of a secure network system for Cytonn Innovation Ltd, a forward-thinking company specializing in providing innovative cloud solutions globally. The project focuses on creating a robust network infrastructure to support various departments within the organization while ensuring the security of sensitive data and resources.

![Secure Company Network Packet Tracer](https://github.com/user-attachments/assets/c084538a-3330-46da-b629-8aa0aebc4081)

## 2. Case Study and Requirements
Cytonn Innovation Ltd has a workforce of 600 staff and is preparing to move to a new building with three floors. The building will host various departments, including Sales and Marketing, Human Resources, Finance, ICT, and a Server Room. The ICT department includes Software Developers, Cloud Engineers, Cybersecurity Engineers, Network Engineers, System Administrators, IT Support Specialists, Business Analysts, and Project Managers.
Prior to the move, a new network service needs to be designed and implemented. The company aims to ensure robust security against internal and external threats by implementing a multi-layered security approach, including a firewall with distinct security zones: outside, inside, and DMZ.

## 3.Network Devices Description

![Screenshot 2024-10-10 040320](https://github.com/user-attachments/assets/110af8ba-297f-4c6e-b13f-a1d8d94509d8)


### Cisco ASA Firewall
#### Cisco Adaptive Security Appliance (ASA) is a security device that combines firewall, VPN, and other network security services in a single platform. It provides advanced threat defense, intrusion prevention, and protects the network from attacks by monitoring, controlling, and filtering traffic. Key features include:

#### ![image](https://github.com/user-attachments/assets/57273964-e90d-4b1a-829e-cc97baf0b8aa)

    - Stateful packet inspection
    - Virtual Private Network (VPN) support
    - Intrusion Prevention System (IPS)
    - Web filtering and malware defense
    - Secure access control and user authentication
    
### Cisco Catalyst Switches (3850 & 2960)
#### Cisco Catalyst switches are enterprise-class switches designed for secure and scalable network access.

#### ![image](https://github.com/user-attachments/assets/d44c5f75-cced-4962-b9fa-5bc18ceec707) ![image](https://github.com/user-attachments/assets/544a5ce9-8ef1-43f0-a6a4-2563e3f18126)

    - Cisco Catalyst 3850: Stackable access switches with integrated wireless controller. Supports advanced features 
    like high-performance Layer 3 routing and quality of service (QoS). Supports up to 480 Gbps stacking bandwidth.
    - Cisco Catalyst 2960: Layer 2 access switch for small to medium networks. Supports basic features like VLANs, 
    STP (Spanning Tree Protocol), and port security. Energy-efficient and simple to deploy for cost-effective LANs.
    
### DHCP Server
#### A Dynamic Host Configuration Protocol (DHCP) server automatically assigns IP addresses and other network configuration parameters (like subnet masks and default gateways) to client devices. This reduces the need for manual IP configuration and ensures that devices in a network can communicate efficiently. Key functions include:
    - Automatic IP assignment
    - IP address lease management
    - DNS and gateway configuration
    
### DNS Server
#### A Domain Name System (DNS) server resolves human-readable domain names (like www.example.com) into machine-readable IP addresses. This process is essential for web browsing and network operations, as it allows devices to locate and communicate with others over the internet or internal networks. Key functions include:
    - Domain name resolution
    - IP address mapping
    - Caching previous lookups for faster responses
    
### FTP Server
#### A File Transfer Protocol (FTP) server enables the transfer of files between a client and a server over a network. FTP is often used for uploading and downloading large files in business environments. Key features include:
    - File sharing and storage
    - Authentication and user access control
    - Data encryption via secure FTP (SFTP)
    
### WEB Server
####  A web server hosts and delivers websites or web-based applications to users over the internet or intranet. It processes incoming HTTP/HTTPS requests, interprets them, and sends the appropriate content (web pages, images, scripts). Commonly used web servers include Apache, Nginx, and Microsoft IIS. Key functions include:
    - Serving static and dynamic content
    - SSL/TLS encryption for secure connections
    - Load balancing for high-traffic sites
    
### Email Server
#### An email server handles the sending, receiving, and storage of emails. It allows users to communicate using email protocols such as SMTP (Simple Mail Transfer Protocol) for outgoing mail, and IMAP/POP3 for incoming mail. Popular email servers include Microsoft Exchange and Postfix. Key functions include:
    - Email routing and delivery
    - Mailbox storage and management
    - Security features like spam filtering and virus scanning
    
### VoIP Gateway
####  A Voice over IP (VoIP) gateway converts voice signals between the public switched telephone network (PSTN) and an IP network. It allows voice calls to be transmitted over IP networks, making it a critical component for enterprises that want to integrate traditional telephony with modern IP-based communication systems. Key features include:
    - Call routing between IP and analog phones
    - Codec conversion and compression for voice data
    - Fax and SMS integration
### Wireless LAN Controller (WLC)
#### A Wireless LAN Controller (WLC) manages and controls wireless access points in a network, ensuring secure and efficient wireless communication. It centralizes wireless network management, enabling simplified configuration, monitoring, and troubleshooting. Key functions include:
    - Wireless network security and access control
    - Centralized configuration for multiple access points
    - Load balancing and roaming support
    
### NAS Storage Server
####  A Network-Attached Storage (NAS) server provides file storage and sharing over a network. It allows users to store and retrieve data from a centralized location, making it ideal for backups, file sharing, and media streaming.  NAS servers often come with built-in redundancy and data protection features like RAID. Key functions include:
    - Centralized file storage and sharing
    - User access control and permissions
    - Data redundancy and backups
    
## 4. IP Addressing
#### The designated IP address ranges for various network components are as follows:
Management Network: 192.168.10.0/24
WLAN: 10.20.0.0/16
LAN: 172.16.0.0/16
VoIP: 172.30.0.0/16
DMZ: 10.11.11.0/27
####  Public Addresses:
•	   - SEACOM: 105.100.50.0/30
•	   - Safaricom: 197.200.100.0/30

## 5.Technologies Implemented

![Screenshot 2024-10-10 040008](https://github.com/user-attachments/assets/9926cc73-50cb-4617-a3fa-271fa4920214)

### Design Tool: Cisco Packet Tracer
Cisco Packet Tracer was used for network design and simulation before the actual deployment. It allowed for a virtual environment to test configurations, create network topologies, and simulate device behavior to ensure functionality before real-world implementation.

### Hierarchical Design
A hierarchical network design model was implemented, consisting of three layers: Core, 
    Distribution, and Access. This model improves scalability, redundancy, and network manageability. Redundancy 
    is achieved through multiple links between layers to ensure high availability.
### ISPs: Connectivity to an Airtel ISP Router
The network was connected to an Airtel ISP router to provide external 
    internet access. This ensures reliable and high-speed connectivity for the organization's internal network.
### Wireless LAN Controller (WLC)

#### ![image](https://github.com/user-attachments/assets/bac76ff5-2a1f-4a27-9878-d7ed027789f4)

Each department was equipped with a Wireless Access Point (WAP) managed by a Wireless LAN Controller (WLC). This provided WiFi access for users and allowed centralized management and monitoring of wireless networks.

### VoIP: Deployment of IP Phones

#### ![image](https://github.com/user-attachments/assets/cf102348-f197-4fdc-8eaa-7232ab686c44)

#### VoIP (Voice over IP) technology was implemented using IP phones to enable efficient voice communication over the IP network. This solution integrates voice services with the existing data network, reducing costs and simplifying management.

### VLAN: Maintained VLANs with Specific IDs
#### VLANs (Virtual Local Area Networks) were set up with unique IDs to segregate network traffic. 
    VLANs were created for:
    - Management
    - LAN (General user traffic)
    - WLAN (Wireless network traffic)
    - VoIP (Dedicated for IP phone communication)
    - Blackhole (For isolating unwanted or suspicious traffic)
    
### EtherChannel: LACP for Link Aggregation
Link Aggregation Control Protocol (LACP) was used to implement EtherChannel, allowing multiple physical links between switches to be combined into a single logical link. This increases bandwidth and provides redundancy in case of link failure.

### Spanning Tree Protocol (STP)
STP was configured to prevent network loops and ensure a loop-free topology. Features like PortFast were enabled on access ports to expedite the connection of end devices, and BPDUguard was applied to prevent the introduction of rogue switches.

### Subnetting: IP Address Allocation
Subnetting was used to logically divide the network into smaller sub-networks. This allows for efficient IP address allocation, improved network management, and enhances security by isolating different departments or services.

### Basic Device Settings
Basic configurations were applied to all network devices, including setting hostnames, enabling secure passwords for access, and configuring necessary logging and monitoring settings to enhance security and manageability.

### Inter-VLAN Routing
Inter-VLAN routing was enabled on multilayer switches to allow communication between different VLANs. 
    This setup ensures that departments can communicate with each other while maintaining network segmentation for security purposes.
### Core Switch: IP Assignment for Multilayer Switches

![image](https://github.com/user-attachments/assets/71f7b8ee-adf5-4831-b6f0-de3681b11c8f)


Multilayer switches in the core layer were assigned IP addresses to handle both Layer 2 switching and Layer 3 routing. These switches manage both local traffic and inter-VLAN routing.

### DHCP Server: Dynamic IP Allocation
A DHCP server was configured to dynamically assign IP addresses to end devices in the network. This ensures efficient IP management and reduces the chances of IP conflicts.

### HSRP: High Availability Router Protocol
The Hot Standby Router Protocol (HSRP) was implemented to ensure high availability for routing services. In case the primary router fails, the standby router takes over, minimizing downtime.

### Static Addressing: Server Room Devices
Static IP addresses were assigned to critical devices in the server room, such as servers, storage devices, and printers. This ensures stable and predictable access to these resources.

### Routing Protocol: OSPF for Route Advertisement
OSPF (Open Shortest Path First) was selected as the routing protocol to efficiently advertise routes within the internal network. OSPF is a scalable and reliable protocol for dynamic routing, providing fast convergence and optimal path selection.

### Standard ACL for SSH
A Standard Access Control List (ACL) was created to allow secure remote access using SSH.This restricts remote access to specific IP addresses, enhancing security.
### Cisco ASA Firewall

![image](https://github.com/user-attachments/assets/334cc721-2366-457e-92e2-b03d27610498)

The Cisco ASA firewall was configured to secure the network by controlling incoming and outgoing traffic based on predefined security rules. It provides protection against external threats and ensures internal network segmentation.

### Final Testing: Communication Verification
After configuring the entire network, thorough testing was conducted to ensure proper communication between all devices and verify that all configurations were applied correctly. This testing included end-to-end connectivity checks, security audits, and performance evaluations.

### 6. Conclusion

# ![image](https://github.com/user-attachments/assets/e6027e05-1bfa-4a99-866c-bf84d2db921f)


The design and implementation of a secure network system for Cytonn Innovation Ltd is critical to ensuring operational efficiency and safeguarding sensitive data. By employing a structured approach with robust security measures, the new network will support the company's growth and adaptability in the digital landscape.


