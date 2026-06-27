# Windows Infrastructure Lab

A virtual Windows infrastructure project built using Proxmox VE, pfSense, Windows Server 2025 and Windows 11 Pro to gain hands-on experience with Active Directory, DNS, DHCP and Windows domain administration.

---

## Overview

This project documents the design and deployment of an isolated Windows infrastructure lab hosted within Proxmox VE.

The aim was to build a realistic Windows environment from scratch while learning how the core infrastructure components work together. The lab is isolated from the home network using a dedicated pfSense firewall, allowing services such as Active Directory, DNS and DHCP to be deployed without affecting production devices.

The completed environment includes a Windows Server Domain Controller, a domain-joined Windows 11 client and role-based access control using Active Directory Security Groups and SMB file shares.

---

## Technologies

* Proxmox VE
* pfSense
* Windows Server 2025
* Windows 11 Pro
* Active Directory Domain Services (AD DS)
* DNS
* DHCP
* SMB File Sharing

---

## Objectives

* Build an isolated Windows infrastructure within Proxmox
* Configure virtual networking using pfSense
* Deploy Windows Server as a Domain Controller
* Configure Active Directory Domain Services (AD DS)
* Implement DNS and DHCP
* Join Windows 11 clients to the domain
* Configure Organisational Units (OUs), users and security groups
* Implement role-based access control (RBAC) using SMB file shares
* Document the deployment and architecture

---

## Network Architecture

The lab is hosted on Proxmox VE and isolated from the home network using a dedicated pfSense virtual firewall.

The pfSense WAN interface connects to the home LAN (10.27.27.0/24), while the LAN interface provides an isolated subnet (192.168.10.0/26).

Windows Server acts as the Domain Controller, providing Active Directory, DNS and DHCP services, while the Windows 11 client receives its network configuration from the Windows DHCP server and authenticates against the domain.

<p align="center">
  <img src="images/windows-lab-network-diagram.png" alt="Windows Infrastructure Lab Network Diagram" width="900">
</p>

---

## Network Addressing

| Device                   | Address         |
| ------------------------ | --------------- |
| Home Router              | 10.27.27.1      |
| pfSense WAN              | 10.27.27.3      |
| pfSense LAN              | 192.168.10.1/26 |
| Domain Controller (DC01) | 192.168.10.10   |
| Windows 11 Client        | DHCP            |

---

## Services

### pfSense

* Routing
* NAT
* Firewall
* Internet Gateway

### Domain Controller (DC01)

* Active Directory Domain Services
* DNS
* DHCP
* SMB File Sharing
* User & Group Management

### Windows 11 Client

* Domain Joined
* DHCP Client
* Active Directory Authentication

---

## Features Implemented

* Virtual networking using Proxmox bridges
* Network isolation using pfSense
* Double NAT architecture
* Active Directory Domain Services (AD DS)
* Windows DNS
* Windows DHCP Server
* Domain-joined Windows client
* Organisational Units (Servers, Workstations, Users and Groups)
* User and Security Group management
* SMB file shares
* Role-Based Access Control (RBAC)

---

## Lessons Learned

Throughout this project I gained practical experience with:

* Building a Windows domain from scratch.
* Understanding how Active Directory relies on integrated DNS.
* Configuring Windows Server as a DHCP server.
* Designing an isolated virtual network using Proxmox and pfSense.
* Implementing role-based access control using Active Directory Security Groups.
* Troubleshooting domain joins, DNS configuration and SMB permissions.
* Documenting and presenting technical infrastructure through architecture diagrams and video walkthroughs.

---

## Project Walkthrough

A complete walkthrough of the project is available on YouTube, covering:

* Project overview
* Network architecture
* Proxmox configuration
* pfSense configuration
* Windows Server deployment
* Active Directory
* DNS & DHCP
* Domain joining
* Organisational Units
* Security Groups
* SMB file shares
* Demonstration of the completed environment

📺 YouTube:
[YouTube Link]

---

## Future Improvements

Some features I'd like to explore next include:

* Group Policy Objects (GPOs)
* Windows Server Update Services (WSUS)
* Certificate Services (AD CS)
* Multi-Domain Controller replication
* Microsoft Deployment Toolkit (MDT)
* Microsoft LAPS
* Network monitoring and logging

```
```
