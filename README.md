# Enterprise-Home-Lab

## Summary

This project demonstrates the deployment, governance, and security auditing of a hybrid home lab environment. The lab integrates Active Directory Domain Services (AD DS) for centralized identity management, an EdgeRouter & Ubiquiti AP for network segmentation and remote access, and a Wazuh SIEM for continuous compliance auditing and syslog monitoring. 

## System Architecture

### Network Topology

<img width="600" height="450" alt="image" src="https://github.com/user-attachments/assets/bce179aa-c6cf-40da-9f08-19dbe44622fd" />

*Home lab network*

## Technology Stack & Capabilities

### Ubiquiti EdgeRouter PoE-5

- Routes network traffic to correct outbound address (Home router) in order to ensure internet connectivity
- Assigns network devices IP addresses via DHCP, with important network components mapped to static addresses
- Controls network traffic with firewall policies and rules, blocking unauthorized inbound connections and prohibiting guest network intervisibility
- Provides remote vpn access to the network by combining l2tp and IPsec

<img width="1400" height="650" alt="Screenshot 2026-09-10 001532" src="https://github.com/user-attachments/assets/8e56e46a-15e0-4808-ac34-22d349030667" />

*EdgeRouter Dashboard*

<img width="1400" height="650" alt="Screenshot 2026-09-10 001814" src="https://github.com/user-attachments/assets/6195d83d-9b4b-4735-8f5c-91906e5351e5" />

*EdgeRouter inbound firewall rules*



### Windows Server 2022

- Deploys Active Directory Domain Services to manage the lab domain
- Utilizes Group Policy Objects, Organizational Units, and Security Groups to enforce Zero Trust principles
- Manages the provisioning, deprovisioning, and account management of domain users


### Wazuh SIEM

- Provides lab visibility by aggregating logs from all parts of the network onto a central platform
- Houses details related to suspicious network activity, endpoint vulnerabilities, device hardening, and continuous compliance to multiple frameworks


## Key Takeaways

- User and Computer Management within Active Direcctory
- Group Policy Management
- Role-based Access Control
- Networking Principles/Troubleshooting
- SIEM Log Analysis


