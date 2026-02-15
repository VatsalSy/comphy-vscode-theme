# CoMPhy Color Theme Collection

[![License](https://img.shields.io/github/license/VatsalSy/comphy-vscode-theme)](LICENSE)
[![Download VSIX](https://img.shields.io/badge/download%20VSIX-raw-blue)](https://raw.githubusercontent.com/VatsalSy/comphy-vscode-theme/main/comphy-theme.vsix)
[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/VatsalSy/comphy-vscode-theme/publish.yml?label=publish)](https://github.com/VatsalSy/comphy-vscode-theme/actions)<br>
[![VS Marketplace Downloads](https://img.shields.io/visual-studio-marketplace/d/vatsalsy.comphy-theme?label=VS%20Marketplace)](https://marketplace.visualstudio.com/items?itemName=VatsalSy.comphy-theme)
[![VS Marketplace Rating](https://img.shields.io/visual-studio-marketplace/r/vatsalsy.comphy-theme?label=rating)](https://marketplace.visualstudio.com/items?itemName=VatsalSy.comphy-theme)<br>
[![Open VSX Downloads](https://img.shields.io/open-vsx/dt/vatsalsy/comphy-theme?label=Open%20VSX)](https://open-vsx.org/extension/vatsalsy/comphy-theme)<br>

A collection of high-contrast VSCode themes based on the Gruvbox color scheme, optimized for clarity, readability, and enhanced language support.

## Acknowledgment

This theme collection is based on the excellent [Gruvbox Theme by jdinhify](https://github.com/jdinhify/vscode-theme-gruvbox). The original theme provided a solid foundation for building these customized variants. The Anysphere variants are inspired by the Cursor Dark Anysphere theme.

## Changes from Original Theme

- Higher contrast between background and foreground colors
- Modified semantic token colors for better readability
- Enhanced syntax highlighting for modern language features
- Adjusted UI element colors for clearer visual hierarchy
- Optimized terminal colors for better visibility
- Refined bracket pair colorization
- Added comprehensive LaTeX support with specialized syntax highlighting (all variants)

## Features

- High contrast theme based on Gruvbox Dark
- Clear, non-hazy foreground colors
- Optimized syntax highlighting for multiple languages
- Consistent UI elements
- Semantic token coloring support

## Installation

### From VSCode Marketplace

1. Open VSCode
2. Go to Extensions (Ctrl+Shift+X / Cmd+Shift+X)
3. Search for "CoMPhy Color Theme Collection"
4. Click Install

### From Source (VSIX)

1. Clone the repository: `git clone https://github.com/VatsalSy/comphy-vscode-theme.git`
2. Build the VSIX package: `./scripts/build.sh --package`
3. Open VSCode
4. Go to Extensions (Ctrl+Shift+X / Cmd+Shift+X)
5. Click "Install from VSIX..."
6. Select the generated `.vsix` file from the repository root

## Building from Source

### Prerequisites

- Node.js (v14 or higher)
- npm (comes with Node.js)

### Build Process

1. Clone the repository:

   ```bash
   git clone https://github.com/VatsalSy/comphy-vscode-theme.git
   cd comphy-vscode-theme
   ```

2. Run the build script:

   ```bash
   ./scripts/build.sh
   ```

   This will:
   - Check for required dependencies
   - Generate theme JSON files from base configurations
   - List all generated themes

3. To create a `.vsix` package for distribution:

   ```bash
   ./scripts/build.sh --package
   ```

   This will additionally:
   - Package the extension into a `.vsix` file
   - Display the package size and filename

### Manual Build Steps

If you prefer to run the build steps manually:

1. Generate theme files:

   ```bash
   npm run build
   # or
   node scripts/build-themes.js
   ```

2. Package the extension (requires VSCE):

   ```bash
   npm install -g @vscode/vsce
   npx @vscode/vsce package
   ```

### Development

To test your changes locally:
1. Open the project in VSCode
2. Press `F5` to launch the Extension Development Host
3. The extension will be loaded in a new VSCode window for testing

## Theme Variants

This collection includes four variants of the Gruvbox Dark theme:

1. **CoMPhy Gruvbox (High Contrast)** - Uses a dark Gruvbox background (`#1d2021`) for strong readability with classic Gruvbox accents
2. **CoMPhy Gruvbox (Soft)** - Uses a softer Gruvbox background (`#32302f`) for reduced eye strain in long sessions
3. **CoMPhy Gruvbox Anysphere (High Contrast)** - Uses a darker Anysphere-style background (`#141414`) with modern purple accents
4. **CoMPhy Gruvbox Anysphere (Highest Contrast, pop)** - Uses pure black (`#000000`) and a vibrant pop palette for maximum visual impact

All variants maintain the same high-quality syntax highlighting and specialized language support (including TeX/LaTeX), differing in their background intensity and color schemes.

## CoMPhy Gruvbox Anysphere (High Contrast)

The **Anysphere (High Contrast)** variant combines Gruvbox token structure with a darker, modern UI surface:

- **Darker UI Foundation**: Uses `#141414` editor/sidebar surfaces and `#0d0d0d` activity bar for stronger contrast than classic Gruvbox backgrounds
- **Purple-led Accent System**: Uses `#a35db0` for focus, tabs, links, and type-related tokens
- **Consistent Navigation Cues**: Keeps active tab/panel borders and hover states visually prominent without going full pure-black

## CoMPhy Gruvbox Anysphere (Highest Contrast, pop)

Note: this variant intentionally diverges from the classic Gruvbox palette — see the full variant docs at docs/highest-contrast-version.md.

The **Highest Contrast, pop** variant is designed for maximum visual impact and monitors requiring extreme contrast:

- **Pure Black Background**: Uses true black (#000000) for the editor to achieve maximum contrast
- **Vibrant "Pop" Colors**: Features a Dracula-inspired palette with highly saturated, distinctive colors:
  - Comments: #6272a4 (muted blue-gray for reduced distraction)
  - Strings: #50fa7b (bright green)
  - Keywords: #f1fa8c (pale yellow)
  - Functions: #ff79c6 (hot pink)
  - Numbers: #bd93f9 (bright purple)
  - Types: #8be9fd (bright cyan)
- **Visual Hierarchy**: Subtle variation with sidebars using #0a0a0a while editor remains pure black
- **Enhanced Navigation**: Includes hover highlights for better code exploration

**Note**: This variant uses pure black (#000000) specifically for monitors that need extreme contrast and maximum "pop" effect. Some users may find pure black causes eye strain on OLED displays - in such cases, consider using the standard High Contrast variants instead.

## Color Palette (Original Gruvbox Variants)

The traditional variants use the following Gruvbox colors:

- Background: #1d2021 (Dark0 Hard)
- Foreground: #ebdbb2 (Light1)
- Red: #fb4934
- Green: #b8bb26
- Yellow: #fabd2f
- Blue: #83a598
- Purple: #d3869b
- Aqua: #8ec07c
- Orange: #fe8019

## Language Support

Enhanced syntax highlighting for:
- Python
- JavaScript/TypeScript
- Java
- C/C++
- Go
- HTML/CSS
- JSON
- Markdown
- Shell scripts
- LaTeX/TeX (with specialized math, environment, and reference highlighting in all theme variants)
- And more...

## Customization

To customize the theme, you can override settings in your `settings.json`:

```json
{
  "workbench.colorCustomizations": {
    "[CoMPhy Gruvbox (High Contrast)]": {
      // Add your customizations here
    },
    "[CoMPhy Gruvbox Anysphere (High Contrast)]": {
      // Add your customizations here
    }
  }
}
```

## Changelog

For the complete changelog with detailed version history, see [CHANGELOG.md](CHANGELOG.md).

## Contributing

Feel free to open issues or submit pull requests on GitHub.

## Color Palette Reference

For the full palettes and contrast guidelines, see docs/color-palette.md.

## License

MIT License - see LICENSE file for details.
