<div align="center">

# ⌨️ RMS Switcher

**The macOS menu-bar toolbox that replaces six small utilities with one fast, native app.**

Fixes text typed in the wrong keyboard layout as you type, and puts a command bar, a clipboard manager,
screenshots with OCR, a multilingual input field and a file tray one keystroke away.

[![Release](https://img.shields.io/github/v/release/max-ramas/rms-switcher-public?color=blue)](https://github.com/max-ramas/rms-switcher-public/releases/latest)
![Downloads](https://img.shields.io/github/downloads/max-ramas/rms-switcher-public/total)
[![Platform](https://img.shields.io/badge/macOS-14%2B-lightgrey?logo=apple)](#requirements)
[![Apple Silicon](https://img.shields.io/badge/Apple%20Silicon-native-lightgrey)](#requirements)
[![Trial](https://img.shields.io/badge/free%20trial-14%20days-brightgreen)](#licensing)
[![License](https://img.shields.io/badge/license-commercial-lightgrey)](LICENSE)

[Why](#why-rms-switcher) • [Download](https://github.com/max-ramas/rms-switcher-public/releases/latest) • [Features](#features) • [Hotkeys](#default-hotkeys) • [Privacy](#privacy-and-security) • [Install](#install) • [Licensing](#licensing) • [FAQ](#faq)

</div>

---

> This repository hosts **downloads, release notes and the license** for RMS Switcher.
> The source code is not published.

## Why RMS Switcher

If you type in more than one language, you know the moment: a whole sentence in `ghbdtn` instead of
`привет`. If you work on a Mac all day, you also keep a clipboard manager, a launcher, a screenshot
tool and a few other helpers running just to get through the day. RMS Switcher is one small app that
does all of it, and does it quietly.

- **One icon instead of six.** Layout switching, launcher, clipboard history, screenshots with an
  editor and OCR, a floating input field and a file tray share one menu-bar item, one settings
  window and one set of hotkeys.
- **Native and light.** Written in Swift for Apple Silicon, with no third-party packages and no
  embedded browser. It starts instantly and stays out of the way.
- **Private by design.** Your clipboard history and settings live on your Mac. Clipboard text is
  encrypted at rest, API keys are kept in the macOS Keychain, and nothing you type is sent anywhere
  unless you explicitly turn on an AI feature.
- **Careful with your text.** The layout fixer skips passwords, URLs, e-mail addresses, code
  identifiers, ALL-CAPS and names; it works only when you finish a word and can be undone with one
  shortcut.
- **Fully usable from the first minute.** Every Mac gets a free 14-day trial with all features and
  no credit card.

## Features

### Smart layout switcher
- **Automatic fix at the end of a word** for English, Russian and Ukrainian: it recognizes text
  typed on the wrong layout from letter patterns (phonotactics and n-grams), erases it and types
  the right word, then switches the system layout so the next word starts correctly.
- **Manual fix with Double Shift** — converts the selection or the word at the caret in any app,
  including Chromium and Electron apps. Undo with `⌃⌥Z` or by pressing Double Shift on an empty
  field.
- **More languages by key map and dictionaries:** Georgian, Armenian, Turkish, Hebrew and Arabic.
- **Knows when to stay out:** password and secure fields, ALL-CAPS, camelCase, names, a built-in
  list of 300+ developer terms, e-mail addresses, short English words with punctuation (`cab.`,
  `web.`), and apps you add to a blacklist (remote desktop and virtual-machine apps are excluded
  by default).
- **Caret indicator** — a small `[RU]` / `[EN]` pill shows the layout you just switched to.
- Choose which of your enabled macOS layouts take part in automatic switching.

### Command bar — `⌥ Space`
A fast launcher in the Spotlight/Raycast style, without a heavy index of its own:
- apps with recents and frequency ranking, and files found through macOS search;
- **process killer** with live CPU usage (`⌘⇧P`);
- **calculator and converter** (`⌃⌥=`): expressions, units and currencies with automatically
  refreshed exchange rates;
- **Ask AI** (`⌘⇧A`) with a local model, a cloud provider or Siri.

### Clipboard manager — `⌘⇧C`
- Searchable history of text, images and copied files (files are stored as paths), with thumbnails
  and `⌘1`–`⌘9` quick paste.
- **Text is encrypted** (AES-GCM) with a key kept in your Keychain; images stay on your Mac.
- Pinned items, **snippets**, plain-text paste (`⌘⌥V`), Quick Look, and an **editor** for text
  entries (`⌘E`).
- Imports history from other clipboard managers.

### Screenshots with an editor and OCR
- Area (`⌘⇧2`), full screen (`⌘⇧1`), window (`⌘⇧0`), delayed (`⌘⇧9`) and **scrolling** (`⌘⇧8`)
  capture, with a floating thumbnail you can copy, save, pin to the screen or open in the editor.
- **Editor:** arrows, shapes, text, rulers and **irreversible redaction** (pixelation plus blur,
  not a see-through black box); every element stays selectable and editable.
- **OCR** of any screenshot, with QR-code and barcode detection.

### Floating multilingual input — `⌘⇧Space`
A small field that types into any app: transliteration for 16 languages (Turkish, Spanish,
Serbian, Montenegrin, Lithuanian, Latvian, Estonian, Romanian, Moldovan, Russian, Ukrainian,
Georgian, Armenian, Hebrew, Arabic, English) with diacritics restored — handy when an app has no
proper input method.

### AI helpers — optional
Polish a selection (`⌘⇧E`) or translate it (`⌘⌥T`) with OpenAI, Claude, Gemini, DeepL or a local
Ollama / LM Studio model. Nothing is sent until you add your own key or point the app at a local
model.

### File Tray
A staging area for files, in the style of a drop shelf. Drag a file to the top edge of the screen
(under the notch by default; left or right if you prefer) or rest the pointer there, and the tray
slides out. It keeps **references, not copies**, follows files that are renamed or moved, survives
restarts and lets you drag files out again.

### Everything else in the tray
Mouse **wheel direction** reversal for a classic mouse (the trackpad is left alone), a **tray
organizer** that hides menu-bar clutter, a **quiet mode**, a keep-awake toggle, launch at login,
and an autocorrect manager. The interface is available in Russian and English.

## Default hotkeys

All of them can be changed in **Settings** and are tied to physical keys, so they keep working on any
keyboard layout.

| Action | Hotkey |
| --- | --- |
| Command bar | `⌥ Space` |
| Clipboard history | `⌘⇧C` |
| Plain-text paste | `⌘⌥V` |
| Floating multilingual input | `⌘⇧Space` |
| Polish selection / translate selection | `⌘⇧E` / `⌘⌥T` |
| Ask AI / Process killer / Calculator | `⌘⇧A` / `⌘⇧P` / `⌃⌥=` |
| Fix word on the wrong layout | Double `Shift` |
| Undo layout fix | `⌃⌥Z` |
| Screenshot: area / screen / window / delay / scrolling | `⌘⇧2` / `⌘⇧1` / `⌘⇧0` / `⌘⇧9` / `⌘⇧8` |
| File Tray | `⌃⌥F` |

## Privacy and security

- Settings, clipboard history and the file-tray list are stored in
  `~/Library/Application Support/RMSSwitcher/`. Clipboard **text** is encrypted; the key and your
  API keys are stored in the macOS Keychain.
- Password and secure input fields are never read or changed.
- The app talks to two RMS services only: the **license server** (issues the trial, checks the
  license) and the **update server** (looks for new versions). Updates are verified with a
  cryptographic signature before they are installed, and the installer refuses a package signed by a
  different certificate.
- AI features contact the provider you choose, with your own key, and only when you use them.

## Requirements

- A Mac with **Apple Silicon** (M1 or newer).
- **macOS 14 Sonoma** or newer.
- Permissions, requested when needed: **Accessibility** (layout switching and text replacement),
  **Screen Recording** (screenshots and OCR); optional: Full Disk Access (importing another clipboard
  manager), Contacts and Notes (only when you press the matching button).

## Install

1. Download `RMSSwitcher.zip` from the [latest release](https://github.com/max-ramas/rms-switcher-public/releases/latest).
2. Unzip it and move **RMSSwitcher.app** to `/Applications`.
3. Open it. The first launch starts your 14-day trial and shows the permissions guide.

> **Gatekeeper:** builds are signed but not yet notarized by Apple, so macOS may refuse to open the
> app the first time. Right-click **RMSSwitcher.app → Open** (once), or run
> `xattr -dr com.apple.quarantine /Applications/RMSSwitcher.app`.

**Updates:** the app looks for new versions by itself and shows a notice in the tray menu and in
*About*; you decide when to install. **Check for updates…** in the tray menu checks right away. The
update is downloaded, verified, replaces the app and relaunches it, with automatic rollback if the
new version does not start.

**Uninstall:** quit the app, delete `RMSSwitcher.app`, and optionally remove
`~/Library/Application Support/RMSSwitcher/`.

## Licensing

Every Mac gets a **free 14-day trial** with full functionality, automatically and without a credit
card. After that a license key is required; enter it in **Tray → Activate license…** (or in
*About → License…*). The license terms are in [LICENSE](LICENSE).

Paid plans are being finalized. Pricing and the purchase link will appear here and in the app; until
then licensing questions go to [support@rms-ds.com](mailto:support@rms-ds.com).

## FAQ

**Does it work offline?** Yes. The license is verified online from time to time and stays valid
offline for the period shown in the license; everything except AI features and updates works without
a connection.

**Does it work with Intel Macs?** No — Apple Silicon only.

**Will it change text in my password manager or terminal?** Secure fields are skipped, and you can
add any app to the blacklist in Settings. Automatic switching happens only when you finish a word.

**What happens when the trial ends?** The app keeps running but asks for a license key; your data and
settings stay as they are.

**Why is the app not notarized?** Notarization requires an Apple Developer ID, which is planned. Until
then the first launch needs the right-click → Open step above.

## Support

Questions, bug reports and feature requests: open an [issue](../../issues) or write to
[support@rms-ds.com](mailto:support@rms-ds.com) · [rms-ds.com](https://rms-ds.com)

<div align="center">

© RMS Digital Services

</div>
