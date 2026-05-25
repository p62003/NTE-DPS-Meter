# Patch Notes

---

## v4.0 — May 25, 2026

### New Feature: Damage ECG (Electrocardiogram)

A real-time damage waveform chart in the main window that records every single hit.

- All party hits merged into one timeline. Wave colors reflect attack rhythm (green = rapid combos / gray = normal / red = gap between bursts).
- Character switch points are marked on the X-axis with avatar icons, showing rotation timing at a glance.
- Drag with inertia scrolling, Ctrl+scroll to zoom the time axis, hover to view character name and damage value.
- Collapsible, and also integrated into Report Comparison mode.

---

### New Feature: Personal Dashboard (Sponsor Exclusive)

Analyze your battle history and track personal growth. All data is processed locally — nothing is uploaded.

- **Combat Overview** — Total sessions, accumulated damage, most-used character, historical max damage table, last 5 battles.
- **Damage Growth** — Per-character damage trend curves. Click avatar buttons to switch characters.
- **Appearance Stats** — Character usage frequency analysis.
- **Dungeon Growth** — Per-stage damage progress curves.

---

### New Feature: Cultivation Guide (Free)

A material overview for 20 characters with tri-lingual support.

- **Breakthrough Materials** — Required materials and quantities per stage, with item icons.
- **Skill Upgrades** — Upgrade materials for 4 active skills + 2 passive skills (including passive unlock costs).
- **Bond Gifts** — Three strategies: Fons efficiency (best value), gold-only (zero Fons cost), fewest types (minimal inventory).

---

### New Feature: Discord Account Linking

- Link your Discord account from the desktop app with one click — opens the browser for OAuth authorization.
- Your linked Discord account can be used to log into the analytics platform and access full features.
- Serial activation now requires a linked Discord account to prevent abuse.

---

### Improvements

**Analytics Platform**
- Discord login is now supported. Once logged in, Rankings are directly accessible on the web.
- Sponsors can verify their serial key on the website after Discord login, without needing the desktop app.
- Report uploads now include stage information (mode/boss/difficulty), preparing for future stage-based rankings.

**Announcement Window**
- Serial management is now unified in the startup announcement window — all serial operations in one place.
- Discord binding is now required before activating a serial key.

**Context Menu**
- Menu items reorganized into logical groups for a cleaner structure.
- Sponsor-exclusive features (Dashboard, More Analytics) are now visible to all users, with a prompt shown for non-sponsors.

**Main Window**
- Header bar buttons rearranged for a more intuitive workflow.

**Simplified Chinese**
- Fixed character names, stage names, and cultivation material names not being properly converted in Simplified Chinese mode.

### Fixes

- Fixed overlay DPS dropping to zero or showing incorrect values after session transitions (timer state not cleared when freeze was lifted).
- Fixed serial deactivation not properly clearing binding data on restart (settings file not removing fields on deactivation).

---

## v3.1 — May 23, 2026

### New Features

- Report Manager now has a "Refresh" button — view new reports and apply language changes without closing the window.
- Report Manager now has an "Open Folder" button to quickly access the reports directory.
- Beyond the Rails now displays ECT (Estimated Clear Time), previously excluded.

### Improvements

**Session Architecture**
- Session mode detection refactored into a 3-primitive + 5-handler architecture, improving detection stability and maintainability.
- Anomaly Hunt now supports Boss19.
- Weekly Clone now supports retry detection (auto-saves when the same boss appears again). ⚠️ **Preview** — This feature is not yet stable. The reliable approach is to manually press F6 to reset DPS when retrying.

**Overlay**
- The overlay right-click menu is no longer blocked when other windows are open. You can now operate the overlay at any time.
- Unknown characters now display a fallback icon in the overlay and rank bar, replacing the "?" text.

**Main Window**
- When the main window is already open but in the background, triggering it again now brings it to the foreground instead of closing it.
- Reordered title bar buttons.

**Context Menu**
- Reordered menu items: language toggle moved next to network interface; diagnostics and dump moved above check for updates.

**Report Manager**
- Adjusted text color on gold buttons (Rankings, Pairings, Upload Selected) for better readability.

**Updater**
- Npcap downloads now include SHA256 checksum verification to prevent corrupted or tampered files.
- Added path traversal defense to block malicious manifest paths from accessing local files.

### Fixes

- Fixed overlay click-through not working during combat, restoring normal in-game interaction.
- Fixed certain characters (Daffodill, Fadia, Hotori) causing report uploads to be rejected.

---

## v3.0 — May 17, 2026

### New Feature: Session Mode Auto-Detection

The tool now automatically identifies the game mode you're playing and records full stage information in battle reports.

**Supported Modes**
- **High-Risk Commissions** — Automatically identifies boss and difficulty tier (I–VI). Reports display the commission name.
- **Weekly Clone** — Automatically identifies boss and difficulty tier (I–VII).
- **Anomaly Hunt** — Automatically identifies world bosses.
- **Beyond the Rails** — Automatically identifies route, station, and upper/lower half.
- When no mode can be matched, the session is marked as "Free Combat."

**Stage Information Display**
- A new "Stage" column in the Report Manager shows the commission name with a Roman numeral tier (e.g., "Beat King III", "Fracture Circle S5 Upper").
- Each mode has a dedicated icon, displayed in the Report Manager, main window dropdown, and comparison mode.
- Tier detection uses HP matching: mob health values extracted from DataTables are matched against observed values to determine the current difficulty.

---

### New Feature: HPS Indicator (Hits Per Second)

A new metric for measuring character attack speed.

- The overlay card displays total HPS on row 4.
- Also shown in the main window header, rank summary, and character detail panel.
- Battle report JSON now includes an `hps` field (total HPS + per-character HPS).

---

### New Feature: ECT Indicator (Estimated Clear Time)

Real-time estimation of how long it will take to defeat the current target.

- The overlay card displays ECT on row 5, formatted as `mm:ss`.
- Calculated as: target's current HP ÷ your DPS.
- ECT automatically follows when you switch attack targets.

---

### New Feature: Session End Freeze

- When a stage ends, the overlay freezes and retains the final combat data display.
- The overlay will not auto-collapse due to inactivity, letting you review your final performance.
- Automatically unfreezes when the next combat begins.

---

### Improvements

**Overlay**
- Data rows expanded from 3 to 5: Total Damage, Hit Count, DPS, HPS, ECT.
- Character portrait enlarged (22px → 33px) for better visibility.
- Unknown character placeholder now shows a gray avatar instead of a "?" text.
- Simplified click behavior: clicking during combat directly collapses the overlay without waiting for click-through to disengage.

**Main Window Now Free**
- All main window entry points (tray double-click, Alt+E, context menu) no longer require a Sponsor key.
- Report Comparison remains Sponsor-exclusive.

**Analytics Platform**
- Minimum upload damage threshold lowered from 100,000 to 50,000, allowing lower-level players' full boss kills to qualify for rankings.
- Added FAQ to the Compositions page explaining why report counts differ from Rankings.

**Performance & Stability**
- Packet processing hot-path optimizations for smoother performance during high hit rates.
- Improved memory usage: the Report Manager no longer retains full report data in memory.
- Internal code architecture cleanup for improved long-term stability.

---

### Fixes

- Fixed High-Risk Commission stage detection failure. When mobs attack the player, their HP values could pollute the boss HP observation pool, causing incorrect tier matching.
- Fixed `total_damage` calculation inconsistency during report upload.
- Fixed a memory leak caused by repeatedly opening and closing the Report Manager.
- Fixed report dropdowns in the main window and comparison mode not refreshing after deleting reports.

---

## v2.01 — May 7, 2026

### Fixes

**Overlay DPS Calculation**
- Fixed an issue where the overlay DPS was significantly lower than the report DPS after resetting (F6). The overlay's timer was not cleared on reset, causing the denominator to span the entire session instead of just the post-reset combat.

**Duplicate Upload Prevention**
- Reports can now only be uploaded once. The server uses device ID + timestamp as a unique key and rejects duplicate uploads.

---

### Improvements

**Report Manager**
- Uploaded reports now show a ✓ mark next to the date (dimmed) for easy identification.
- "Select All" automatically skips already-uploaded reports.
- Upload results now display a colored summary: ✓ success, ⟳ duplicate, ✗ failed.
- Failures show a player-friendly error message.
- Checkbox selection count updates in real time.
- Character names now follow the current language setting.
- Added "Rankings" and "Pairings" buttons that open the analytics platform with automatic authentication.

**Analytics Platform (ntedpsmeter.com)**
- The Connect page now supports automatic verification when opened from the desktop app — no need to manually paste tokens.
- Added FAQ sections to the Homepage, Rankings, and Pairing Rates pages explaining how median, pairing rates, and other stats are calculated.
- Report data no longer auto-expires.

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
