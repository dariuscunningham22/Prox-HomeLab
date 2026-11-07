# Proxmox Package Repository Configuration

## Objective
Configure package sources so the Proxmox host can retrieve updates without attempting to use subscription-only enterprise repositories.

## Background
During package updates, the Proxmox enterprise repository returned an authorization error because the host did not have an enterprise subscription. The repository configuration was adjusted to use the Proxmox no-subscription repository for this homelab.

## Configuration Summary
- Kept the Debian package sources configured for the installed Debian release.
- Configured the Proxmox VE no-subscription repository.
- Disabled the Proxmox enterprise repository.
- Disabled the Ceph enterprise repository, which also returned an authorization error during the initial update attempt.

## Verification
Ran the package index refresh command:

```bash
apt update
```

The updated configuration completed without the prior enterprise repository authorization errors. The package manager also reported available package upgrades.

## Skills Practiced
- Linux package management
- APT repository configuration
- Troubleshooting repository authorization errors
- Reading package manager output

## Caution
Repository configuration can vary by Proxmox VE and Debian release. Confirm the correct repository instructions in the official Proxmox documentation before making future changes. Do not blindly copy repository entries across versions.
