<div align="center">

# Active Directory Homelab with PowerShell Automation

**Windows Server 2019 + Windows 10 | Oracle VirtualBox**

A homelab simulating a small business network — Domain Controller setup, RAS/NAT routing, DHCP scoping, and user creation via PowerShell.

</div>

---

## Overview

This project walks through building an Active Directory environment from scratch, configuring core network services, and using PowerShell to automate the creation of 100x AD user accounts — simulating how a real enterprise network provisions and manages users at scale.

## Components

| Service | Role |
|---|---|
| **AD DS** | Domain Controller setup, custom Domain Admin account |
| **RAS (Remote Access Service)** | Routes internet access from the internal network through the DC (acts as gateway/NAT) |
| **DHCP Server** | Automatic IP address assignment with a defined scope |
| **PowerShell** | created 100x AD users based on the given parameters of the hash-table |

## Topology

```
        Internet
            │
      [NAT Adapter]
            │
 ┌──────────┴───────────┐
 │  Windows Server 2019   │
 │  (Domain Controller)   │
 │  - AD DS               │
 │  - RAS/NAT             │
 │  - DHCP                │
 └──────────┬───────────┘
      [Internal Network Adapter]
            │
 ┌──────────┴───────────┐
 │      Windows 10        │
 │  (Domain-joined client) │
 └────────────────────────┘
```

## What's Implemented

- [x] Domain Controller with dual NICs (NAT + internal network).
- [x] AD DS installation and domain promotion.
- [x] Custom Domain Admin account (promoted to Domain Admins group).
- [x] RAS/NAT configuration for internet access on the internal network.
- [x] DHCP scope configuration for automatic client IP addressing.
- [x] PowerShell script to create 100x AD users.
- [x] Windows 10 client joined to the domain, verified login with a generated account.

## Setup Steps

1. Created DC VM in VirtualBox with two network adapters (NAT + Internal Network).
2. Installed Windows Server 2019, installed AD DS role, promoted to Domain Controller.
3. Created a custom Domain Admin account.
4. Configured RAS/NAT to route internal network traffic to the internet.
5. Configured DHCP scope for client IP leasing.
7. Ran the script in PowerShell ISE to create 1000x AD users with ease.
8. Created Windows 10 client VM, joined it to the domain. 
9. Logged in as a generated user account to verify domain connectivity.

## Screenshots

*PLEASE HEAD TO MY LINKEDIN FOR MORE INFORMATION*

<div align="center">

</div>
