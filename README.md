# aPaste

**Everything you've ever copied.**

[![macOS](https://img.shields.io/badge/macOS-13%2B-black?logo=apple&logoColor=white)](https://github.com/AlliotTech/aPaste/releases/latest)
[![GitHub release](https://img.shields.io/github/v/release/AlliotTech/aPaste?color=blue)](https://github.com/AlliotTech/aPaste/releases/latest)
[![License](https://img.shields.io/github/license/AlliotTech/aPaste)](LICENSE)

aPaste is a lightweight, beautiful clipboard manager for macOS. One shortcut, and your full clipboard history appears — text, images, links, files. Find what you need. Paste it. Move on.

## Features                                                                                                  

- **Never lose a copy** — Full clipboard history, captured automatically from every app                      
- **Pinboards** — Save snippets to color-coded boards, always one shortcut away, never auto-deleted
- **Instant search** — Fuzzy search across your entire history as you type
- **Privacy controls** — Ignore specific apps, hide contents from screenshots                                
- **Zero footprint** — No Dock icon. No splash screen. Starts at login. Runs silently
## Keyboard Shortcuts

All shortcuts are customizable in Settings → Shortcuts.

| Action | Default |
|:---|:---|
| Toggle panel | `^ `` ` |
| Activate Paste Stack | `⌘ ⇧ C` |
| Next Pinboard | `⌘ →` |
| Previous Pinboard | `⌘ ←` |
| Create Pinboard | `⌘ ⇧ N` |
| Paste selected item | `↩` |
| Search history | Type anything |
| Navigate items | `← ↑ ↓ →` |
| Close panel | `Esc` |

## Install

### Homebrew

```bash
brew tap alliottech/tap
brew install --cask alliottech/tap/apaste --no-quarantine
```

### Manual

Download the [latest DMG](https://github.com/AlliotTech/aPaste/releases/latest), drag `aPaste.app` to `/Applications`, then remove the quarantine flag:

```bash
xattr -d com.apple.quarantine /Applications/aPaste.app
```

## Requirements

macOS 13 Ventura or later.
