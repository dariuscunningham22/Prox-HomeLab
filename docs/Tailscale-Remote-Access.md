# Tailscale Remote Access

## Objective
Enable remote access to the Proxmox homelab when the laptop is connected to a network outside the home network.

## Environment
- Tailscale installed on the Proxmox host.
- Tailscale installed on the Windows laptop.
- Both devices authenticated to the same Tailscale network (tailnet).

## Implementation Summary
1. Installed Tailscale on the Proxmox host.
2. Installed Tailscale on the laptop.
3. Authenticated both devices to Tailscale.
4. Confirmed the devices appeared in the Tailscale device network.
5. Used the Proxmox web interface from the laptop while connected to a different network.

## Verification
Remote access was tested successfully: the Proxmox web interface could be reached from the laptop over Tailscale while the laptop was away from the home network.

## Outcome
Tailscale provides a private remote connectivity path for homelab administration without needing to expose the Proxmox management interface directly to the public internet.

## Skills Practiced
- Remote access configuration
- Overlay networking fundamentals
- Device authentication
- Remote connectivity testing

## Security Notes
- Do not publish Tailscale authentication keys, recovery codes, or private device details.
- Do not expose the Proxmox management interface directly to the public internet.
- Review device access and account security periodically.
