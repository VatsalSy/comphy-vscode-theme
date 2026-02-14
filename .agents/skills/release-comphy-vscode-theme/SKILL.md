---
name: release-comphy-vscode-theme
description: Create versioned releases with proper tagging and automation for the CoMPhy Gruvbox VS Code theme extension. Use when asked to "release", "cut a release", "bump version", "create tag", "publish", or when preparing a new version.
---

# Release Workflow

`package.json` version is the single source of truth for the extension. Tags must be `vMAJOR.MINOR.PATCH` and match `package.json`. Publishing is handled by GitHub Actions (`Publish Extension`) on tag push or GitHub Release publish.

## Automated Release (Preferred)

### Tag Push (Standard)

1. Update version + changelog, regenerate themes, commit.
2. Create annotated tag `vX.Y.Z` and push tags.
3. The `Publish Extension` workflow publishes to VS Marketplace and Open VSX.

### GitHub Release (Alternate Trigger)

Publishing also runs when a GitHub Release is published with a `vX.Y.Z` tag that matches `package.json`.

### Dry Run (Validation)

Manually run the workflow with `dry_run=true` to validate packaging without publishing.

Required secrets: `VS_MARKETPLACE_TOKEN`, `OPEN_VSX_TOKEN`.

## Manual Release (Fallback)

### Pre-flight Checks

```bash
git branch --show-current  # Must be "main"
git status --porcelain     # Must be empty
git fetch origin main && git diff HEAD origin/main --quiet
```

### Analyze Changes

```bash
git describe --tags --abbrev=0
git log $(git describe --tags --abbrev=0)..HEAD --oneline
node -p "require('./package.json').version"
```

### Version Bump Decision

| Change Type | Bump | Example |
| --- | --- | --- |
| Breaking changes | `major` | 1.4.2 -> 2.0.0 |
| New features | `minor` | 1.4.2 -> 1.5.0 |
| Fixes/docs/refactors | `patch` | 1.4.2 -> 1.4.3 |

### Update Version + Changelog

- Update `package.json` version.
- Add a new section to `CHANGELOG.md` with date and highlights.

### Generate Themes

```bash
npm run build
```

### Pre-release Validation

```bash
npm run lint
npm test
```

### Package VSIX (Required)

```bash
VERSION=$(node -p "require('./package.json').version")
npx @vscode/vsce package
mv "comphy-gruvbox-$VERSION.vsix" comphy-gruvbox.vsix
```

### Execute Release

```bash
VERSION=$(node -p "require('./package.json').version")
git add package.json CHANGELOG.md themes/*.json comphy-gruvbox.vsix
git commit -m "Release v$VERSION"
git tag -a "v$VERSION" -m "Release v$VERSION"
git push --follow-tags
```

### Manual Publish (Only if Actions Unavailable)

```bash
npm install -g @vscode/vsce ovsx
VSCE_TOKEN=...  # VS_MARKETPLACE_TOKEN
OVSX_TOKEN=...  # OPEN_VSX_TOKEN
npx @vscode/vsce publish -p $VSCE_TOKEN
npx ovsx create-namespace vatsalsy -p $OVSX_TOKEN || true
npx ovsx publish -p $OVSX_TOKEN
```

## Post-release Verification

```bash
git ls-remote --tags origin | tail -3
node -p "require('./package.json').version"
git describe --tags --abbrev=0
```

- Confirm the new version is visible for `vatsalsy.comphy-gruvbox` on VS Marketplace and Open VSX.

## Rollback (if needed)

If a tag needs to be removed, delete it locally and remotely, then create a revert commit.

```bash
git tag -d vX.Y.Z
git push origin --delete vX.Y.Z
git revert <release-commit-sha>
git push
```
