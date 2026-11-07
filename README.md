# Prox-HomeLab
My proxmox homeserver to host services, experiment and gain technical hands on experience
# Proxmox Homelab

## Overview

This repository documents my personal homelab built using Proxmox VE. The purpose of this project is to gain hands-on experience with virtualization, Linux administration, networking, remote access, and system administration while developing practical skills for entry-level IT, help desk, and cybersecurity roles.

I will use this repository to document configurations, troubleshooting processes, project implementations, and lessons learned throughout the development of my homelab.

## Hardware & Environment

| Component          | Specification            |
| ------------------ | ------------------------ |
| Host System        | HP EliteDesk Mini 600 G5 |
| Memory             | 32 GB RAM                |
| Storage            | 1 TB                     |
| Hypervisor         | Proxmox VE 9.2.1         |
| Network Connection | Ethernet                 |
| Management Device  | Windows laptop           |
| Remote Access      | Tailscale                |

## Current Implementation

### Proxmox VE Installation

- Installed Proxmox VE 9.2.1 on a refurbished HP EliteDesk Mini.
- Configured the system for network connectivity through Ethernet.
- Accessed the Proxmox web interface from a Windows laptop.
- Established a foundation for managing virtual machines and virtualized services.

### Repository Configuration

- Configured the Proxmox no-subscription repository.
- Disabled the enterprise repositories to avoid subscription-related repository errors.
- Configured Debian and Proxmox package sources.
- Verified repository connectivity using `apt update`.

### SSH Administration

- Established SSH access to the Proxmox host from Windows PowerShell.
- Practiced remote Linux system administration through the command line.

### Tailscale Remote Access

- Installed and configured Tailscale on the Proxmox host and personal laptop.
- Verified remote access to the Proxmox web interface over a different network.
- Established a secure remote management method for the homelab.

## Planned Projects

- [ ] Deploy a Windows Server virtual machine.
- [ ] Configure Active Directory Domain Services.
- [ ] Create and manage domain users and groups.
- [ ] Join a Windows client to the domain.
- [ ] Configure Group Policy Objects (GPOs).
- [ ] Deploy an Ubuntu Server virtual machine.
- [ ] Install Jellyfin using Docker.
- [ ] Document virtual networking and network segmentation.
- [ ] Implement centralized logging and monitoring.
- [ ] Expand the homelab with additional cybersecurity projects.

## Repository Structure

```text
Proxmox-Homelab/
├── README.md
├── docs/
│   ├── Proxmox-Installation.md
│   ├── Repository-Configuration.md
│   ├── SSH-Access.md
│   └── Tailscale-Remote-Access.md
├── virtual-machines/
│   ├── Windows-Server.md
│   └── Ubuntu-Server.md
├── networking/
│   └── Homelab-Network.md
├── screenshots/
└── scripts/
```

## Skills Developed

- Virtualization and hypervisor administration
- Linux command-line administration
- SSH remote administration
- Network connectivity troubleshooting
- Repository and package management
- Remote access configuration
- Virtual machine deployment
- Technical documentation

## Project Goals

The long-term goal of this homelab is to create a realistic environment for practicing IT administration, networking and cybersecurity concepts. As the environment expands, I will document each implementation, configuration, troubleshooting process, and verification step.

This project is ongoing and is being created halfway through my junior year of college and will continue to evolve as I develop new technical skills.
