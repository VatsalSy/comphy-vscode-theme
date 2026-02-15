# CoMPhy Gruvbox Pop Theme

## Overview

**CoMPhy Gruvbox Pop** is the high-intensity variant in this collection. It pairs a pure black background with a warm off-white foreground and saturated accent colors for maximum separation between code elements.

## Design Philosophy

- **Maximum Contrast**: Pure black editor background (`#000000`) with warm off-white text (`#e8e0d4`)
- **High-Visibility Syntax**: Saturated accent palette for fast token recognition
- **Intentional UI Hierarchy**: Near-black UI surfaces to keep focus on code
- **Comfort Tuning**: Pop text softened from pure white to reduce halation in long sessions

## Color Palette

### Base Colors

| Component | Color | Hex | Purpose |
|-----------|-------|-----|---------|
| **Editor Background** | Pure Black | `#000000` | Maximum contrast foundation |
| **Editor Foreground** | Warm Off-White | `#e8e0d4` | High readability with reduced glare |
| **Sidebar / Activity Bar** | Near Black | `#0a0a0a` | Subtle visual hierarchy |
| **Cursor** | Deep Purple | `#9b4fa0` | Visual focus indicator |
| **Selection Background** | Translucent Purple | `#bd93f930` | Highlighted text backdrop |

### Syntax Highlighting Colors

| Element | Color | Hex | Purpose |
|---------|-------|-----|---------|
| **Comments** | Blue-Gray | `#7887ab` | Reduced distraction while staying readable |
| **Strings** | Bright Green | `#50fa7b` | High visibility for string literals |
| **Keywords** | Pale Yellow | `#f1fa8c` | Strong keyword prominence |
| **Functions** | Hot Pink | `#ff79c6` | Distinctive callable symbols |
| **Numbers** | Bright Purple | `#bd93f9` | Numeric constant visibility |
| **Types** | Bright Cyan | `#8be9fd` | Type distinction |
| **Operators** | Orange | `#ffb86c` | Clear operator visibility |
| **Variables** | Soft Off-White | `#e2dcd0` | Neutral body text with hierarchy |
| **Decorators** | Deep Purple | `#9b4fa0` | Annotation highlighting |

### UI Accent Colors

| Element | Color | Hex | Purpose |
|---------|-------|-----|---------|
| **Focus Border** | Bright Purple | `#bd93f9` | Active element indication |
| **Button Background** | Deep Purple | `#9b4fa0` | Interactive element base |
| **Button Hover** | Light Purple | `#a977ff` | Interactive feedback |
| **Progress Bar** | Bright Purple | `#bd93f9` | Progress indication |
| **Text Links** | Bright Purple | `#bd93f9` | Clickable text |
| **Active Line Number** | Orange | `#ffb86c` | Current line indicator |
| **Line Highlight** | Translucent White | `#ffffff0d` | Low-noise row tracking |

### Terminal ANSI Colors

| Color | Normal | Hex | Bright | Hex |
|-------|--------|-----|--------|-----|
| **Black** | Dark Gray | `#212121` | Blue-Gray | `#6272a4` |
| **Red** | Red | `#ff5555` | Bright Red | `#ff6e6e` |
| **Green** | Green | `#50fa7b` | Bright Green | `#69ff94` |
| **Yellow** | Yellow | `#f1fa8c` | Bright Yellow | `#ffffa5` |
| **Blue** | Blue | `#6cb6ff` | Bright Blue | `#79c7ff` |
| **Magenta** | Magenta | `#bd93f9` | Bright Magenta | `#d6acff` |
| **Cyan** | Cyan | `#8be9fd` | Bright Cyan | `#a4ffff` |
| **White** | Light Gray | `#cccccc` | Bright White | `#ffffff` |

## Contrast Ratios

Most color combinations meet or exceed WCAG AA requirements:

- **Primary text on background** (`#e8e0d4` on `#000000`): very high contrast
- **Comment text on background** (`#7887ab` on `#000000`): readable while subdued
- **Accent tokens on background**: designed for quick visual separation

## Usage Recommendations

### Ideal For

- Monitors that benefit from very high contrast
- Bright ambient light environments
- Users who prefer saturated syntax accents
- Extended coding sessions where fast token recognition matters

### Considerations

- Pure black UI can feel intense on some displays
- Saturated accents are intentionally bold and not minimalistic

## Comparison with Shipped Variants

| Aspect | CoMPhy Gruvbox Classic | CoMPhy Gruvbox Pop |
|--------|-------------------------|--------------------|
| **Background** | `#1d2021` | `#000000` |
| **Contrast Level** | High | Maximum |
| **Color Saturation** | Earthy Gruvbox | Vibrant pop |
| **Accent Profile** | Traditional Gruvbox accents | Dracula-inspired accents |
| **Use Case** | Daily balanced coding | Maximum visibility and punch |

## Installation Note

This theme is included in the CoMPhy Color Theme Collection. After installation, choose either **CoMPhy Gruvbox Classic** or **CoMPhy Gruvbox Pop** from the color theme picker in VS Code or Cursor.
