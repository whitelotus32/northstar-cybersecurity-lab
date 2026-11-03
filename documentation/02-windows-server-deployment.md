# 02 — Windows Server 2025 Deployment

## Objective
Deploy Windows Server 2025 Standard Evaluation inside the NORTHSTAR-DC01 virtual machine using Oracle VirtualBox.

## Installation
Windows Server 2025 was installed within the NORTHSTAR-DC01 virtual machine.

The installation process included:

Selecting the Windows Server 2025 Standard Evaluation image.

Selecting the Desktop Experience installation option.

Installing the operating system to the allocated 60 GB virtual disk.

Completing installation and booting into Windows Server.

## Server Configuration

After installation, Server Manager was used to review the initial server configuration.

The server was identified as:

Hostname: NORTHSTAR-DC01

Operating System: Windows Server 2025 Standard Evaluation

Workgroup: WORKGROUP

Remote Management: Enabled

Remote Desktop: Disabled

## Initial Network Configuration

PowerShell was used to inspect the network configuration:

Get-NetIPConfiguration

The output showed:

Property

Value

Interface

Ethernet

Adapter

Intel PRO/1000 MT Desktop Adapter

IPv4 Address

10.10.10.10

DNS Server

10.10.10.10

Default Gateway

Not configured

## Validation
The following initial deployment checks were completed:

Windows Server successfully booted.

Server Manager was accessible.

The virtual network adapter was recognized.

PowerShell returned network configuration information.

## Next Steps

Verify VirtualBox network mode.

Validate IP addressing and DNS configuration.

Install Active Directory Domain Services.

Promote NORTHSTAR-DC01 to a domain controller.

## Evidence

The following screenshots document the Windows Server deployment process:

- [Windows Server installation](../screenshots/windows-server/)
- [VirtualBox configuration](../screenshots/virtualbox/)
- [Network configuration](../screenshots/networking/)

Evidence includes operating system selection, virtual disk allocation, successful installation, Server Manager, and initial network configuration.


## Notes
This is a Windows Server Evaluation installation intended for lab learning. No Active Directory Domain Services role has been installed or promoted in this phase.
