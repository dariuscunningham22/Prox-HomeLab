# Virtual Machine: OPNsense Firewall

## Purpose

A virtual OPNsense firewall/router provides routing and firewalling for
a dedicated internal homelab network.

## Proxmox settings

  Setting     Value
  ----------- -----------------------
  VM name     `OPNsense-Firewall`
  Firmware    SeaBIOS
  CPU         2 cores
  Memory      2 GiB
  Disk        20 GiB (`local-lvm`)
  Network 0   VirtIO, `vmbr0` (WAN)
  Network 1   VirtIO, `vmbr1` (LAN)

## Interfaces

-   WAN (`vtnet0`): DHCP from home router.
-   LAN (`vtnet1`): `10.10.10.1/24`.

## Current status

Installed and booted successfully. Interface configuration and ping
tests have been performed. Web GUI finalization, Ubuntu client
validation, configuration backup, and persistence test remain to be
documented/completed as applicable.
