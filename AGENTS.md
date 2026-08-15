# Suwon Lake Theme

Custom dark theme for Omarchy desktop, based on Tokyo Night.

## Design Concept

- **Dark theme** base (background: `#1c1f26`)
- **Teal + Orange** two-tone color concept
  - Primary: Teal (`#5ec4b8`) - accent, highlights, borders
  - Secondary: Muted Orange (`#d4956a`) - titles, graph mid-point
- Teal visibility against dark background is the top priority

## Color Palette

| Role | Color | Hex |
|------|-------|-----|
| Primary (teal) | accent, highlights, `blue` | `#5ec4b8` |
| Primary variant | sub teal | `#4fb3b8` |
| Primary dark | `cyan` | `#3eb8a8` |
| Secondary (orange) | btop titles, graph mid, `orange` | `#d4956a` |
| Selection | muted teal-tinted highlight | `#283d40` |
| Background | base dark | `#1c1f26` |
| Foreground | main text | `#a9b1d6` |

## Color Rules

- **Primary teal for UI emphasis**: accent, borders, keyboard shortcuts, graph start, active/urgent workspaces
- **Secondary orange in a subdued tone**: headings, graph midpoint, semantic `orange`
- Orange must not overpower teal — keep saturation/brightness restrained
- Terminal yellow/bright-yellow stay on the readable orange variants (`#e0af68`, `#ff9e64`)
- Graph gradient: teal → orange → pink (`#5ec4b8` → `#d4956a` → `#f7768e`)
- Omarchy 4.0 maps terminal/editor cursor to `bright_foreground`; do not rely on a `cursor` key

## Theme Files

- `colors.toml` - Omarchy 4.0 semantic palette (source of truth for generated app configs)
- `shell.lock.toml` - Lock-screen chrome override (teal borders, red error)
- `bar/workspaces.qml` - 4.0 bar override: focused/urgent workspace markers use `accent`
- `btop.theme` - btop override to keep the teal → orange → pink graph gradient
- `neovim.lua` - Neovim colorscheme (tokyonight)
- `vscode.json` - VS Code theme (Tokyo Night Storm)
- `keyboard.rgb` - Keyboard RGB color
- `icons.theme` - Icon theme (Yaru-purple)
- `unlock.png` - Lock-screen shape asset
- `preview-unlock.png` - Lock-screen preview image
- `backgrounds/` - Wallpapers

## Local Development

Omarchy 4.0 copies the theme into `~/.local/state/omarchy/current/theme` and generates app configs from `colors.toml`. After editing theme files, run `omarchy theme refresh` (or `omarchy theme set <name>`). Saving a file is not enough.

A symlink from `~/.config/omarchy/themes/<name>` to a working copy is enough for iteration. `omarchy theme update` skips symlinks.

`bar/workspaces.qml` is a custom bar widget. To use it, point the `omarchy.workspaces` entry in `~/.config/omarchy/shell.json` at that file with `type = "qml"`.

## Public Repository

This repo is public. Keep committed docs and messages useful to any reader, not just this machine.

- Do not commit host-specific paths, clone names, or "this machine" setup (for example a local `suwon-lake-dev` symlink next to an installed clone)
- Describe workflows in generic terms so they apply to anyone installing or developing the theme
- Commit messages follow the existing English history; do not mention local checkout layout or unpublished machine state
