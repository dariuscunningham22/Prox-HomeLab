# Virtual Machine: Ubuntu Lab Client

## Status: Planned

Ubuntu Desktop LTS is intended to be the first client VM on the isolated
OPNsense LAN. It will provide a graphical browser for accessing the
OPNsense web GUI and a client environment for network testing.

## Proposed VM configuration

  Setting   Planned value
  --------- ----------------------
  VM name   `Ubuntu-Lab-Client`
  OS        Ubuntu Desktop LTS
  CPU       2 cores
  Memory    4 GiB
  Disk      32 GiB (`local-lvm`)
  Network   VirtIO on `vmbr1`

## Expected network configuration

-   IPv4 address: `10.10.10.100–10.10.10.199` (DHCP)
-   Gateway: `10.10.10.1`
-   DNS: OPNsense LAN gateway (depending on DHCP/DNS configuration)

## Planned validation

``` bash
ip addr
ip route
ping -c 4 10.10.10.1
ping -c 4 8.8.8.8
ping -c 4 google.com
```

After installation and testing, update this document with actual VM
specs, address lease, test results, and screenshots.
