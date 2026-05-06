# NTE DPS Meter

Real-time damage statistics tool for Neverness to Everness (NTE).

Reads combat data through passive packet analysis — no game memory injection, no game file modification.

**Version**: v2.00 | **Supported game version**: v1.08+

## Features

### DPS Calculation

| Item | Description |
|------|-------------|
| Basis | Average damage per second over the recorded time |
| Scope | All characters in your party (personal) |
| Start | Begins on first hit |
| End | Stops on last hit |

Reflects your entire combat performance — deaths, idling, and positioning mistakes all count against your DPS since the timer keeps running while no damage is dealt.

### Free

- **DPS Overlay** — Always-on-top transparent card with circular avatar + breathing ring + 3-line real-time stats; auto-expands during combat, auto-collapses when idle
- **Character Detection** — Automatically identifies the active character, supports all 17 characters
- **Battle Report Manager** — Auto-saves on reset; filter by damage range, sort, upload to community
- **Community Rankings** — Per-character damage rankings (tier-based by battle duration); requires uploading a report to unlock
- **Hotkeys** — Show/hide overlay, reset stats (F6); fully customizable key bindings
- **Network Adapter Selection** — Manually select adapter when traffic is unclear; ExitLag continuously supported
- **Tri-lingual Interface** — 繁體中文 / 简体中文 / English (instant switch)
- **System Tray Resident** — No taskbar clutter
- **Auto-update** — Manual check triggers automatic update process

### Sponsor Features

Includes all free features, plus:

- **Main Window** — Intuitive interface to view full team damage contribution at any time, data stored locally
- **Report Comparison** — Side-by-side A/B comparison of different team compositions + efficiency summary
- **Team Composition Stats** — Community character pairing heatmap ([ntedpsmeter.com](https://ntedpsmeter.com))
- **Full Analytics Access** — Rankings + Compositions, all features unlocked

### Community Analytics Platform

Online at [ntedpsmeter.com](https://ntedpsmeter.com), aggregating community combat data:

- **Character Damage Rankings** — Tier-based (1min / 3min / 6min / 9min) with median + max + range display
- **Pairing Matrix** — Visual character combination adoption rates (Sponsor only)
- **Connect Flow** — Paste your Device ID or Analytics Token to view personal stats on the web
- **Tri-lingual Website** — EN / 繁中 / 簡中
- **Privacy-first** — Explicit consent before upload, anonymized data

## System Requirements

- Windows 10 / 11
- [Npcap](https://npcap.com/) — Packet capture driver (check "WinPcap API-compatible Mode" during installation)
- Run as **Administrator**

## Usage

1. Install Npcap (first-time install handled automatically by the updater)
2. Run `NTE_DPS_Meter.exe` (Right-click → Run as administrator)
3. Launch the game; the overlay automatically displays DPS when combat begins
4. Right-click menu provides access to main window, network adapter, report manager, hotkey settings, and more

### Default Hotkeys

| Hotkey | Function |
|--------|----------|
| `F6` | Reset stats and save battle report |
| `Alt + D` | Show/hide overlay |
| `Alt + E` | Show/hide main window (Sponsor) |

Hotkeys can be customized in settings.

## Safety

This tool only passively reads network packets, similar to Wireshark:

- Does not read or modify game memory
- Does not inject DLLs or hook game processes
- Does not send any packets to the game server
- Does not modify any game files

## FAQ

**Q: The overlay isn't responding?**
A: Make sure you're running as administrator and that Npcap is properly installed.

**Q: Can't capture packets with an accelerator/VPN active?**
A: Open "Select Network Adapter" from the system tray and manually switch to the correct network interface.

**Q: Are the displayed damage values accurate?**
A: Values come directly from combat packets sent by the game client, consistent with the game's internal calculations.

**Q: Why does my antivirus keep flagging it?**
A: This program does not yet have an EV code signing certificate (expensive). Windows Defender may flag it as unknown. Please add the program folder to your exclusion list:

Right-click Desktop → Display Settings → Privacy & Security → Windows Security → Virus & Threat Protection → Manage Settings → scroll down to "Exclusions" → Add an exclusion → Add exclusion scope → Folder → select the program directory

## Third-Party Tool & Disclaimer

This is a third-party tool with no affiliation to Hotta Studio or Perfect World.

- **How it works**: Uses passive network packet analysis (Passive Sniffing) to calculate combat data. Does not modify game memory, alter game packets, or provide any automation capabilities.
- **Risk assessment**: Despite its non-intrusive design, official definitions of "third-party tools" vary. Please review NTE's official policy before use.
- **Disclaimer**: This program is intended for technical discussion and combat data analysis only. The developer assumes no legal liability or compensation obligation for any account restrictions or losses resulting from use of this tool. Running the program constitutes acceptance of this disclaimer.

## Sponsorship

Sponsor serial keys are a thank-you reward for supporting development — not a subscription. Each key is valid for 30 days. Not sponsoring does not affect free features in any way.

## Contact

- Email: dont.stop.ha@gmail.com
- Discord: https://discord.gg/nbTMDCpvrB

---

NTE DPS Meter by Aletheia
