![Windows Server](https://img.shields.io/badge/Windows_Server-2022-0078D6?style=for-the-badge&logo=windows)
![Active Directory](https://img.shields.io/badge/Active_Directory-AD_DS-0052CC?style=for-the-badge)
![PowerShell](https://img.shields.io/badge/PowerShell-5.1-5391FE?style=for-the-badge&logo=powershell)
![VMware](https://img.shields.io/badge/VMware-Workstation-607078?style=for-the-badge&logo=vmware)
# Windows Server 2022 Active Directory Home Lab

A hands-on Windows Server 2022 Home Lab that demonstrates the deployment, configuration, and administration of an enterprise Active Directory environment.

This project covers the installation and management of Active Directory Domain Services (AD DS), DNS, DHCP, File Server, Group Policy, Roaming Profiles, and PowerShell automation using VMware Workstation.

---

## Lab Topology

![Lab Topology](images/Digram.PNG)

---

## Technologies Used

- Windows Server 2022
- Windows 11
- VMware Workstation
- Active Directory Domain Services (AD DS)
- DNS
- DHCP
- SMB File Sharing
- NTFS Permissions
- Access-Based Enumeration (ABE)
- Group Policy (GPO)
- Group Policy Preferences (Drive Mapping)
- Roaming Profiles
- PowerShell

---

## Lab Modules

| Module | Description |
|---------|-------------|
| **01. Environment Setup** | Create the virtual machine, install AD DS, promote the server to a Domain Controller, and create Organizational Units (OUs), users, and security groups. |
| **02. DNS Configuration** | Configure DNS zones, create DNS records, and verify name resolution. |
| **03. DHCP Configuration** | Configure DHCP scopes, exclusions, scope options, and validate automatic IP assignment. |
| **04. File Server** | Configure storage, shared folders, NTFS permissions, Access-Based Enumeration (ABE), and deploy mapped network drives using Group Policy Preferences (GPP). |
| **05. Roaming Profiles** | Configure roaming profiles and verify user profile synchronization across domain computers. |

---

## Documentation

- 📄 [01 - Environment Setup](01-Environment-Setup.md)
- 📄 [02 - DNS Configuration](02-DNS-Configuration.md)
- 📄 [03 - DHCP Configuration](03-DHCP-Configuration.md)
- 📄 [04 - File Server](04-File-Server.md)
- 📄 [05 - Roaming Profiles](05-Roaming-Profiles.md)

---

## Skills Demonstrated

- Active Directory Administration
- Windows Server Administration
- DNS Configuration
- DHCP Deployment
- Organizational Unit (OU) Design
- User & Group Management
- PowerShell Automation
- File Server Administration
- NTFS Permissions
- SMB File Sharing
- Access-Based Enumeration (ABE)
- Group Policy Management
- Group Policy Preferences (Drive Mapping)
- Roaming Profiles
- Windows Client Domain Join

---

## Project Structure

```text
WIN-SRV-Homelab
│
├── README.md
├── 01-Environment-Setup.md
├── 02-DNS-Configuration.md
├── 03-DHCP-Configuration.md
├── 04-File-Server.md
├── 05-Roaming-Profiles.md
└── images/
```

---

## Features

- Enterprise Active Directory Deployment
- DNS & DHCP Services
- Department-Based Organizational Units
- User & Security Group Management
- PowerShell Automation
- Secure SMB File Sharing
- NTFS Permissions
- Access-Based Enumeration (ABE)
- Drive Mapping using Group Policy Preferences (GPP)
- Roaming User Profiles
- Windows 11 Domain Integration

---

## Author

**Mazen Medhat**

- IT Student
- System Administration & Networking Enthusiast
- Cybersecurity Enthusiast

If you found this project useful, feel free to ⭐ star the repository.
