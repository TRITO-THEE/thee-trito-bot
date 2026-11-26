# thee_trito bot

[![Release](https://img.shields.io/github/v/release/TRITO-THEE/thee-trito-bot?color=2563EB&label=latest%20release)](https://github.com/TRITO-THEE/thee-trito-bot/releases/latest)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-blue)](https://github.com/TRITO-THEE/thee-trito-bot/releases/latest)
[![License](https://img.shields.io/badge/license-Proprietary-red)](#)

Windows desktop auto-coding bot for natural human-paced typing and automated project writing in Visual Studio Code.

---

## Quick Download

| Asset | Version | Size | Download |
|---|---|---|---|
| `thee_trito_bot_Setup.exe` | **v1.3.2** | 64.10 MB | [**Download Windows Setup Wizard**](https://github.com/TRITO-THEE/thee-trito-bot/releases/download/v1.3.2/thee_trito_bot_Setup.exe) |

### Integrity Verification (SHA-256)
Verify downloaded installer integrity in PowerShell before running:
```powershell
Get-FileHash .\thee_trito_bot_Setup.exe -Algorithm SHA256
# Expected SHA-256:
# 05544da3a254f79ca9c376504249f9214c676905df66374f34100bd2010004e1
```

---

## Key Features

- **Windows Setup Wizard (`thee_trito_bot_Setup.exe`)**: Dark-mode Inno Setup installer with optional Desktop shortcut, Start with Windows option, Start Menu entry, and clean Add/Remove Programs uninstaller.
- **Instant ~1-Second Launch**: Built on PyInstaller `--onedir` architecture—no temporary single-file extraction delay on startup.
- **Zero-Loss `%APPDATA%` Config Persistence**: Saves preferences, manifests, and session state to `%APPDATA%\thee_trito_bot\config` so upgrades and uninstalls preserve your data.
- **Hide to System Tray**: Click **Hide to Tray** (or **X** when enabled) to keep builds running in the taskbar tray; left/double-click tray icon to restore or right-click for quick actions.
- **Built-in 1-Click Silent Self-Updater**: Automatically checks GitHub Releases and upgrades installed files silently via `thee_trito_bot_Setup.exe` while preserving your config.
- **Dark-Graphite PySide6 Qt6 UI**: Solid, opaque desktop dashboard with floating real-time QWERTY HUD.
- **Self-Healing Editor Engine**: Real-time Cursor-Anchor Guard detects accidental clicks/keystrokes and repairs cursor drift automatically.
- **Natural 15–60 WPM Flow Waves & Mechanical Sound Engine**: Dynamic human typing cadence with optional Cherry MX / Topre / Model M mechanical key audio, Focus Guard, and Wake-Lock.

---

## Global Hotkeys

- `F8`: Pause / Resume build or typing session
- `F9` or `Esc`: Emergency stop (releases Shift/modifier keys immediately)

---

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for full release history.
