# Ubuntu Lab Client Virtual Machine

## Overview

An Ubuntu Linux virtual machine was deployed on Proxmox VE as a client system within the isolated homelab network.

The Ubuntu VM connects to the OPNsense LAN interface through the Proxmox `vmbr1` bridge. It serves as a client machine for testing network connectivity, routing, DHCP, and firewall functionality.

## Virtual Machine Specifications

| Configuration | Value |
|---|---|
| VM Name | Ubuntu-Lab-Client |
| Hypervisor | Proxmox VE 9.2.1 |
| Operating System | Ubuntu Desktop |
| Version | 26.04.01 |
| Network Bridge | vmbr1 |
| IPv4 Address | 10.10.10.100/24 |
| Default Gateway | 10.10.10.1 |
| CPU | 2 cores |
| RAM |4 GB |
| Disk Size| 32 GB |


## Network Configuration

The Ubuntu VM is connected to the isolated lab network through `vmbr1`.

| Setting | Value |
|---|---|
| Network | 10.10.10.0/24 |
| Client IP | 10.10.10.100 |
| Gateway | 10.10.10.1 |
| Gateway Device | OPNsense LAN |
| Proxmox Bridge | vmbr1 |


## Installation Process

1. Created a new Ubuntu virtual machine in Proxmox.
2. Configured the virtual machine hardware.
3. Connected the virtual network adapter to `vmbr1`.
4. Installed Ubuntu Linux.
5. Completed the initial system configuration.
6. Verified the assigned IP address.
7. Used the Ubuntu client to test the isolated lab network.

## Testing and Validation

The Ubuntu client is intended to validate:

- Connectivity to the OPNsense LAN gateway.
- Communication within the isolated lab network.
- Routing through the OPNsense firewall.
- Internet connectivity through OPNsense.
- DNS resolution.
- Firewall rule behavior.

Document the actual results of each test as they are completed.

## Purpose

The Ubuntu client provides a Linux workstation for future lab activities, including:

- Linux system administration
- Network troubleshooting
- Firewall testing
- SSH configuration
- Security tools installation
- Vulnerability scanning in the isolated lab
- Log analysis and monitoring

## Skills Demonstrated

- Linux virtual machine deployment
- Ubuntu installation
- IP addressing
- Virtual networking
- Network connectivity testing
- Linux administration
