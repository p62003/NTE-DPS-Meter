# Patch Notes

---

## v2.00 — May 6, 2026

### New Feature: Community Analytics

A community-driven analytics platform is now live at [ntedpsmeter.com](https://ntedpsmeter.com).

**Rankings**
- Character damage rankings are now available, segmented by effective combat duration into four tiers: 1-minute, 3-minute, 6-minute, and 9-minute.
- Each character entry displays minimum, median, and maximum damage across all submitted reports in that tier.
- Rankings are accessible to all users who have uploaded at least one qualifying battle report.

**Character Pairing Rates**
- A 17×17 heatmap visualizing how frequently each character pair appears together in submitted team compositions.
- Available to Sponsors via Analytics Token verification.

**Connect**
- Paste your Device ID or Analytics Token on the Connect page to link your local data with your web profile.
- Once connected, personal upload history and ranking positions are visible on the website.

**Website**
- Full tri-lingual support: English, Traditional Chinese, Simplified Chinese.
- Language preference is persisted across sessions.

---

### New Feature: Battle Reports

**Saving**
- Pressing the Reset hotkey (default: F6) now saves the current combat session as a battle report.
- Reports are stored locally in JSON format and persist between application restarts.

**Report Manager**
- A dedicated management interface for browsing all saved reports.
- Filter by damage range, sort by multiple criteria, and view upload status at a glance.

**Report Comparison**
- Select any two reports for side-by-side A/B comparison.
- Displays damage difference, DPS difference, and an efficiency verdict indicating whether performance improved or declined.

**Upload**
- Upload qualifying reports to the community analytics platform directly from the Report Manager.
- Minimum threshold: 100,000 total damage, combat duration under 9 minutes.
- A privacy consent dialog is presented before first upload. All data is anonymized.

---

### New Feature: Sponsor System

- Sponsor serial keys are available as a thank-you for supporting continued development.
- Each key is valid for 30 days and bound to a single device.
- Activation and deactivation are handled automatically on application launch and exit.
- Sponsors gain access to: Main Window, Report Comparison, Character Pairing Rates, and full analytics platform features.

---

### New Feature: Auto-Updater

- A standalone updater (`NTE_Updater.exe`) handles the entire update process independently from the main application.
- On first run, the updater detects whether Npcap is installed and guides the user through official installation if needed.
- Updates are differential — only modified files are downloaded based on manifest comparison.
- The update process runs entirely in the background with a responsive UI.

---

### Overlay

- The DPS overlay card has been redesigned with a circular character portrait, a breathing ring animation, and a colored border that matches the active character's element.
- Three data lines are displayed: total damage, DPS, and hit count.
- The overlay automatically expands when combat is detected and collapses when idle.
- Character switches trigger a layered expand animation.
- Right-clicking the overlay now opens a full context menu with access to all application features.

---

### Main Window (Sponsor)

- A dual-panel display showing character damage rankings on the left and per-hit detail on the right.
- View your full party's damage contribution breakdown at any time.
- All data is processed and stored locally.

---

### Interface

**Tri-lingual Support**
- The application interface supports Traditional Chinese, Simplified Chinese, and English.
- Language can be switched instantly without restarting.

**Hotkeys**
- Default bindings: F6 (reset and save report), Alt+D (toggle overlay), Alt+E (toggle main window).
- All hotkeys are fully customizable through the hotkey settings dialog.

**Context Menu**
- A unified right-click menu is shared between the system tray icon and the overlay.
- Provides access to: Main Window, Report Manager, Network Adapter, Hotkey Settings, Copy Device ID, Copy Analytics Token, Announcement, Discord, and Language Switch.

**Announcement Window**
- Displays serial key status, current version, and the latest changelog on startup.
- Content is fetched from the update server; falls back to a local cache when offline.

**General**
- All interactive elements now provide press feedback (scale + bounce) on click.
- The application resides in the system tray without occupying taskbar space.

---

### Network

- A manual network adapter selection dialog is available when the tool cannot automatically detect game traffic.
- ExitLag is continuously supported.

---

### Security

- Upload validation now enforces UUID format on device identifiers, team/character data consistency, and cross-validates damage totals against individual character damage sums.
- Rate limiting operates on client IP to prevent device ID rotation bypass.
- API key verification uses constant-time comparison.

---

## v1.00 — April 30, 2026

### Initial Release

- Passive network packet sniffing for NTE combat data.
- Real-time DPS overlay with automatic character detection for all 17 launch characters.
- Npcap integration. Requires Administrator privileges.

---

NTE DPS Meter by Aletheia
