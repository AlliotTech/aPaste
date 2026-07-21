# aPaste

### Your clipboard history, one shortcut away.

[![macOS](https://img.shields.io/badge/macOS-15%2B-black?logo=apple&logoColor=white)](https://github.com/AlliotTech/aPaste/releases/latest)
[![GitHub release](https://img.shields.io/github/v/release/AlliotTech/aPaste?color=blue)](https://github.com/AlliotTech/aPaste/releases/latest)

aPaste is a fast, keyboard-first clipboard manager for macOS. Open a focused panel, search your saved clipboard history, keep important snippets on Pinboards, and paste back into your workflow without breaking focus.

[Download Latest Release](https://github.com/AlliotTech/aPaste/releases/latest) · [Install with Homebrew](#homebrew)

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
- **Present safely** — Ignore sensitive apps and hide preview contents when you need privacy
- **Sync on your terms** — Optionally sync via a folder you control, with end-to-end encryption support
- **Feel native on macOS** — Menu bar app, no Dock icon, no clutter, no friction

## Features

- **Automatic clipboard history** — Capture supported clipboard content while respecting ignored apps and confidential or transient content markers
- **Pinboards** — Save snippets to color-coded boards, always one shortcut away, never auto-deleted
- **Rich previews** — Styled text, links, colors, images, and files render as scannable cards
- **Instant search** — Search as you type, then narrow by type, date, or source app
- **Privacy controls** — Ignore specific apps, skip transient/confidential pasteboard content, hide contents from screenshots
- **Smart Capture Rules** — Ignore or automatically pin new captures by content type, source app, text, URL host, file extension, or captured byte range
- **Quick Actions** — Transform text, format JSON, clean links, create Markdown links, or copy recognized image text
- **Folder sync** — Sync history and pinboards through Syncthing, Dropbox, iCloud Drive, or any shared folder
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

Download the [latest architecture-matched DMG](https://github.com/AlliotTech/aPaste/releases/latest), drag `aPaste.app` to `/Applications`, then remove the quarantine flag:

```bash
xattr -dr com.apple.quarantine /Applications/aPaste.app
```

## Requirements

macOS 15 or later.
