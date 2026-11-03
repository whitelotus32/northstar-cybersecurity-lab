# 03 — Initial Network Configuration

## Objective
Configure the virtual machine's network attachment for an isolated lab and record the guest's initial network configuration.

## VirtualBox Network
The VM's Adapter 1 was configured as:
- **Attached to:** Internal Network
- **Name:** `Northstar-internal`
- **Adapter type:** Intel PRO/1000 MT Desktop (82540EM)
- **Promiscuous mode:** Deny
- **Virtual cable connected:** Enabled

An Internal Network is intended for communication among VMs attached to the same named VirtualBox internal network. It is separate from the host's ordinary network connection.

## Guest Network Settings
The guest's IPv4 properties were set to obtain an IP address and DNS server automatically in the Windows interface dialog. Subsequent PowerShell output showed:

```powershell
Get-NetIPConfiguration
```

Captured output:

| Field | Value |
|---|---|
| Interface alias | Ethernet |
| Interface index | 6 |
| Adapter description | Intel(R) PRO/1000 MT Desktop Adapter |
| Network profile | Unidentified network |
| IPv4 address | `10.10.10.10` |
| IPv4 default gateway | None shown |
| DNS server | `10.10.10.10` |

The screenshot shows the IP and DNS values, but does not establish which service assigned them. This is a recorded observation, not a claim that DHCP or DNS is already functioning.

## Evidence
Place screenshots in `../screenshots/networking/`:
- VirtualBox Internal Network configuration
- Guest IPv4 properties dialog (if retained)
- PowerShell `Get-NetIPConfiguration` output

## Current State and Follow-up
The guest has a recorded IPv4 address of `10.10.10.10` and DNS value of `10.10.10.10`. Connectivity, name resolution, and the final static-IP configuration should be tested and documented before or during the Active Directory setup phase.

Do not assume the DNS service is operational merely because the DNS server address is displayed.
