# Active_Directory_HomeLab
Active Directory homelab built with Windows Server 2019 and Windows 10 in VirtualBox. Covers AD DS installation, domain controller promotion, OU structure, user/group management, and Group Policy Objects (GPOs) for centralized endpoint control. Includes screenshots and step-by-step documentation of domain join and policy enforcement testing.


<div align="center">

# 🖥️ Active Directory Homelab

**Windows Server 2019 + Windows 10 + PowerShell | VirtualBox**

</div>

---

## 📋 Overview

This lab simulates a small business network using **Active Directory Domain Services (AD DS)** on Windows Server 2019, joined by a Windows 10 client, with additional network services configured to handle IP addressing, name resolution, and remote access.

## 🧩 Components

| Service | Role |
|---|---|
| **AD DS** | Centralized domain (`corp.local`), user/group management, OU structure |
| **Group Policy (GPO)** | Login scripts, drive mapping, security/audit policies |
| **DHCP Server** | Automatic IP addressing and scope management for domain clients |
| **RAS (Remote Access Service)** | Remote connectivity into the domain network |
| **DNS** | Internal hostname resolution for domain-joined machines |

## 🗺️ Topology

```
                 ┌─────────────────────────┐
                 │   Windows Server 2019    │
                 │  (Domain Controller)     │
                 │  - AD DS                 │
                 │  - DHCP Server           │
                 │  - RAS                   │
                 │  - DNS                   │
                 └───────────┬─────────────┘
                             │
                    Internal Network (LAN)
                             │
                 ┌───────────┴─────────────┐
                 │      Windows 10          │
                 │   (Domain-joined client)  │
                 └──────────────────────────┘
```

## ✅ What's Implemented

- [x] AD DS installation and domain controller promotion
- [x] OU structure with delegated administration
- [x] Fine-grained password policies
- [x] GPO-based login scripts and drive mapping
- [x] DHCP server — scope creation, lease management, reservations
- [x] RAS configuration for remote client access into the domain
- [x] Domain join and Group Policy verification on Windows 10 client

## 🛠️ Setup Steps

1. Deployed Windows Server 2019 in VirtualBox with static IP
2. Installed AD DS role → promoted server to domain controller
3. Created OUs and test users, configured password/audit policies
4. Installed and configured **DHCP role** — defined scope, exclusions, lease duration
5. Installed and configured **RAS** — enabled remote access into `corp.local`
6. Joined Windows 10 client to domain via DHCP-assigned IP
7. Verified GPO application and remote connectivity from client

## 📸 Screenshots

*PLEASE HEAD TO MY LINKEDIN FOR MORE INFORMATION*

---

<div align="center">

**Tech stack:** Windows Server 2019 · Windows 10 · VirtualBox · Active Directory · DHCP · RAS · Group Policy 

</div>
