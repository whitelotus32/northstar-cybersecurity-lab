[README.md](https://github.com/user-attachments/files/34298277/README.md)
# Northstar Cybersecurity Lab

A hands-on cybersecurity and Windows infrastructure lab built with Oracle VirtualBox and Windows Server 2025. Northstar is being developed incrementally, with configuration steps, validation, screenshots, and lessons learned documented as the lab evolves.

## Current Status

**Phase 1 — Virtualization and Windows Server deployment: complete**

| Component | Current configuration |
|---|---|
| Hypervisor | Oracle VirtualBox |
| Virtual machine | `NORTHSTAR-DC01` |
| Guest OS | Windows Server 2025 Standard Evaluation |
| Virtual memory | 4,096 MB (4 GB) |
| Virtual CPUs | 2 |
| Virtual disk | 60 GB VDI, dynamically allocated |
| Network attachment | Internal Network |
| Internal network name | `Northstar-internal` |
| Guest IPv4 | `10.10.10.10` |
| DNS server shown in initial configuration | `10.10.10.10` |

## Project Objectives
- Build a safe, isolated environment for learning Windows infrastructure and cybersecurity.
- Practice server deployment, network configuration, PowerShell, and troubleshooting.
- Progress toward Active Directory, identity and access management, and security administration exercises.
- Maintain reproducible documentation and evidence for a technical portfolio.

## Repository Structure
```text
northstar/
├── README.md
├── documentation/
│   ├── 01-virtualization-setup.md
│   ├── 02-windows-server-deployment.md
│   └── 03-initial-network-configuration.md
└── screenshots/
    ├── virtualbox/
    ├── windows-server/
    └── networking/
```

## Current Milestone
Windows Server 2025 has been installed and booted successfully inside the `NORTHSTAR-DC01` VirtualBox VM. The VM is configured with an Internal Network named `Northstar-internal`. Initial PowerShell output showed IPv4 address `10.10.10.10` and DNS server `10.10.10.10`.

**Active Directory has not yet been installed or configured.** That work will be documented in a later phase after this baseline is committed and reviewed.

## Documentation
- [VirtualBox setup](documentation/01-virtualization-setup.md)
- [Windows Server deployment](documentation/02-windows-server-deployment.md)
- [Initial network configuration](documentation/03-initial-network-configuration.md)

## Safety and Scope
Northstar is a learning lab. Keep lab systems isolated from production networks and use only systems, accounts, and data you are authorized to administer. The current Internal Network configuration is intended to keep this VM's lab traffic separate from the host's ordinary network.

## Evidence
Screenshots are stored in the `screenshots/` folders and referenced from the relevant documentation. Review images for personal information, license keys, credentials, or other sensitive details before publishing.
