# Proxmox VE Installation

## Objective
Install Proxmox VE on a dedicated mini PC to establish a virtualization host for hands-on IT and cybersecurity projects.

## Environment
- **Hardware:** HP EliteDesk Mini 600 G5
- **Memory:** 32 GB RAM
- **Storage:** 1 TB
- **Hypervisor:** Proxmox VE 9.2.1 (recorded installation version)
- **Network:** Ethernet connection to the home network

## Installation Summary
1. Downloaded the Proxmox VE installer image from the official Proxmox website.
2. Created a bootable USB installer using balenaEtcher.
3. Booted the HP EliteDesk Mini from the USB installer.
4. Installed Proxmox VE onto the system's internal storage.
5. Connected the host to the network using Ethernet.
6. Opened the Proxmox web interface from a laptop to manage the host.

## Verification
- The Proxmox host completed installation and booted successfully.
- The web management interface was reachable from the laptop on the network.

## Outcome
A working Proxmox host was established as the foundation for future virtual machines and homelab services.

## Skills Practiced
- Bootable media creation
- Hypervisor installation
- Basic host networking
- Accessing a web-based administration interface

## Notes
Screenshots can be added to the repository's `screenshots/` folder. Avoid publishing private IP addresses, credentials, or other sensitive information in screenshots.
