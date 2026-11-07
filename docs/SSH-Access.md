# SSH Access to the Proxmox Host

## Objective
Manage the Proxmox host remotely through a terminal from a Windows laptop.

## Environment
- **Client:** Windows laptop using PowerShell
- **Remote host:** Proxmox VE host
- **Protocol:** SSH

## Connection
From Windows PowerShell, connect using the Proxmox host's address:

```powershell
ssh root@<PROXMOX-IP-ADDRESS>
```

Replace `<PROXMOX-IP-ADDRESS>` with the host's current IP address. Do not publish your actual home IP details in a public repository.

On first connection, SSH may ask to verify the host's fingerprint. Verify it through a trusted method before accepting.

## Verification
Successfully established an SSH session to the Proxmox host from PowerShell and used the remote command line for administration.

## Skills Practiced
- SSH remote access
- Windows PowerShell
- Linux command-line administration
- Remote server management

## Security Notes
- Never commit passwords, private SSH keys, or authentication tokens.
- Prefer SSH keys and appropriate account security for ongoing administration.
- Restrict administrative access to trusted devices and networks.
