<div align="center">

# ⌨️ RMS Switcher

**A Swiss-army knife for macOS: one menu-bar icon instead of a pile of small utilities.**

Fixes text typed in the wrong keyboard layout as you type, and puts a command bar, a clipboard manager,
screenshots with OCR, a multilingual input field and a file tray one keystroke away.

[![Release](https://img.shields.io/github/v/release/max-ramas/rms-switcher-public?color=blue)](https://github.com/max-ramas/rms-switcher-public/releases/latest)
![Downloads](https://img.shields.io/github/downloads/max-ramas/rms-switcher-public/total)
[![Platform](https://img.shields.io/badge/macOS-14%2B-lightgrey?logo=apple)](#requirements)
[![Apple Silicon](https://img.shields.io/badge/Apple%20Silicon-native-lightgrey)](#requirements)
[![Trial](https://img.shields.io/badge/free%20trial-14%20days-brightgreen)](#licensing)
[![License](https://img.shields.io/badge/license-commercial-lightgrey)](LICENSE)

[Why](#why-rms-switcher) • [Download](#download) • [Features](#features) • [Hotkeys](#default-hotkeys) • [Privacy](#privacy-and-security) • [Install](#install) • [Licensing](#licensing) • [FAQ](#faq)

</div>

---

> This repository hosts **downloads, release notes and the license** for RMS Switcher.
> The source code is not published.

## Download

<div align="center">

[![Download for macOS](https://img.shields.io/badge/%E2%AC%87%EF%B8%8F%20Download%20for%20macOS-RMSSwitcher.dmg-2ea44f?style=for-the-badge&logo=apple&logoColor=white)](https://update.rms-ds.com/get/rms-switcher?src=readme)

Apple Silicon · macOS 14+ · 14-day free trial · also as [.zip](https://update.rms-ds.com/get/rms-switcher/zip?src=readme) · [all releases](https://github.com/max-ramas/rms-switcher-public/releases)

</div>

---

## Why I built it

For years I used excellent apps: Maccy, Shottr, Raycast, Thaw, MOS, Punto Switcher, caffeinate and
others. Some had all the features I needed, some had too few, and some were clearly overkill. Each
one was fairly large, took memory, and added yet another icon to the menu bar. With the notch on a
MacBook that became a real problem.

So I built a "Swiss-army knife" for macOS that solves all of this in one place: **a single icon and
solid functionality** that makes many familiar tools more convenient. I tried not to break habits
you already have and only to extend them, for example by adding editing to screenshots and to text
in the clipboard history.

I hope you will like it and find it as handy as I do.

## Why RMS Switcher

If you type in more than one language, you know the moment: a whole sentence in `ghbdtn` instead of
`привет`. If you work on a Mac all day, you also keep a clipboard manager, a launcher, a screenshot
tool and a few other helpers running just to get through the day. RMS Switcher is one small app that
does all of it, and does it quietly.

- **One icon instead of a dozen.** Layout switching, launcher, clipboard history, screenshots with an
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

### Everything at a glance

| Area | What it does |
| --- | --- |
| **Layout switcher** | Fixes text typed on the wrong layout, automatically or with Double Shift |
| **Screenshots** | Area, screen, window, delayed and scrolling capture; editor; OCR |
| **Clipboard manager** | Searchable history, pinned items, snippets, plain-text paste, text and image editing |
| **Snippets** | Short triggers that expand into your text, with variables |
| **File Tray** | A drop shelf for files at the top edge of the screen |
| **Mouse wheel inversion** | Reverse a classic mouse wheel without touching the trackpad |
| **Multilingual input** | Floating field with transliteration for 16 languages |
| **Translate and polish** | Selected text, via AI providers or a local model |
| **AI assistant** | Ask AI from the command bar (cloud, local model or Siri) |
| **Launcher** | Apps, files and recents from one command bar |
| **Calculator and currency converter** | Expressions, units and live exchange rates |
| **Process manager** | See CPU usage and quit stuck apps |
| **Caffeinate** | Keep-awake toggle in the tray |
| **Tray organizer** | Hides menu-bar clutter behind a divider (made for notch Macs) |
| **Autocorrect control** | System autocorrect and prediction on or off, per app |
| **Quiet mode** | No sounds, pills or notifications when you need silence |

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
A temporary shelf for files: collect them in one place, then sort them into folders and apps.

- **Open it** by dragging a file to the top edge of the screen (under the notch by default; left or
  right if you prefer), by resting the pointer there (when the tray holds files), with `⌃⌥F`, or from
  the tray menu. A tray opened by a drag closes by itself when the pointer leaves it.
- **Files and folders** are kept as **references, not copies**: the original stays where it is, the
  tray follows renames and moves, remembers the list between restarts, and shows files that were
  deleted as dimmed entries.
- **Select several:** click selects, `⌘`-click adds or removes one, `⇧`-click selects a range, and
  dragging over empty space draws a selection rectangle. A drag carries **every selected file**.
- **Dragging out works like Finder:** the file is **moved** on the same disk and **copied** to another
  disk; hold `⌥` to always **copy**, `⌘⌥` to make an **alias**. A moved file leaves the tray; copies
  and aliases stay so you can place them in the next folder too.
- Right-click for **Open, Show in Finder, Copy paths, Select all, Remove from tray**; double-click
  opens the item. The tray never takes keyboard focus, so selection is by mouse.

### Snippets and text expansion
Type a short trigger in any app and it is replaced on the fly: `@@` becomes your e-mail address,
`;;phone` your phone number, `;;date` today's date. Snippets can contain variables (`{DATE}`,
`{TIME}`, `{YEAR}`), live next to the clipboard history, and can be created, edited and deleted
there. Expansion never touches password fields and can be switched off in Settings.

### Mouse wheel direction
Reverse the **vertical and/or horizontal scrolling of a classic mouse wheel** (Settings → Mouse
wheel) without installing a separate utility. The trackpad and Magic Mouse keep the system
direction.

### Control over macOS autocorrect
Switch the system's gray inline prediction and autocorrect on or off **globally or per app**
(for example off in Terminal and your editor, on in Messages), with *system default / force on /
force off* modes.

### Your own rules and dictionaries
- A list of words the layout switcher must **never** convert.
- Installable **dictionary packs** (updated from rms-ds.com) that improve recognition for more
  languages.
- Per-language control: choose which of your enabled macOS layouts take part in automatic
  switching.

### Menu bar, power and quiet
A **tray organizer** that hides menu-bar clutter behind a divider, a **quiet mode** (no sounds, no
caret pill, no notifications, screenshots go straight to the clipboard), a **keep-awake** toggle,
launch at login, and a language setting (system / Russian / English).

### Your data
- Retention and size limits for the clipboard history, a custom folder for screenshots,
  JSON **export** of history and snippets, and **import** from other clipboard managers.
- A live counter in the tray: characters typed, corrections made, and AI usage with its cost in USD.

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
- Once a day (and after an update) the app tells the license server that an install exists: an
  anonymous device hash, the app version and the update channel. Nothing about your text, files or
  clipboard is sent, and the license key itself never leaves your Mac.
- AI features contact the provider you choose, with your own key, and only when you use them.

## Requirements

- A Mac with **Apple Silicon** (M1 or newer).
- **macOS 14 Sonoma** or newer.
- Permissions, requested when needed: **Accessibility** (layout switching and text replacement),
  **Screen Recording** (screenshots and OCR); optional: Full Disk Access (importing another clipboard
  manager), Contacts and Notes (only when you press the matching button).

## Install

1. Download **[RMSSwitcher.dmg](https://update.rms-ds.com/get/rms-switcher?src=readme)**
   (the same app is also available as [`RMSSwitcher.zip`](https://update.rms-ds.com/get/rms-switcher/zip?src=readme)).
2. Open the DMG and drag **RMSSwitcher** onto the **Applications** folder (or unzip the zip and move
   the app there yourself).
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
card. After the trial, a license is required.

| Plan | Price | Per month |
| --- | --- | --- |
| 1 month | €5 | €5.00 |
| 3 months | €12 | €4.00 |
| 6 months | €20 | €3.33 |
| **12 months** | **€30** | **€2.50** |

**How to buy:** sign in (or register) at the
[RMS license shop](https://license.rms-ds.com/dashboard/shop), choose **RMS Switcher** and pay. Your
license key appears in your dashboard. In the app open **Tray → Activate license…** (or
*About → License…*) and paste it. The same buttons are in the app: **Buy a license…** opens the shop.

The license terms are in [LICENSE](LICENSE). Licensing questions:
[support@rms-ds.com](mailto:support@rms-ds.com).

## FAQ

**Does it work offline?** Yes. The license is verified online from time to time and stays valid
offline for the period shown in the license; everything except AI features and updates works without
a connection.

**Does it work with Intel Macs?** No — Apple Silicon only.

**Will it change text in my password manager or terminal?** Secure fields are skipped, and you can
add any app to the blacklist in Settings. Automatic switching happens only when you finish a word.

**What happens when the trial ends?** The features are switched off until you buy a license or enter
a key; the tray menu, settings, updates and the purchase buttons stay available. Your data and
settings are never deleted, and nothing is recorded in the meantime.

**Why is the app not notarized?** Notarization requires an Apple Developer ID, which is planned. Until
then the first launch needs the right-click → Open step above.

## Support

Questions, bug reports and feature requests: open an [issue](../../issues) or write to
[support@rms-ds.com](mailto:support@rms-ds.com) · [rms-ds.com](https://rms-ds.com)

<div align="center">

© RMS Digital Services

</div>
