# Admin Configuration

[← README](../README.md) | [← 02 Compiling](02-compiling.md)

---

## admins.txt

Open `config/admins.txt` in any text editor. Delete everything in it. Add one line per admin:

```
BYONDUsername = Rank
```

Example:

```
Cameron653 = Host
```

Save and close.

---

## Ranks

Case-sensitive. `host` won't work; `Host` will.

| Rank | Access |
|------|--------|
| `Host` | Full permissions; bypasses all admin checks |
| `Admin` | Standard full-admin |
| `Moderator` | Player management; no server-level access |
| `Mentor` | Help channel only; no admin powers |

Rank permissions are defined in `config/admin_ranks.txt`. The defaults are fine for a private server.

---

## Verifying In-Game

Your rank from `admins.txt` applies the moment you connect. Open the **Admin** tab in the top menu to confirm. If the tab's missing, the username in `admins.txt` doesn't match your BYOND login exactly.

---

## Other Config Files

| File | Controls |
|------|----------|
| `config/config.txt` | Server name, port, round restart settings |
| `config/game_options.txt` | Antagonist toggles, vote options |
| `config/dbconfig.txt` | Database connection (leave blank for no DB) |
| `config/admin_ranks.txt` | Permission definitions per rank |

For a basic private server, only `admins.txt` and `config.txt` need attention.

---

[04: Launching](04-launching.md)
