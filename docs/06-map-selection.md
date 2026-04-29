# Map Selection

[← README](../README.md) | [← 05 Port Forwarding](05-port-forwarding.md)

---

The active map is whichever `.dm` file is checked in the `.dme`. Only one should be checked at a time. The `.dmm` files (the actual map data) are loaded by code; you don't touch those.

---

## Switching Maps

1. Open the `.dme` in Dream Maker. Don't compile yet.
2. In the file tree, expand `maps/`.
3. Find the currently checked `.dm` file and uncheck it.
4. Expand the folder for the map you want and check its `.dm` file.
5. Compile: **Build → Compile**.

---

## VOREStation Maps

| Folder | File | Size | Notes |
|--------|------|------|-------|
| `virgo_minitest` | `virgo_minitest.dm` | Small | Fastest compile and load |
| `tether` | `tether.dm` | Medium | Standard station |
| `stellar_delight` | `stellar_delight.dm` | Large | Larger layout |
| `groundbase` | `groundbase.dm` | Medium | Surface/ground setting |

`virgo_minitest` is the fastest option for local testing. Compile time drops noticeably compared to the full maps.

---

## After Switching

- Always recompile before launching. A map switch without recompile loads the old map or errors.
- Player saves in `data/player_saves/` are unaffected by map changes.
- Admin-placed objects and pre-placed structures don't carry over between maps.

---

## Custom Maps

Drop the map folder under `maps/your_map_name/` and register the `.dm` file with the codebase map system. That's outside the scope of this guide.
