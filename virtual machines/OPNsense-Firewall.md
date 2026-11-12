# OPNsense Virtual Firewall

## Overview

OPNsense was deployed as a virtual machine on Proxmox VE to serve as the firewall and router for the isolated homelab network.

The virtual machine provides hands-on experience with firewall administration, routing, network segmentation, DHCP, and network troubleshooting.

## Virtual Machine Specifications

| Configuration | Value |
|---|---|
| VM Name | OPNsense |
| Hypervisor | Proxmox VE 9.2.1 |
| CPU | 2 cores |
| Memory | 2048 MB (2 GB) |
| Storage | 20 GB |
| BIOS | SeaBIOS |
| Disk Storage | local-lvm |
| Network Adapter 1 | VirtIO - vmbr0 |
| Network Adapter 2 | VirtIO - vmbr1 |

## Network Configuration

OPNsense was configured with two network interfaces.

| Interface | Proxmox Bridge | Purpose |
|---|---|---|
| WAN (vtnet0) | vmbr0 | Connects to the existing home network |
| LAN (vtnet1) | vmbr1 | Connects to the isolated lab network |

### WAN Configuration

- WAN interface obtains its IP address through DHCP from the home router.
- WAN connects through the Proxmox `vmbr0` bridge.

### LAN Configuration

- LAN IP Address: `10.10.10.1`
- Subnet Mask: `255.255.255.0`
- Network: `10.10.10.0/24`
- DHCP Pool: `10.10.10.100 - 10.10.10.199`

The LAN interface provides connectivity to virtual machines connected to the isolated `vmbr1` bridge.

## Installation and Configuration Process

1. Uploaded the OPNsense ISO installer to Proxmox.
2. Created a new OPNsense virtual machine.
3. Configured CPU, memory, storage, and network interfaces.
4. Attached the OPNsense installation ISO.
5. Installed OPNsense and rebooted the VM.
6. Assigned WAN and LAN interfaces.
7. Configured the LAN IP address and DHCP range.
8. Configured firewall and network settings.
9. Performed network connectivity tests.

## Testing and Validation

Connectivity testing was performed after configuring the firewall.

The firewall was used to validate communication between the lab network and upstream network.

Additional testing and firewall rule documentation will be added as the lab expands.

## Purpose

The OPNsense virtual firewall provides a controlled environment for:

- Network segmentation
- Firewall rule configuration
- Routing and DHCP administration
- Network connectivity troubleshooting
- Security testing
- Isolated virtual machine networking

## Skills Demonstrated

- Firewall deployment and configuration
- WAN and LAN interface configuration
- Virtual networking in Proxmox
- DHCP configuration
- IP addressing and subnetting
- Network troubleshooting
