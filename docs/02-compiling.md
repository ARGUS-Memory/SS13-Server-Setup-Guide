# Compiling

[← README](../README.md) | [← 01 Getting the Code](01-getting-the-code.md)

---

## Config Setup

Do this before compiling.

1. Open the codebase folder in Explorer.
2. Go into `config/example/`.
3. Select all (`Ctrl+A`), copy, paste into `config/`.
4. If Windows asks about conflicts, choose **Don't copy**.

Any file already in `config/` stays as-is. The example files are defaults for files that don't exist yet.

---

## Compiling

The recommended way to compile is the build script, not Dream Maker directly. The build script handles tgui (the JavaScript UI layer) and other dependencies alongside the DM code.

**Option A: double-click `BUILD.bat`** in the repository root. It will wait for a keypress before closing so you can read the output.

**Option B: double-click `bin/build.cmd`**. Same result, closes as soon as it finishes.

**Option C: VSCode** users can press `Ctrl+Shift+B` to build, or `F5` to build and launch with the debugger attached.

The script installs a private copy of Node automatically on Windows. No manual Node setup needed.

Output streams in the terminal window. A full compile of VOREStation takes 3-15 minutes depending on your machine. A successful build ends with a line like:

```
Saving VOREStation.dmb (###KB)
```

That `.dmb` is the compiled server binary used by Dream Daemon.

The build script skips steps whose inputs haven't changed since the last run, so incremental builds after small changes are much faster.

---

## Common Errors

| Error | Cause |
|-------|-------|
| `undefined var` / `undefined proc` | Missing dependency or bad merge; check for submodules (`tgui`, `rust-g`) |
| `cannot find file` | Path has spaces or non-ASCII characters; move the folder |
| Build hangs indefinitely | Antivirus scanning every file as it runs; add the codebase folder to AV exclusions |
| tgui build fails | Node install failed or was blocked; check the terminal output for npm errors |

---

[03: Admin Config](03-admin-config.md)
