# Proxmox Networking
## Goal

Create an isolated virtual network for enterprise services.

## Configuration

Created:

vmbr0
- Physical bridge
- Connected to eno1

vmbr2
- Internal bridge
- No physical interfaces attached

## Why?

vmbr2 acts as a virtual Layer 2 switch, allowing communication between pfSense, the Domain Controller and Windows client without exposing the lab directly to the home network and internet.

## Verification

- pfSense detects WAN
- pfSense detects LAN
- Windows Server reaches Internet
