# Enterprise-Home-Lab

## Summary

This project demonstrates the deployment, governance, and security auditing of a hybrid home lab environment. The lab integrates Active Directory Domain Services (AD DS) for centralized identity management, an EdgeRouter & Ubiquiti AP for network segmentation and remote access, and a Wazuh SIEM for continuous compliance auditing and syslog monitoring. 

## System Architecture

### Network Topology

<img width="600" height="450" alt="image" src="https://github.com/user-attachments/assets/dd534845-f11c-4ee7-b62b-dbf1bc6661c5" />


*Home lab network*

## Technology Stack & Capabilities

### Ubiquiti EdgeRouter PoE-5

- Routes network traffic to correct outbound address (Home default gateway) in order to ensure internet connectivity
- Assigns network devices IP addresses via DHCP, with different DHCP servers for Admin and Guest subnets, and important network components mapped to static addresses
- Controls network traffic with firewall policies and rules, blocking unauthorized connections from unsecure ports (21, 23, 80, etc.) and prohibiting guest network intervisibility
- Provides remote vpn access to the network by combining l2tp and IPsec

<img width="1400" height="650" alt="Screenshot 2026-09-10 001532" src="https://github.com/user-attachments/assets/8e56e46a-15e0-4808-ac34-22d349030667" />

*EdgeRouter Dashboard*

<img width="1400" height="650" alt="Screenshot 2026-09-10 001814" src="https://github.com/user-attachments/assets/6195d83d-9b4b-4735-8f5c-91906e5351e5" />

*EdgeRouter inbound firewall rules*



### Windows Server 2022

- Deploys Active Directory Domain Services to manage the lab domain
- Utilizes Group Policy Objects, Organizational Units, and Security Groups to enforce password policies, disable insecure authentication protocols, and ensure appropriate user access rights
- Manages the provisioning, deprovisioning, and account management of domain users

<img width="1200" height="650" alt="Screenshot 2026-09-10 000629" src="https://github.com/user-attachments/assets/6e600c5e-4db1-4044-94ac-3064074e8e14" />

*Active Directory Group Policy Objects*

### Wazuh SIEM

- Provides lab visibility by aggregating logs from all parts of the network onto a central platform
- Deploys agents to endpoints to provide data related to suspicious network activity, endpoint vulnerabilities, device hardening reccomendations, and continuous compliance to multiple frameworks

<img width="1500" height="750" alt="Screenshot 2026-09-10 000831" src="https://github.com/user-attachments/assets/ec8f8fa4-fa3f-4db0-86a1-c665df0e7129" />

*Wazuh Active Directory agent dashboard*

<img width="1200" height="725" alt="Screenshot 2026-09-10 001049" src="https://github.com/user-attachments/assets/fc3c44f9-3db6-4419-a4c1-aa6afd5be816" />

*Wazuh parsed logs*




## Key Takeaways

- User and Computer Management within Active Directory
- Group Policy Management
- Role-based Access Control
- Networking Principles/Troubleshooting
- SIEM Log Analysis


