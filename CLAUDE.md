# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build Commands
- Package extension: `npx @vscode/vsce package`
- Install VSCE if not present: `npm install -g @vscode/vsce`
- Publish: Push to main branch (GitHub Action handles VSCode Marketplace and Open VSX Registry)
- Debug theme: F5 in VSCode to launch Extension Development Host

## Architecture Overview
This is a VSCode theme extension that provides two flagship CoMPhy Gruvbox-based color themes:
1. **CoMPhy Gruvbox Classic** - Traditional Gruvbox hard dark background (#1d2021)
2. **CoMPhy Gruvbox Pop** - Pure black (#000000) with vibrant Dracula-inspired syntax palette

## Theme File Structure
Theme JSON files in `themes/` directory follow this organization:
1. **tokenColors**: Syntax highlighting rules with TextMate scopes
   - General/global tokens (comments, constants, keywords, etc.)
   - Language-specific scopes (Python, JavaScript, LaTeX, etc.)
2. **colors**: UI element colors (editor, sidebar, terminal, etc.)
3. **semanticTokenColors**: Modern semantic highlighting

## Development Guidelines
- JSON formatting: 2-space indentation
- Use descriptive comments to delineate sections in theme files
- Theme naming convention: "CoMPhy Gruvbox [Variant]" (Classic, Pop)
- Color declarations should reference Gruvbox palette names in comments
- All edits go to source files in `theme-base/` -- never edit `themes/*.json` directly
- Test theme modifications across multiple languages, especially C, Python, and LaTeX
- Increment version in package.json for all changes before pushing

## Color Palettes
### Classic (Gruvbox):
- Background: #1d2021, Foreground: #ebdbb2
- Red: #fb4934, Green: #b8bb26, Yellow: #fabd2f
- Blue: #83a598, Purple: #d3869b, Aqua: #8ec07c, Orange: #fe8019

### Pop (Dracula-inspired):
- Background: #000000, Foreground: #e8e0d4
- Functions: #ff79c6, Strings: #50fa7b, Keywords: #f1fa8c
- Numbers: #bd93f9, Types: #8be9fd, Comments: #7887ab, Operators: #ffb86c