# Windows Infrastructure Lab

A virtual Windows infrastructure project built using Proxmox VE, pfSense, Windows Server 2025 and Windows 11 Pro to gain hands-on experience with Active Directory, DNS, DHCP and Windows domain administration.

---

## Network Architecture

<p align="center">
  <img src="images/windows-lab-network-diagram.png" alt="Windows Infrastructure Lab Network Diagram" width="900">
</p>

The environment is hosted on Proxmox VE and isolated from the home network using a dedicated pfSense virtual firewall.

The pfSense WAN interface connects to the home LAN (10.27.27.0/24), while the LAN interface provides an isolated subnet (192.168.10.0/26). Windows Server acts as the Domain Controller, providing Active Directory, DNS and DHCP services, while a Windows 11 client receives its network configuration from the Windows DHCP server and authenticates against the domain.

---

## Overview

This project documents the design and deployment of an isolated Windows infrastructure lab hosted within Proxmox VE.

The aim was to build a realistic Windows environment from scratch while learning how Active Directory, DNS, DHCP and Windows networking work together in a domain environment.

Rather than simply installing the services, the focus was on understanding how each component integrates with the rest of the infrastructure and troubleshooting common configuration issues throughout the deployment.

---

## Technologies

- Proxmox VE
- pfSense
- Windows Server 2025
- Windows 11 Pro
- Active Directory Domain Services (AD DS)
- DNS
- DHCP
- SMB File Sharing

---

## Features Implemented

- Virtual networking using Proxmox bridges
- Isolated network using pfSense
- Double NAT architecture
- Active Directory Domain Services (AD DS)
- Windows DNS
- Windows DHCP Server
- Domain-joined Windows 11 client
- Organisational Units (Servers, Workstations, Users and Groups)
- User and Security Group management
- SMB File Shares
- Role-Based Access Control (RBAC)

---

## Network Addressing

| Device | Address |
|---------|---------|
| Home Router | 10.27.27.1 |
| pfSense WAN | 10.27.27.3 |
| pfSense LAN | 192.168.10.1/26 |
| Domain Controller (DC01) | 192.168.10.10 |
| Windows 11 Client | DHCP |

---

## Services

### pfSense

- Routing
- NAT
- Stateful Firewall
- Internet Gateway

### Domain Controller (DC01)

- Active Directory Domain Services
- DNS
- DHCP
- SMB File Sharing
- User & Group Management

### Windows 11 Pro

- Domain Joined
- Active Directory Authentication
- DHCP Client

---

## Challenges & Solutions

During the project I encountered and resolved several issues, including:

- DNS configuration preventing clients from joining the domain.
- Windows 11 Home edition lacking domain join support.
- SMB share permissions using Security Groups instead of assigning permissions directly to users.
- Designing an isolated virtual network using a dedicated Proxmox bridge (`vmbr2`) and pfSense.

---

## Lessons Learned

This project gave me practical experience with:

- Deploying a Windows domain from scratch.
- Understanding how Active Directory relies on DNS.
- Configuring Windows Server as a DHCP server.
- Implementing role-based access control using Security Groups.
- Designing an isolated network using Proxmox and pfSense.
- Troubleshooting domain joins, DNS and authentication issues.

---

## Project Walkthrough

A complete walkthrough of the project is available on YouTube.

The video covers:

- Network architecture
- Proxmox configuration
- pfSense configuration
- Windows Server deployment
- Active Directory
- DNS & DHCP
- Domain joining
- Organisational Units
- Security Groups
- SMB File Shares
- Demonstration of the completed environment

📺 YouTube:
(Link)

---

## Future Improvements

Planned additions include:

- Group Policy Objects (GPOs)
- Microsoft LAPS
- Windows Server Update Services (WSUS)
- Active Directory Certificate Services (AD CS)
- PowerShell automation
- Microsoft Deployment Toolkit (MDT)
