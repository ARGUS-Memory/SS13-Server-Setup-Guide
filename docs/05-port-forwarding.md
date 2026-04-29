# Port Forwarding

[← README](../README.md) | [← 04 Launching](04-launching.md)

---

Skip this if you're running the server for yourself or LAN only. You only need it if players are connecting from outside your network.

---

## What to Forward

Default BYOND port: **2337**. Set in Dream Daemon before pressing GO. Forward that port, both **TCP and UDP**.

---

## Router Steps

1. Find your router's admin panel IP. Run `ipconfig` in a command prompt; look for **Default Gateway** (usually `192.168.1.1` or `192.168.0.1`).
2. Log into the router panel. Credentials are usually on a sticker on the router.
3. Find **Port Forwarding** (sometimes listed under Advanced, NAT, or Firewall).
4. Add a rule:
   - **External port:** 2337
   - **Internal IP:** your PC's local IP (`ipconfig` → **IPv4 Address** on your active adapter)
   - **Internal port:** 2337
   - **Protocol:** TCP + UDP (add two rules if the router separates them)
5. Save.

Search *"port forward [router model]"* for model-specific instructions with screenshots.

---

## Your Public IP

Players use your **public** IP, not your local one. Check [ifconfig.me](https://ifconfig.me).

Share as:

```
byond://YOUR.PUBLIC.IP:2337
```

---

## If It Still Doesn't Work

**ISP block:** Some residential ISPs block all inbound connections by default. Port forwarding works at your router but traffic never reaches it. Options:

- **VPN with port forwarding** (AirVPN, Mullvad): forward through the VPN's IP instead of your home IP.
- **Tailscale or ZeroTier**: overlay network. Players install the client and join your network directly. No ISP involvement.
- **VPS relay**: cheap VPS running a proxy that tunnels to your home machine.

**Windows Firewall:** Even with forwarding correct, Defender may be blocking Dream Daemon. Go to **Windows Defender Firewall → Allow an app through firewall**, find Dream Daemon, and make sure both Private and Public are checked.

---

[06: Map Selection](06-map-selection.md)
