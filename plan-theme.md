# Suwon Midnight Theme Plan

## Overview
Suwon Midnight is a fork of Tokyo Night theme with a teal color scheme replacing the original sky blue accents.

## Core Colors
- Primary teal: `#4db6ac` (rgb: 77, 182, 172)
- Secondary teal: `#26a69a` (rgb: 38, 166, 154)
- Background: `#1c1f26` (blue-grey slate for better teal contrast)

## Current Implementation Status

### ✅ Completed Components
- **hyprland.conf**: Active border with teal gradient
- **alacritty.toml**: Terminal colors updated to teal scheme
- **btop.theme**: System monitor highlights in teal
- **hyprlock.conf**: Lock screen check color in teal
- **mako.ini**: Notification borders in teal
- **walker.css**: App launcher selection and borders in teal
- **swayosd.css**: OSD borders in teal

### 🔄 Potential Future Updates
- **neovim.lua**: Syntax highlighting theme adjustments
- **icons.theme**: Icon accent colors (if applicable)
- **backgrounds/**: Consider teal-tinted wallpaper variants

## Color Usage Guidelines

### Primary Use Cases for `#4db6ac`
- Selection backgrounds
- Primary borders
- Highlight elements
- Active states

### Secondary Use Cases for `#26a69a`
- Bright variants
- Hover states
- Secondary accents

### Consistency Rules
1. All interactive elements should use teal accents
2. Use consistent blue-grey background (`#1c1f26`) across all components
3. Keep original text colors for readability
4. Use teal gradients where appropriate (borders, progress bars)

## Maintenance Notes
- When adding new components, reference existing teal values
- Test color contrast for accessibility
- Maintain consistency across all configuration files
- Consider both light and dark variants of teal for different contexts