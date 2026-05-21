# Windows Server 2025 Lab

## Overview
This project demonstrates the deployment and management of a Windows Server 2025 enterprise lab environment using VMware Workstation.  
The lab includes Active Directory Domain Services (AD DS), DNS, DHCP, Group Policy Management, file sharing, NTFS permissions, software deployment, and client management for Windows 10 and Windows 11 systems.

---

## Lab Topology
- 1 Domain Controller (Windows Server 2025)
- 1 Windows 10 Client
- 1 Windows 11 Client
- VMware NAT Network

---

## Technologies Used
- Windows Server 2025
- Windows 10
- Windows 11
- VMware Workstation
- Active Directory Domain Services (AD DS)
- DNS Server
- DHCP Server
- Group Policy Management (GPO)
- NTFS Permissions
- Shared Folder Management

---

## Implemented Features

### 1. Server and Client Installation
- Installed Windows Server 2025
- Installed Windows 10 and Windows 11 clients
- Configured VMware virtual machines

---

### 2. Network Configuration
- Configured static IP addresses
- Configured subnet mask, gateway and DNS
- Enabled ICMP (Ping) through Windows Firewall
- Verified connectivity between server and clients

---

### 3. Shared Folder Configuration
- Created shared folders between server and clients
- Configured Share Permissions and Security Permissions
- Created users for shared folder access
- Tested shared folder connectivity

---

### 4. Password Policy Configuration
- Disabled password complexity requirements
- Configured password policies using Group Policy
- Applied policy updates using:

```powershell
gpupdate /force
```

---

### 5. DNS Server Configuration
- Installed and configured DNS Server
- Created Forward Lookup Zone
- Created Reverse Lookup Zone
- Verified DNS name resolution using nslookup

---

### 6. DHCP Server Configuration
- Installed DHCP Server role
- Configured DHCP Scope
- Assigned IP addresses dynamically to clients

---

### 7. Active Directory Domain Services
- Installed Active Directory Domain Services (AD DS)
- Promoted server to Domain Controller
- Created domain environment

---

### 8. Domain Join
- Joined Windows 10 and Windows 11 clients to domain
- Verified domain authentication

---

### 9. OU, User and Group Management
- Created Organizational Units (OU)
- Created domain users and security groups
- Managed department structure:
  - IT
  - KeToan

---

### 10. Group Policy Management
Configured and linked multiple Group Policies:

#### Security Policies
- Password Policy
- Account Lockout Policy
- Disable USB Storage
- Disable Control Panel
- Disable Windows Settings
- Disable Command Prompt

#### Desktop Policies
- Desktop Wallpaper Deployment
- Prevent users from changing wallpaper

#### User Policies
- Allowed P-IT users to logon to Domain Controller
- Denied P-KeToan users from logging on to Domain Controller

#### Utility Policies
- Network Drive Mapping
- Software Deployment using GPO

---

### 11. Software Deployment
- Deployed 7-Zip automatically using Group Policy Software Installation

---

### 12. NTFS Permission Management
Configured department-based access control:

#### IT Department
- Only IT group can access IT data

#### KeToan Department
- Only KeToan group can access KeToan data

#### Shared Data
- Both departments can access shared data

#### Additional Restrictions
- Prevented users from deleting files belonging to other users

---

### 13. USB Restriction and Account Security
Configured security hardening policies:

#### Disable USB Storage
```txt
Computer Configuration
→ Policies
→ Administrative Templates
→ System
→ Removable Storage Access
```

#### Account Lockout Policy
```txt
Computer Configuration
→ Policies
→ Windows Settings
→ Security Settings
→ Account Policies
→ Account Lockout Policy
```

## Skills Demonstrated
- Windows Server Administration
- Active Directory Management
- DNS and DHCP Administration
- Group Policy Management
- NTFS Permission Management
- Enterprise Network Administration
- Windows Client Management
- Security Policy Configuration

---

## Author
Nguyen Huy Thao
