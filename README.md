# aPaste

English | [简体中文](README.zh-CN.md)

### Your clipboard history, one shortcut away.

[![macOS](https://img.shields.io/badge/macOS-15%2B-black?logo=apple&logoColor=white)](https://github.com/AlliotTech/aPaste/releases/latest)
[![GitHub release](https://img.shields.io/github/v/release/AlliotTech/aPaste?color=blue)](https://github.com/AlliotTech/aPaste/releases/latest)

aPaste is a fast, keyboard-first clipboard manager for macOS. Open a focused panel, search your saved clipboard history, keep important snippets on Pinboards, and paste back into your workflow without breaking focus.

[Download Latest Release](https://github.com/AlliotTech/aPaste/releases/latest) · [Install with Homebrew](#homebrew) · [Website](https://apaste.alliot.tech/)

`Instant recall` · `Pinboards for snippets` · `Private by default` · `Menu bar only` · `Built for macOS`

```bash
brew tap alliottech/tap
brew install --cask alliottech/tap/apaste
xattr -dr com.apple.quarantine /Applications/aPaste.app
```

| Dark | Light |
|:---:|:---:|
| ![aPaste framed screenshot in dark mode](screenshot/liquid-dark_framed.png) | ![aPaste framed screenshot in light mode](screenshot/liquid-light_framed.png) |

One shortcut opens your saved clipboard history with rich previews, fast search, and Pinboards that stay available whenever you need them.

## Why aPaste

- **Find saved items instantly** — Browse your clipboard history in a focused panel built for fast scanning, search filters, and quick paste-back
- **Keep what matters** — Save recurring snippets, links, and assets to pinboards instead of losing them in a long history
- **Stay in flow** — Navigate, search, and paste without touching the mouse
- **Present safely** — Ignore sensitive apps by default, and switch on screenshot hiding when you need it
- **Sync on your terms** — Optionally sync through a shared folder you choose, with opt-in end-to-end encryption
- **Feel native on macOS** — Menu bar app, no Dock icon, no clutter, no friction

## Features

- **Automatic clipboard history** — Capture supported clipboard content while respecting ignored apps and confidential or transient content markers
- **Pinboards** — Save snippets to color-coded boards, always one shortcut away, never auto-deleted
- **Rich previews** — Captured content types are text, links, images, and files; text items additionally get rich-text and colour previews
- **Instant search** — Search as you type, then narrow by type, date, or source app
- **Privacy controls** — Ignore specific apps and skip transient/confidential pasteboard content by default; hiding contents from screenshots is an opt-in setting that is off until you enable it
- **Smart Capture Rules** — Ignore or automatically pin new captures by content type, source app, text, URL host, file extension, or captured byte range
- **Quick Actions** — Nine transforms in the card right-click menu: Trim Whitespace, Convert to Uppercase, Convert to Lowercase, Convert to One Line, Pretty-print JSON, Minify JSON, Remove Tracking Parameters, Copy as Markdown Link, Copy Recognized Text
- **Folder sync** — Sync history and pinboards through any shared folder you pick. aPaste talks to the folder only; if that folder happens to sit inside iCloud Drive, Dropbox, or a Syncthing share, those tools move the files. End-to-end encryption is optional and requires a passphrase you set (PBKDF2-SHA256 + ChaCha20-Poly1305)
- **aPaste Stack** — Collect several items, then paste them back in order
- **Content editor** — Edit text, rich text, or images before pasting
- **Two panel layouts** — Choose the Bottom panel or the Command Center layout
- **History retention** — Set a retention policy, or erase the entire history in one click
- **Pause capture** — Temporarily stop recording the clipboard
- **Image text recognition** — Toggle OCR for captured images
- **Capture-rule tooling** — Test rules against sample content and review an activity log of what they matched
- **Discreet menu bar** — Optionally hide the menu bar icon
- **Drag-and-drop export** — Drag cards out of the panel to export their contents
- **Stays out of the way** — No Dock icon. No splash screen. Optional launch at login

## Screenshots

### Panel

![aPaste panel in dark mode](screenshot/no-liquid-dark-apaste-panel.png)
![aPaste panel in light mode](screenshot/no-liquid-light-apaste-panel.png)

### Liquid Glass

![aPaste liquid glass dark mode](screenshot/liquid-dark.png)
![aPaste liquid glass light mode](screenshot/liquid-light.png)
![aPaste liquid glass with colorful preview](screenshot/liquid-dark-preview-color.png)
![aPaste liquid glass link preview](screenshot/liquid-preview-link.png)

### Standard

![aPaste standard dark mode](screenshot/no-liquid-dark.png)
![aPaste standard light mode](screenshot/no-liquid-light.png)

## Keyboard Shortcuts

Most command shortcuts are customizable in Settings → Shortcuts; fixed panel navigation shortcuts are listed for reference.

| Action | Default |
|:---|:---|
| Toggle panel | `⌃ + Backtick` |
| Activate aPaste Stack | `⌘ ⇧ C` |
| Next Pinboard | `⌘ →` |
| Previous Pinboard | `⌘ ←` |
| Create Pinboard | `⌘ ⇧ N` |
| Toggle search | `⌘ F` |
| Jump to source context | `⌘ G` |
| Copy and close | `⌘ C` |
| Select all cards | `⌘ A` |
| Undo delete | `⌘ Z` |
| Open Settings | `⌘ ,` |
| Paste selected item | `↩` |
| Search history | Type anything |
| Navigate items | `← ↑ ↓ →` |
| Close panel | `Esc` |

## Install

### Homebrew

```bash
brew tap alliottech/tap
brew install --cask alliottech/tap/apaste
xattr -dr com.apple.quarantine /Applications/aPaste.app
```

### Manual

Each release ships **two separate single-architecture DMGs** — `aPaste-v<version>-arm64.dmg` for Apple Silicon and `aPaste-v<version>-x86_64.dmg` for Intel. There is no universal binary, so download the one that matches your chip. To check, open the Apple menu → About This Mac and look at the chip or processor line.

Download the matching DMG from [Releases](https://github.com/AlliotTech/aPaste/releases/latest), drag `aPaste.app` to `/Applications`, then remove the quarantine flag:

```bash
xattr -dr com.apple.quarantine /Applications/aPaste.app
```

### Why the `xattr` command is needed

aPaste is ad-hoc signed and not notarized by Apple. Gatekeeper therefore refuses to launch it and reports the app as damaged or from an unidentified developer. Removing the quarantine attribute clears that flag, so the app you just downloaded can start.

### Accessibility permission

Pasting into the frontmost app works by simulating ⌘V with a synthetic CGEvent, which macOS only allows for trusted apps. Grant it under System Settings → Privacy & Security → Accessibility. Global shortcuts work without this permission; only paste-back needs it.

## Requirements

macOS 15 or later.
