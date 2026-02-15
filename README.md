# CoMPhy Color Theme Collection

[![License](https://img.shields.io/github/license/VatsalSy/comphy-vscode-theme)](LICENSE)
[![Download VSIX](https://img.shields.io/badge/download%20VSIX-raw-blue)](https://raw.githubusercontent.com/VatsalSy/comphy-vscode-theme/main/comphy-theme.vsix)
[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/VatsalSy/comphy-vscode-theme/publish.yml?label=publish)](https://github.com/VatsalSy/comphy-vscode-theme/actions)<br>
[![VS Marketplace Downloads](https://img.shields.io/visual-studio-marketplace/d/vatsalsy.comphy-theme?label=VS%20Marketplace)](https://marketplace.visualstudio.com/items?itemName=VatsalSy.comphy-theme)
[![VS Marketplace Rating](https://img.shields.io/visual-studio-marketplace/r/vatsalsy.comphy-theme?label=rating)](https://marketplace.visualstudio.com/items?itemName=VatsalSy.comphy-theme)<br>
[![Open VSX Downloads](https://img.shields.io/open-vsx/dt/vatsalsy/comphy-theme?label=Open%20VSX)](https://open-vsx.org/extension/vatsalsy/comphy-theme)<br>

Two flagship dark themes based on Gruvbox, built for long coding sessions in Python, C, and LaTeX.

## Acknowledgment

This theme collection is based on the excellent [Gruvbox Theme by jdinhify](https://github.com/jdinhify/vscode-theme-gruvbox). The Pop variant draws inspiration from the Cursor Dark Anysphere and Dracula palettes.

## Theme Variants

### CoMPhy Gruvbox Classic

Traditional Gruvbox dark with `#1d2021` background. Warm, familiar palette optimized for readability with properly differentiated terminal bright colors and WCAG-aware comment contrast.

### CoMPhy Gruvbox Pop

Pure black (`#000000`) background with a vibrant Dracula-inspired syntax palette. Designed for maximum visual impact and all-day comfort:

- Warm off-white foreground (`#e8e0d4`) to reduce halation
- Hot pink functions, bright green strings, pale yellow keywords
- Purple/cyan type system, muted blue-gray comments
- Subtle line highlighting visible on pure black

## Features

- Dedicated C/C++ syntax scopes (preprocessor, macros, structs, pointers, sizeof)
- Markdown heading hierarchy (H1-H6 warm-to-cool color gradient)
- Enhanced Shell scripting (pipes, redirects, heredocs, builtins)
- CSS/SCSS support (IDs, pseudo-classes, variables, units, !important)
- Python enhancements (docstrings, exceptions, logical operators)
- Regex highlighting (patterns, character classes, quantifiers, anchors)
- ~30 semantic token definitions including Python-specific tokens
- Comprehensive LaTeX support (math mode, citations, sections)
- UI polish: sticky scroll, breadcrumbs, notifications, diff editor, inlay hints

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

## Color Palettes

### Classic (Gruvbox)

- Background: #1d2021 (Dark0 Hard)
- Foreground: #ebdbb2 (Light1)
- Red: #fb4934, Green: #b8bb26, Yellow: #fabd2f
- Blue: #83a598, Purple: #d3869b, Aqua: #8ec07c, Orange: #fe8019

### Pop (Dracula-inspired)

- Background: #000000, Foreground: #e8e0d4
- Functions: #ff79c6, Strings: #50fa7b, Keywords: #f1fa8c
- Numbers: #bd93f9, Types: #8be9fd, Comments: #7887ab, Operators: #ffb86c

## Language Support

Enhanced syntax highlighting for:
- Python (including docstrings, exceptions, decorators, type annotations)
- C/C++ (preprocessor directives, macros, structs, pointers, sizeof)
- LaTeX/TeX (math mode, environments, citations, references, sections)
- JavaScript/TypeScript (classes, modules, interfaces, enums)
- Shell scripts (pipes, redirects, heredocs, builtins, command substitution)
- CSS/SCSS (IDs, pseudo-classes, variables, units, property values)
- Markdown (H1-H6 heading hierarchy, blockquotes, lists, code blocks)
- Regex (patterns, character classes, quantifiers, anchors)
- HTML/JSX, Go, Rust, JSON, YAML

## Customization

To customize the theme, you can override settings in your `settings.json`:

```json
{
  "workbench.colorCustomizations": {
    "[CoMPhy Gruvbox Classic]": {
      // Add your customizations here
    },
    "[CoMPhy Gruvbox Pop]": {
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
