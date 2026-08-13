<p align="center">
  <img src="route23.png" width="112" alt="Route23">
</p>

<h1 align="center">Route23</h1>

<p align="center">A macOS desktop browser with built-in file, image, RSS, and bookmark management.</p>

<p align="center">
  <a href="https://github.com/Route23/r23/releases/latest"><img src="https://img.shields.io/github/v/release/Route23/r23?label=release&color=FFA60B" alt="Latest release"></a>
  <a href="https://github.com/Route23/r23/releases"><img src="https://img.shields.io/github/downloads/Route23/r23/total?label=downloads&color=FFA60B" alt="Downloads"></a>
  <img src="https://img.shields.io/badge/macOS-14%2B%20%C2%B7%20Apple%20Silicon-black?logo=apple" alt="macOS 14+ · Apple Silicon">
</p>

---

This is the **public download & auto-update channel** for Route23. The application source is private; signed builds and update manifests are published here.

## Features

- **Split-pane browsing** with spaces (multiple pane grids)
- **Finder-parity file browser** with an image gallery + lightbox
- **RSS reader** and **bookmarks**
- **Terminal** and **agent** panes
- **Per-host zoom**, secret mode, and more
- **In-app auto-updates** (signed, delta-friendly)

## Install

### Homebrew (recommended)

```sh
brew install --cask Route23/tap/route23
```

Opens right away — the cask clears the quarantine flag on install.

### Manual (.dmg)

1. Download `Route23_<version>_aarch64.dmg` from the [latest release](https://github.com/Route23/r23/releases/latest).
2. Drag **Route23.app** into **Applications**.
3. First launch only — clear the quarantine flag (the app is unsigned):

   ```sh
   xattr -dr com.apple.quarantine /Applications/Route23.app
   ```

   > 未署名のため、手動インストール時は初回だけ上記を実行してから開いてください（Homebrew では不要）。

**Requirements:** macOS 14 (Sonoma) or later · Apple Silicon (arm64).

## Updating

- **In-app:** Settings → About → **Check for Updates**. Updates apply on restart; your tabs and logins are restored.
- **Homebrew:** `brew upgrade --cask route23`.

## What's in a release

| Asset | Purpose |
| --- | --- |
| `Route23_<version>_aarch64.dmg` | Installer for manual download |
| `Route23.app.tar.gz` + `.sig` | Auto-updater artifact (minisign-signed) |
| `latest.json` | Updater manifest (`releases/latest/download/latest.json`) |

## Notes

- Builds are **unsigned / not notarized** (free distribution). Homebrew installs open directly; a manual `.dmg` needs the one-time `xattr` command above.
- This repository hosts distribution only — the source code is private.

---

<p align="center"><sub>© 2026 Coordinate-Cat. All rights reserved.</sub></p>
