# thee_trito bot

[![Release](https://img.shields.io/github/v/release/TRITO-THEE/thee-trito-bot?color=2563EB&label=latest%20release)](https://github.com/TRITO-THEE/thee-trito-bot/releases/latest)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-blue)](https://github.com/TRITO-THEE/thee-trito-bot/releases/latest)
[![License](https://img.shields.io/badge/license-Proprietary-red)](#)

Standalone Windows desktop auto-coding bot for natural human-paced typing and automated project writing in Visual Studio Code.

---

## Quick Download

| Asset | Version | Size | Download |
|---|---|---|---|
| `thee_trito_bot.exe` | **v1.3.1** | 91.75 MB | [**Download Latest Executable**](https://github.com/TRITO-THEE/thee-trito-bot/releases/download/v1.3.1/thee_trito_bot.exe) |

### Integrity Verification (SHA-256)
Verify downloaded file integrity in PowerShell before running:
```powershell
Get-FileHash .\thee_trito_bot.exe -Algorithm SHA256
# Expected SHA-256:
# 2e96202aa8c01e4ed6c52d73f0db3134548e047466f57134442f81546a49e430
```

---

## Key Features

- **Dark-Graphite PySide6 Qt6 UI**: Solid, opaque, lightning-fast desktop dashboard with floating real-time QWERTY HUD and cross-platform `Fusion` styling.
- **Built-in 1-Click Auto-Updater**: Checks GitHub Releases automatically in the background. Installs updates in 1 click via zero-downtime hot-swapping while preserving all your local configuration profiles.
- **Crystal-Clear Manual Update Feedback**: Instant 3-state feedback on the "Check for Updates" button (`Update Available`, `Up to Date`, or `Offline / Network Error`).
- **Self-Healing Editor Engine**: Real-time Cursor-Anchor Guard automatically detects human clicks, arrow navigation, or accidental keystrokes, instantly repositioning the cursor and self-healing indentation drift.
- **Visual VS Code Explorer Mode**: Human-like mouse movements to the Explorer sidebar with smooth ease-out curves and automated fallback to high-speed filesystem file creation.
- **Natural 15–60 WPM Flow Waves**: Variable typing speed, rhythmic micro-pauses, human typo simulation, and customizable typing profiles.
- **Mechanical Sound Engine**: Realistic mechanical switch sound feedback (Cherry MX Blue, Brown, Red, Topre, IBM Model M).
- **Focus Guard & Wake-Lock**: Keeps your PC awake during extended builds and automatically pauses when VS Code loses focus.

---

## Global Hotkeys

- `F8`: Pause / Resume build or typing session
- `F9` or `Esc`: Emergency stop (releases Shift/modifier keys immediately)

---

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for full release history.
