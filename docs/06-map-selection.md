# Map Selection

[← README](../README.md) | [← 05 Port Forwarding](05-port-forwarding.md)

---

Map selection in VOREStation is controlled by `#define` flags in a single file, not by checking files in Dream Maker's file tree.

---

## Switching Maps

1. Open `maps/~map_system/_map_selection.dm` in any text editor.
2. Comment out the active `#define` by adding `//` at the start of the line.
3. Uncomment the `#define` for the map you want by removing the `//`.
4. Save the file.
5. Recompile with `BUILD.bat` or `bin/build.cmd`.

Only one map define should be active at a time.

---

## Available Maps

| Define | Map folder | Notes |
|--------|-----------|-------|
| `USE_MAP_MINITEST` | `virgo_minitest` | Smallest map. Fastest compile and load. Good for local testing. |
| `USE_MAP_TETHER` | `tether` | Mid-size station. |
| `USE_MAP_STELLARDELIGHT` | `stellar_delight` | Larger station. Active by default. |
| `USE_MAP_GROUNDBASE` | `groundbase` | Surface/ground setting. |

### Example

To switch from `stellar_delight` to `virgo_minitest`, change:

```dm
//#define USE_MAP_TETHER
#define USE_MAP_STELLARDELIGHT
//#define USE_MAP_GROUNDBASE
//#define USE_MAP_MINITEST
```

to:

```dm
//#define USE_MAP_TETHER
//#define USE_MAP_STELLARDELIGHT
//#define USE_MAP_GROUNDBASE
#define USE_MAP_MINITEST
```

---

## After Switching

- Always recompile before launching. Switching the define without recompiling loads the old map or errors.
- Player saves in `data/player_saves/` are unaffected by map changes.
- Admin-placed objects and pre-placed structures don't carry over between maps.
