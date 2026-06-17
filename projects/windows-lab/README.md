# Virtualised Windows Lab
## Overview
This project documents the creation of an isolated Windows lab hosted within Proxmox. The goal is to build a fully virtualised network environment from scratch. 

This lab is separated from the primary home network using a dedicated pfSense VM, creating an environment where testing gone wrong doesn't impact any production services.
## Technologies
- Proxmox VE
- pfSense
- Windows Sserver
- Windows 11
- Active Directory
- DNS
- DHCP
## Objectives
- Configure virtual networking within Proxmox
- Create an isolated subnet using pfSense
- Implement Double NAT and routing concepts
- Deploy Windows Server and Windows 11 virtual machines
- Configure Active Directory Domain Services
- Deploy and manage DNS and DHCP services
- Design and implement subnetting and static routing
- Configure firewall rules and network access controls
## Planned Architecture
Home Network -> Lab pfSense (WAN) -> Lab pfSense (LAN) -> DC01, WIN11-01
## Documentation
Project upgrades, configuration notes, screenshots, and diagrams will be added throughout the build process.
