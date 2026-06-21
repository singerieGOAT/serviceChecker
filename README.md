# serviceChecker

*by singerieWhip*

A Windows console tool that shows the status and start-up type of a set of monitored services and lets you start or stop any of them by number — all from a single administrator session.

> **Built entirely with AI** — every line of C++ in this project was written by [Claude](https://claude.ai) (Anthropic).

---

## Objective

serviceChecker gives you a quick, single-screen view of a fixed list of Windows background services and one-key control over each of them.

It is the companion to **singerieCleaner**: where that tool *stops* services, serviceChecker does the inverse and makes sure they are **running** again. Starting a service that was left **Disabled** automatically restores its normal start-up type first, then starts it. Nothing is ever deleted.

> **Reboot your PC after changing a service's status** so the change is fully applied.

---

## What it does

serviceChecker runs as an elevated console application and shows a numbered table of the monitored services:

```
   #  SERVICE             | STATUS      | START TYPE
   -- --------------------|-------------|---------------------
    1 SysMain             | Running     | Automatic
    2 CDPSvc              | Running     | Automatic
    3 PcaSvc              | Stopped     | Manual
    4 DPS                 | Running     | Automatic
   ...
```

Controls:

- **`[number]`** — toggle the service on that line: start it if it is stopped, stop it if it is running. The action applies immediately and the table refreshes — no need to press Enter.
- **`[A]`** — start every stopped service at once.
- **`[R]` / Enter** — refresh the table.
- **`[0]`** — quit.

Colours: status is green when *Running*, red when *Stopped* or missing, cyan while *pending*; start type is green for *Automatic*, yellow for *Manual*, red for *Disabled*.

---

## Requirements

- Windows 10 / 11
- Administrator rights (the app auto-elevates via UAC if needed)
- x64

---

## Checksum

**SHA-256** (Release x64):
```
B8B920D6F60194F7F39609EAC5C80820B01C3516BD26DC92509C15A7B18CF5D6
```

VirusTotal scan: https://www.virustotal.com/gui/file/b8b920d6f60194f7f39609eac5c80820b01c3516bd26dc92509c15a7b18cf5d6
