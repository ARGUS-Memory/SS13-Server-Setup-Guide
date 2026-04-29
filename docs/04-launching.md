# Launching the Server

[← README](../README.md) | [← 03 Admin Config](03-admin-config.md)

---

## Loading the Server in Dream Daemon

Search for **Dream Daemon** in the Start menu. It installs with BYOND.

1. Click the three-dot menu (or folder icon, depending on your BYOND version).
2. Navigate to the codebase folder.
3. Select the `.dmb` file (compiled output from Dream Maker, same name as the `.dme`).
4. Click **Open**.

---

## Port

Check the **Port** field before pressing GO. Default is `2337`. Change it here if that port's taken. Whatever you set is what players use to connect.

---

## Starting

Press **GO**.

Dream Daemon will appear frozen for 30 seconds to a couple of minutes. It's loading map files and running subsystem initialisation. Don't close it.

---

## Joining

Once Dream Daemon shows the world as running, click the yellow **Join** button. Wait for the in-game initialisation to finish before running any commands; the round starts in a pre-game lobby.

---

## Starting the Round

In the **Admin** tab:

```
Start-Now
```

Skips the countdown. Or just let the pre-game timer expire normally.

---

## Stopping

Press **STOP** in Dream Daemon. The world saves before closing. Closing the window directly mid-round may lose save state.

---

[05: Port Forwarding](05-port-forwarding.md)
