# Virtualised Windows Enterprise Lab

## Overview

This project documents the design, deployment and administration of a virtualised Windows enterprise environment hosted within Proxmox VE.

The objective was to build a small enterprise network from scratch using Windows Server, Active Directory and pfSense, providing a safe environment to develop practical infrastructure and systems administration skills without impacting the production home network.

The lab includes virtual networking, routing, Active Directory Domain Services (AD DS), DNS, DHCP, domain-joined Windows clients and role-based access control using security groups and SMB file shares.

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

* Create an isolated enterprise network within Proxmox
* Configure virtual networking and routing using pfSense
* Deploy Windows Server as a Domain Controller
* Configure Active Directory Domain Services
* Implement DNS and DHCP services
* Join Windows 11 clients to the domain
* Configure users, organisational units and security groups
* Implement role-based access control using SMB shares
* Document the deployment process and architecture

---

## Network Architecture

The home network remains isolated from the lab through a dedicated pfSense virtual firewall implementing double NAT.

Addressing:

Home Network

10.27.27.0/24

Lab Network

192.168.10.0/26

| Device                   | Address         |
| ------------------------ | --------------- |
| Home Router              | 10.27.27.1      |
| pfSense WAN              | 10.27.27.3      |
| pfSense LAN              | 192.168.10.1/26 |
| Domain Controller (DC01) | 192.168.10.10   |
| Windows 11 Client        | DHCP            |

---

## Active Directory

Domain:

win.lab

Implemented:

* Active Directory Domain Services
* Integrated DNS
* DHCP
* Organisational Units
* Domain Users
* Security Groups
* SMB File Shares

Organisational Units:

* Servers
* Workstations
* Users
* Groups

---

## Identity & Access Management

Created multiple domain users and implemented role-based access control through Active Directory Security Groups.

Permissions are assigned using the model:

User → Security Group → Shared Resource

rather than assigning permissions directly to user accounts.

---

## Services

The Domain Controller provides:

* Active Directory
* DNS
* DHCP
* SMB File Sharing

pfSense provides:

* Routing
* NAT
* Firewall
* Internet Connectivity

---

## Skills Demonstrated

* Windows Server Administration
* Active Directory
* DNS
* DHCP
* Group-based Access Control
* Windows Domain Management
* Network Segmentation
* pfSense
* Virtualisation using Proxmox
* Enterprise Network Design
* Troubleshooting
* Documentation

---

## Walkthrough

A complete walkthrough of the deployment, configuration process and network architecture has been recorded and is available on YouTube.

The video explains:

* Network design
* pfSense configuration
* Active Directory deployment
* DNS & DHCP configuration
* Domain joining
* Security groups
* File sharing
* Overall architecture
