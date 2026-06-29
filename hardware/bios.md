# BIOS Configuration
ASUS BIOS configurations made for power efficiency, not performance.
## CPU Power Saving

| Setting | Value |
|---------|-------|
| Intel SpeedStep (EIST) | Enabled |
| Intel Speed Shift | Enabled |
| CPU C-States | Enabled |
| C3 Report | Enabled |
| C6 Report | Enabled |
| C7 Report | Enabled |
| C8 Report | Enabled |
| Package C-State Limit | Auto |

## CPU

| Setting | Value |
|---------|-------|
| Hyper-Threading | Enabled |
| Intel Turbo Boost | Enabled |
| CPU Core Voltage | Offset Mode (optional undervolt) |

## Cooling

| Setting | Value |
|---------|-------|
| Q-Fan | Enabled |
| Fan Mode | PWM |
| Fan Curve | Custom |

## Boot

| Setting | Value |
|---------|-------|
| Boot Option #1 | Proxmox |
| Boot Option #2 | UEFI OS |

## Disabled

- PXE Boot
- Serial Port
- HD Audio
- RGB Controller

## Operating System

### Proxmox

| Setting | Value |
|---------|-------|
| CPU Governor | powersave |
| Scheduler | Default |
| CPU Scaling Driver | intel_pstate |
