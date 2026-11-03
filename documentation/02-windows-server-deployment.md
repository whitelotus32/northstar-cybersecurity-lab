# 02 — Windows Server 2025 Deployment

## Objective
Install Windows Server 2025 as the guest operating system inside `NORTHSTAR-DC01`.

## Installation Process
1. Attached the Windows Server 2025 ISO to the VM's virtual optical drive.
2. Started the VM and booted into Windows Server Setup.
3. Selected English (United States) language and regional settings.
4. Selected **Install Windows Server**.
5. Selected **Windows Server 2025 Standard Evaluation (Desktop Experience)**.
6. Selected the VM's 60 GB virtual disk, shown as Disk 0 Unallocated Space.
7. Completed setup and allowed the VM to restart.
8. Confirmed the guest reached the Windows Server desktop and Server Manager.

## Validation
The following were visibly confirmed in the captured screenshots:
- VirtualBox showed `NORTHSTAR-DC01` running.
- Server Manager opened successfully.
- Local Server displayed Microsoft Windows Server 2025 Standard Evaluation.
- The guest was running inside the VirtualBox VM.

## Evidence
Store screenshots in `../screenshots/windows-server/`:
- Windows Server Setup language screen
- Setup option and edition selection
- Disk selection showing 60 GB unallocated virtual disk
- Successful boot / Server Manager dashboard
- Local Server properties

## Notes
This is a Windows Server Evaluation installation intended for lab learning. No Active Directory Domain Services role has been installed or promoted in this phase.
