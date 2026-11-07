# Homelab Network Overview

## Purpose
Record the basic network arrangement used by the Proxmox homelab and how the administrator connects to it.

## Current Arrangement
- The HP EliteDesk Mini running Proxmox VE is connected to the home network through Ethernet.
- The Windows laptop is used to administer the host.
- The Proxmox web interface is accessible from the laptop on the local network.
- Tailscale is installed on both the Proxmox host and the laptop.
- Remote access to the Proxmox web interface over Tailscale was tested successfully from a different network.

## Conceptual Diagram

```text
                 Local Home Network
                        |
                 Ethernet connection
                        |
              HP EliteDesk Mini
                Proxmox VE Host
                        |
                 Proxmox Web UI
                        |
             Tailscale connectivity
                        |
                 Windows Laptop
              (local or remote network)
```

## Current Scope
This document describes the current host and management access only. Virtual machine networks, VLANs, firewall rules, and network segmentation will be documented when implemented.

## Security Considerations
- Keep management access limited to trusted devices.
- Do not include passwords, private keys, or sensitive network details in this public repository.
- Avoid exposing the Proxmox management interface directly to the public internet.
