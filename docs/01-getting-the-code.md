# Getting the Code

[← README](../README.md)

---

## Choosing a Codebase

| Codebase | Repo | Notes |
|----------|------|-------|
| VOREStation | github.com/VOREStation/VOREStation | Vore/furry RP |
| CHOMPStation2 | github.com/CHOMPStation2/CHOMPStation2 | Vore/furry, different balance |
| tgstation | github.com/tgstation/tgstation | Mainline; most actively developed |
| baystation12 | github.com/baystation12/baystation12 | Heavy RP focus |

This guide uses VOREStation as the reference. Steps are identical for others.

---

## Downloading

GitHub ZIP: click the green **Code** button on the repo page, then **Download ZIP**.

Git clone (better for ongoing work if you have Git installed):

```
git clone https://github.com/VOREStation/VOREStation.git
```

---

## Extracting

Extract to a path with no spaces or special characters. BYOND breaks on both.

```
C:\SS13\VOREStation\        <- fine
C:\Users\My Name\Desktop\   <- will cause problems
```

The extracted root contains the `.dme` file, `code/`, `config/`, `maps/`, and several others. The `.dme` is the entry point for compiling and for Dream Maker's file tree.

---

[02: Compiling](02-compiling.md)
