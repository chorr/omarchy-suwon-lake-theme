# Suwon Lake Theme

Custom dark theme for Omarchy desktop, based on Tokyo Night.

## Design Concept

- **Dark theme** base (background: `#1c1f26`)
- **Teal + Orange** two-tone color concept
  - Primary: Teal (`#5ec4b8`) - accent, highlights, selection
  - Secondary: Muted Orange (`#d4956a`) - cursor, titles, graph mid-point
- Teal visibility against dark background is the top priority

## Color Palette

| Role | Color | Hex |
|------|-------|-----|
| Primary (teal) | accent, highlights, selection bg | `#5ec4b8` |
| Primary variant | sub teal | `#4fb3b8` |
| Primary dark | bright teal variant | `#33b5a8` |
| Secondary (orange) | cursor, btop titles, graph mid | `#d4956a` |
| Background | base dark | `#1c1f26` |
| Foreground | main text | `#a9b1d6` |

## Color Rules

- **Primary teal for UI emphasis**: accent, selection, keyboard shortcuts, graph start
- **Secondary orange in a subdued tone**: cursor, headings, graph midpoint
- Orange must not overpower teal — keep saturation/brightness restrained
- Terminal ANSI colors (color0-15) orange variants (`#ff9e64`, `#e0af68`) are kept separately for terminal output readability
- Graph gradient: teal → orange → pink (`#5ec4b8` → `#d4956a` → `#f7768e`)

## Theme Files

- `colors.toml` - Terminal/system color definitions (accent, cursor, ANSI colors)
- `btop.theme` - btop system monitor theme
- `neovim.lua` - Neovim colorscheme (tokyonight)
- `vscode.json` - VS Code theme (Tokyo Night Storm)
- `keyboard.rgb` - Keyboard RGB color
- `icons.theme` - Icon theme (Yaru-purple)
- `unlock.png` - Lock-screen shape asset
- `preview-unlock.png` - Lock-screen preview image
- `backgrounds/` - Wallpapers
