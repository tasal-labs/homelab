# Hardware
The hardware components 
## Server

| Component | Specification |
|----------|---------------|
| Motherboard | ASUS Prime Z370-A II |
| CPU | Intel Core i7-8700K (6C/12T) |
| Memory | 64 GB DDR4 |
| Boot Drive | 256 GB NVMe (Proxmox VE + ISOs) |
| Container Storage | 480 GB SATA SSD (LXC rootfs) |
| VM Storage | 1 TB NVMe |
| Bulk Storage | 2 × 2 TB HDD (ZFS Mirror) |
| Case Fans | 2 × Noctua NF-P12 Redux 120mm |
| CPU Cooler | be quiet! Pure Rock Slim 2 |

### Storage Layout

| Device | Purpose |
|--------|---------|
| 256 GB NVMe | Proxmox VE, ISOs, templates |
| 512 GB SATA SSD | LXC root filesystems |
| 1 TB NVMe | Lab and development VMs |
| ZFS Mirror (2 × 2 TB HDD) | Persistent data, backups, Nextcloud, media |

## Router
| Component | Specification |
|----------|---------------|
| CPU | Celeron N6210 (2C) |
| Memory | 4 GB DDR4 |
| Boot Drive | 512 GB NVMe (I know) |
| Ethernet Ports | 2.5 GbE |

## Switch
- TP Link 8-Port Gigabit (to be upgraded)
