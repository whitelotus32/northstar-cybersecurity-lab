# 01 — VirtualBox Setup

## Objective
Provision a virtual machine to host the first Northstar Windows Server system without installing the guest operating system directly on the physical workstation.

## Virtual Machine Configuration

| Setting | Value |
|---|---|
| VM name | `NORTHSTAR-DC01` |
| Guest OS type | Windows Server 2022 (64-bit) selected in VirtualBox's VM profile |
| Memory | 4,096 MB |
| Processors | 2 |
| Virtual disk | `NORTHSTAR-DC01.vdi` |
| Disk capacity | 60.00 GB |
| Disk format | VDI |
| Disk allocation | Dynamically allocated (Pre-allocate Full Size unchecked) |
| Network | Internal Network |
| Internal network name | `Northstar-internal` |
| Adapter | Intel PRO/1000 MT Desktop (82540EM) |
| Virtual cable | Connected |

**Profile note:** The VM wizard's operating-system profile displayed Windows Server 2022 (64-bit), while the mounted installation media and installed guest are Windows Server 2025. The profile is a VirtualBox configuration label; the guest OS was installed from the Windows Server 2025 ISO.

## Installation Media
The Windows Server 2025 ISO was attached to the VM's virtual optical drive (SATA Port 1). The VM booted from the ISO and launched Windows Server Setup.

## Evidence
Place screenshots in `../screenshots/virtualbox/`:
- VM creation and 60 GB virtual disk
- VirtualBox VM summary
- Storage settings showing attached Windows Server ISO
- Network settings showing Internal Network and `Northstar-internal`

## Result
The VM was created and configured with virtual hardware, a virtual disk, installation media, and an isolated internal network. Windows Server installation is documented in the next section.
