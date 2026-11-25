# Changelog

All notable changes to **thee_trito bot** will be documented in this file.

## [1.3.1] - 2026-11-25

### Added
- **3-State Feedback on "Check for Updates"**:
  - Distinguishes clearly between "Update Available", "Up to Date", and "Offline / Network Error".
  - Button switches to `"Checking..."` and temporarily disables while background thread checks GitHub.
  - Informative dark-graphite dialogs for up-to-date and offline states, plus 1-click update prompt when an update is available.
- **Silent Startup Checks**: Automatic startup checks run silently in the background and only present the notification banner if a newer release actually exists.
- **3-State Verification Test Suite**: Automated unit tests for all 3 updater states.

## [1.3.0] - 2026-11-25

### Added
- **Solid Dark-Graphite PySide6 Qt6 Desktop UI**: High-performance native Qt6 interface with `Fusion` styling, zero translucency/glass latency, and an independent floating real-time QWERTY HUD.
- **Built-in 1-Click Auto-Updater**: Automatic background release checks against GitHub Releases API with notification banners and detached process executable replacement.
- **Self-Healing VS Code Editor & Cursor-Anchor Guard**: Actively monitors cursor drift, focus loss, and stray keystrokes; self-heals brackets and indentation automatically.
- **Visual VS Code Explorer Mode**: Smooth human-like mouse movement (`pyautogui.easeOutQuad`) to the Explorer sidebar for native folder/file creation with silent direct filesystem fallback.
- **Human Typing Rhythm**: 15–60 WPM speed curve with flow-wave pacing, simulated typing errors with realistic backspace corrections, and customizable speed profiles.
- **Mechanical Key Audio Engine**: Real mechanical switch sound effects for every keystroke.
- **Focus Guard & Wake-Lock**: Ensures typing only occurs when VS Code is the active window, and prevents Windows from sleeping during multi-hour builds.

## [1.0.0] - 2026-11-24

### Added
- Initial standalone release of `thee_trito_bot.exe`.
