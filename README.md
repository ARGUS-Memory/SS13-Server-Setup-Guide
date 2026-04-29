# SS13 Private Server Setup Guide

Get a local SS13 server running from a public codebase. Five steps, no database required.

---

## Prerequisites

- **BYOND** installed: [byond.com](https://www.byond.com/download)
- A codebase download or clone (VOREStation, tgstation, CHOMPStation, etc.)
- Windows (Dream Maker and Dream Daemon are Windows-native)

---

## Setup

### 1. Get the code

Download the repository ZIP from GitHub (**Code → Download ZIP**, top-right of the file list) and extract it to a folder with no spaces in the path.

[Full details: 01-getting-the-code.md](docs/01-getting-the-code.md)

---

### 2. Compile

`config/` is empty on a fresh clone. Before compiling, copy these files from `config/example/` into `config/`:

- `admins.txt`
- `admin_ranks.txt`
- `config.txt`
- `game_options.txt`
- `dbconfig.txt`

Then double-click `BUILD.bat` in the repository root (or `bin/build.cmd`). The build script compiles the DM code and the tgui JavaScript layer and installs Node automatically on Windows. A full compile takes 3-15 minutes.

[Full details: 02-compiling.md](docs/02-compiling.md)

---

### 3. Set yourself as admin

Open `config/admins.txt`, delete the placeholder content, and add:

```
YourBYONDUsername = Host
```

Rank capitalisation matters. Save and close.

[Full details: 03-admin-config.md](docs/03-admin-config.md)

---

### 4. Launch

Open **Dream Daemon**, load the `.dmb` file from your codebase folder, and press **GO**. The server will be unresponsive for a minute or two while the world initialises; that's normal. Click the yellow **Join** button once it's up.

[Full details: 04-launching.md](docs/04-launching.md)

---

### 5. Port forwarding (remote players only)

Forward port **2337** (TCP + UDP) through your router to your PC's local IP. Players connect via `byond://YOUR.PUBLIC.IP:2337`.

[Full details: 05-port-forwarding.md](docs/05-port-forwarding.md)

---

## Changing the Map

Open the `.dme` in Dream Maker, uncheck the current map's `.dm` file under `maps/`, check the one you want, and recompile.

| Map | Notes |
|-----|-------|
| `virgo_minitest` | Smallest; compiles and loads fastest |
| `tether` | Mid-size station |
| `stellar_delight` | Larger station |
| `groundbase` | Surface/ground variant |

[Full details: 06-map-selection.md](docs/06-map-selection.md)

---

## Quick Notes

- Nothing is exposed to the internet until you forward a port.
- Players need a free BYOND account to connect.
- Admin ranks are case-sensitive: `host` won't work, `Host` will.
- If Dream Daemon crashes immediately, the compile finished with errors.
