# Changelog

All notable changes to the CoMPhy Color Theme Collection will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [3.0.0] - 2026-02-14

### Changed

- **BREAKING**: Extension ID renamed from `comphy-gruvbox` to `comphy-theme` (creates a new marketplace listing).
- Extension display name updated to `CoMPhy Color Theme Collection`.
- Repository and badge links updated to `VatsalSy/comphy-vscode-theme`.

### Migration Notes

- Install the new extension ID: VS Marketplace `VatsalSy.comphy-theme` or Open VSX `vatsalsy/comphy-theme`.
- If `VatsalSy.comphy-gruvbox` is installed, uninstall or disable it and reselect your preferred CoMPhy theme.

## [2.0.1] - 2026-01-31

### Added

- Add `.gitignore` for common OS, editor, and build artifacts.

### Changed

- Update README badges and marketplace links to the `comphy-gruvbox` listing and raw VSIX download.
- Make VSIX packaging a required release step and include the packaged `.vsix` in release commits.

## [2.0.0] - 2025-01-09

### Changed

- **BREAKING**: Repository renamed from `gruvbox_custom_themes` to `comphy-vscode-theme`
- **BREAKING**: All theme display names updated from "Gruvbox Crisp" to "CoMPhy Gruvbox"
  - "Gruvbox Crisp (High Contrast, with TeX)" → "CoMPhy Gruvbox (High Contrast, with TeX)"
  - "Gruvbox Crisp (Medium, with TeX)" → "CoMPhy Gruvbox (Medium, with TeX)"
  - "Gruvbox Crisp (Soft, with TeX)" → "CoMPhy Gruvbox (Soft, with TeX)"
  - "Gruvbox Crisp Anysphere Blend" → "CoMPhy Gruvbox Anysphere Blend"
  - "Gruvbox Crisp Anysphere (High Contrast)" → "CoMPhy Gruvbox Anysphere (High Contrast)"
  - "Gruvbox Crisp Anysphere (Highest Contrast, pop)" → "CoMPhy Gruvbox Anysphere (Highest Contrast, pop)"
- Repository moved to: https://github.com/VatsalSy/comphy-vscode-theme
- Extension description updated to emphasize computational physics workflow optimization
- Added "comphy" and "computational physics" to extension keywords
- **BREAKING**: Extension ID changed from `gruvbox-crisp-tex` to `comphy-gruvbox` (creates new marketplace listing)

### Migration Notes

- **Existing users**: You will need to reselect your theme in VSCode settings after updating
- Theme functionality and colors remain unchanged - only names have been updated
- All color schemes and syntax highlighting remain identical to previous versions
- No changes to theme files, color palettes, or visual appearance

## [1.3.0] - 2025-09-05

### Added

- New theme variant: **Gruvbox Crisp Anysphere (Highest Contrast, pop)**
  - Pure black background (`#000000`) with bright near‑white foreground (`#ffffff`)
  - Purple‑forward accents (focus/links `#bd93f9`, buttons/cursor `#9b4fa0`)
  - Vibrant "pop" syntax palette (functions `#ff79c6`, keywords `#f1fa8c`, strings `#50fa7b`, numbers `#bd93f9`, types `#8be9fd`)
  - Readability improvements for comments/inlay hints using blue‑gray `#6272a4`
  - Terminal ANSI palette aligned to Ghostty/tmux pop scheme

### Changed

- **Gruvbox Crisp Anysphere (Highest Contrast, pop)** refinements:
  - Sidebar/activity bar now use `#0a0a0a` for subtle visual hierarchy while editor remains pure black
  - Added hover states (`editor.hoverHighlightBackground`, `list.hoverBackground`) for better navigation
  - Fixed `terminal.ansiBlack` to `#212121` for visibility of black ANSI text
  - Removed `editor.selectionForeground` to allow VSCode/Cursor to auto-calculate optimal contrast

### Notes

- The **Highest Contrast, pop** variant uses pure black (`#000000`) specifically for monitors requiring extreme contrast and maximum "pop" effect
- This release adds features without removing or changing existing variants; it is a minor version bump per SemVer.

## [1.2.0] - 2025-01-06

### Added

- Two new Anysphere Blend theme variants:
  - Gruvbox Crisp Anysphere Blend (standard)
  - Gruvbox Crisp Anysphere (High Contrast)
- Automated theme generation system from base configuration files
- Comprehensive test suite for theme validation and color contrast testing
- Build scripts for theme generation and quality assurance
- Consolidated color palette documentation

### Changed

- Complete theme architecture overhaul with base configuration system
- Improved build system with automated theme variant generation
- Enhanced documentation with consolidated theme information
- All themes now generated from unified base configuration for consistency

### Fixed

- Semantic token color definitions across all theme variants
- Theme file structure and organization consistency
- Color palette standardization across all variants

## [1.1.8] - 2025-01-06

### Added

- Theme validation tests (`test/validate-themes.js`) to ensure JSON correctness
- Color contrast ratio tests (`test/test-contrast.js`) for WCAG AA accessibility compliance
- Changelog section to README
- *.vsix to .gitignore

### Changed

- Standardized theme file organization and color definitions
- All themes now have consistent token color rule counts (127–133 rules)

### Fixed

- Standardized all hex color values to lowercase across all themes
- Color typo #FB4834 → #fb4934 in purple themes
- Unified theme naming: "Durham Blend" → "Anysphere Blend" for consistency
- Updated documentation to clarify LaTeX support is available in all theme variants

### Removed

- VSIX files from repository (now built only during release)

## [1.1.7] - 2024-12-17

### Fixed

- Removed all JSON comments from theme files for strict JSON compliance
- Updated repository URLs in package.json to match actual repository name
- README download badge to use dynamic latest release link
- Fully implemented medium and soft theme variants with complete token definitions

## [1.1.6] - 2024-12-17

### Fixed

- Text selection visibility in high contrast purple theme

### Changed

- Improved overall contrast and readability

## [1.1.5] - Previous Release

### Added

- Initial release of Gruvbox Crisp theme collection
- Five theme variants:
  - Gruvbox Crisp (High Contrast, with TeX)
  - Gruvbox Crisp (Medium, with TeX)
  - Gruvbox Crisp (Soft, with TeX)
  - Gruvbox Crisp Anysphere Blend
  - Gruvbox Crisp Anysphere Blend (High Contrast)
- Comprehensive LaTeX/TeX support with specialized syntax highlighting
- Enhanced syntax highlighting for multiple languages
- Semantic token coloring support
