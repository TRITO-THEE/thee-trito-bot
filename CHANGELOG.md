# Changelog

All notable changes to **thee_trito bot** will be documented in this file.

## [1.6.1] - 2026-11-28

### Added
- **Excel Studio Step 2 `Choose Folder` Target Picker**: Added a **`Choose Folder`** button beside **`Save As .xlsx...`** to select an output folder and automatically generate `<folder>/<source_stem>_output.xlsx` (or `thee_trito_workbook.xlsx` before picking a source), with sticky `last_excel_target_dir` persistence across source workbook switches.

### Fixed
- **Live Microsoft Excel Cell Typing**: Fixed cell selection and edit-mode pacing inside `write_cell_live_human()` so characters and Excel formulas visibly type into Excel cells, commit cleanly with `Enter`, light up the Keyboard HUD, and self-heal via COM (`.formula2` / `.value`) with `[Excel Self-Heal]` logging when needed.
- **Instant `XLMAIN` Excel Focus Guard**: Upgraded `is_excel_focused()` on Windows via `win32gui` (`XLMAIN` window class detection and browser/editor/bot exclusions) so switching out of Excel immediately pauses typing and updates the badge to **`Paused — Waiting for Excel`** without stealing focus back.

## [1.6.0] - 2026-11-27

### Added
- **Excel Studio Mode (`Live Microsoft Excel COM` + `Fast Headless openpyxl`)**: Added a dedicated emerald-accented Excel Studio workspace with Sheet Queue preview, Excel Settings card, COM busy/Edit-Mode auto-retry (`RPC_E_CALL_REJECTED`), self-healing formula checks via `.formula2`, isolated `excel_manifest.json` & `excel_session_state.json` resume checkpoints, and CLI flags (`--excel-source`, `--excel-target`, `--excel-mode`, `--excel-dry-run`).
- **7 Built-In Enterprise Excel Workbooks**: Added ready-to-run 3-sheet models with formulas, styling, freeze panes, and charts (`corporate_cashflow_model`, `sales_inventory_dashboard`, `student_analytics_gradebook`, `loan_amortization_model`, `accounting_ledger_statements`, `hr_payroll_register`, `project_budget_tracker`) with optional continuous loop.
- **PC Setup Wizard Excel Detection**: Added informational `Microsoft Excel Desktop (Excel Studio)` diagnostics row (`Ready (Live COM + openpyxl)` vs `Headless Mode Only`).

### Fixed
- **Zero Mid-Run Focus Stealing (VS Code & Excel)**: Added passive `wait_until_vscode_focused()` and `wait_until_excel_focused()` polling before periodic self-heal checks, auto-saves (`Ctrl+S`), cursor re-anchoring, next-file opens, folder creation, editor cleanup, and live Excel COM cell writes. Switching to Chrome/Explorer/Notepad now pauses quietly without pulling focus away, and physical inputs in other apps are ignored by `UserInterferenceMonitor`.

## [1.5.0] - 2026-11-26

### Added
- **Smart Check-First PC Setup Wizard & 1-Click VS Code Auto-Installer**: Verifies bundled `PySide6`, `pynput`, `pyautogui`, `pywinctl`, `wakepy`, `%APPDATA%` storage, existing VS Code installs, and `code --version` before any action. Never offers reinstallation when VS Code already exists, adds 1-click **Fix VS Code PATH** (`HKCU\Environment`), and supports WinGet + official Microsoft direct download fallback (`VSCodeUserSetup.exe`) when VS Code is genuinely missing.
- **Automatic VS Code Launch & Focus on Start**: Clicking **Start Build**, **Resume Saved Session**, or **Start Typing** automatically launches VS Code (`code --disable-workspace-trust -n <target_dir>` or `code -n`) and focuses it if not open yet, or opens the Setup Wizard automatically if VS Code is missing.

## [1.4.0] - 2026-11-26

### Added
- **Built-In Starter Projects & Snippets Library**: Added 4 built-in multi-file starter projects and built-in single-file starter scripts accessible right from the dashboard.
- **Continuous Built-In Loop (`Loop continuously`)**: Built-In Projects and Built-In Snippets automatically pause, clear their own typed output in VS Code, and restart continuously until stopped (`F9`, `Esc`, or **Stop**). Custom user folders and files never auto-clear.

## [1.3.2] - 2026-11-26

### Added
- **Windows Setup Wizard (`thee_trito_bot_Setup.exe`)**: Inno Setup 7 installer (`WizardStyle=modern dynamic`, non-admin per-user install, Desktop shortcut task, Start with Windows task, Start Menu integration, and clean Add/Remove Programs uninstaller).
- **Fast `--onedir` App Launch**: Switched packaging from `--onefile` to `--onedir` for near-instantaneous startup.
- **Persistent `%APPDATA%` Config Storage**: Moved frozen config storage to `%APPDATA%\thee_trito_bot\config` with automatic non-destructive migration from legacy portable `config/` folders.
- **Hide to System Tray UX**: Added `Hide to Tray` sidebar button, `Hide to System Tray on Close` preference toggle (default ON), single/double-click restore, one-time tray notice, and clean `Quit thee_trito bot` shutdown.
- **Installer-Aware Silent Self-Updater**: `check_for_update()` prefers `*_Setup.exe` assets (`is_installer=True`) and `apply_update_and_restart()` runs silent in-place upgrades and relaunches automatically.

## [1.3.1] - 2026-11-25

### Added
- **3-State Feedback on "Check for Updates"**: Distinguishes clearly between "Update Available", "Up to Date", and "Offline / Network Error" with `"Checking..."` button feedback and informative dialogs.
- **Silent Startup Checks**: Automatic startup checks stay silent unless a newer release is available.

## [1.3.0] - 2026-11-25

### Added
- **Solid Dark-Graphite PySide6 Qt6 Desktop UI**: High-performance native Qt6 interface with `Fusion` styling, zero translucency/glass latency, and floating real-time QWERTY HUD.
- **Built-in 1-Click Auto-Updater**: Automatic background release checks against GitHub Releases API.
- **Self-Healing VS Code Editor & Cursor-Anchor Guard**: Actively monitors cursor drift, focus loss, and stray keystrokes.
- **Visual VS Code Explorer Mode**: Human-like Explorer navigation with silent direct filesystem fallback.
- **Human Typing Rhythm & Mechanical Audio**: 15–60 WPM flow-wave pacing, typo correction simulation, Focus Guard, and Wake-Lock.

## [1.0.0] - 2026-11-24

### Added
- Initial standalone release of `thee_trito_bot.exe`.
