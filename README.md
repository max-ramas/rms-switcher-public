<div align="center">

# RMS Switcher

**One menu-bar tool for macOS: smart keyboard-layout switcher, command bar, clipboard manager, screenshots with OCR, floating multilingual input and a file tray.**

![Platform](https://img.shields.io/badge/macOS-14%2B-lightgrey) ![Apple Silicon](https://img.shields.io/badge/Apple%20Silicon-arm64-lightgrey) ![License](https://img.shields.io/badge/license-commercial-lightgrey)

</div>

This repository hosts the **downloads** for RMS Switcher. Source code is not published here.

## Download

Get the latest `RMSSwitcher.zip` from [Releases](../../releases/latest), unzip it and move
**RMSSwitcher.app** to `/Applications`.

> **First launch:** builds are signed but not yet notarized by Apple, so macOS may refuse to open
> the app. Right-click **RMSSwitcher.app → Open** (once), or run
> `xattr -dr com.apple.quarantine /Applications/RMSSwitcher.app`.

Requirements: Apple Silicon Mac, macOS 14 (Sonoma) or newer. The app asks for **Accessibility**
(layout switching) and **Screen Recording** (screenshots) on first use.

## What it does

- **Layout switcher** — fixes text typed in the wrong layout (RU, EN, UK automatically; KA, HY, TR,
  HE, AR by key map and dictionaries), Double Shift, undo, `[RU]` indicator at the caret.
- **Command bar** (`⌥ Space`) — launcher, files, process killer, calculator and unit/currency
  conversion, Ask AI.
- **Clipboard manager** — searchable history, encrypted text, snippets, plain-text paste, editing.
- **Screenshots** — area / screen / window / scrolling capture with an annotation editor, redaction
  and OCR.
- **Floating multilingual input** — transliteration and diacritic restore into any app.
- **File Tray** — a staging area for files under the notch; drag files in, drag them out later.
- **Mouse wheel direction** — reverse a classic mouse wheel without touching the trackpad.
- Russian and English interface. Your text stays on your Mac unless you choose an AI provider.

## Licensing

Every Mac gets a **free 14-day trial** with full functionality automatically, no card needed.
After that a license key is required. See [LICENSE](LICENSE) for the terms; licensing questions:
[support@rms-ds.com](mailto:support@rms-ds.com).

## Updates

RMS Switcher checks for new versions by itself and installs them from the app on your confirmation
(**Check for updates…** in the tray menu).

## Support

Issues and feature requests: the [Issues](../../issues) tab, or
[support@rms-ds.com](mailto:support@rms-ds.com) · [rms-ds.com](https://rms-ds.com)
