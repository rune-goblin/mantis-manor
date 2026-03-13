# Mantis Manor

Scene maps for **Mark of the Mantis**, the PF2E standalone adventure.

Assets by [Forgotten Adventures](https://forgotten-adventures.net) and [Tom Cartos](https://www.patreon.com/tomcartos).

## Scenes

- **Everbloom Groundfloor** -- ground floor of Everbloom Manor with walls, lights, and roof tiles
- **Everbloom Second Floor** -- upper floor and tower
- **Forgotten Cellar** -- the hidden basement beneath the manor

## Installation

Paste this manifest URL in Foundry VTT (*Add-on Modules > Install Module*):

```
https://github.com/MarkPearce/mantis-manor/releases/latest/download/module.json
```

## Compatibility

- Foundry VTT v12 -- v13
- PF2E system

## Development

Scene data lives in `packs/_source/mantis-manor-scenes/` as JSON source files. Foundry compiles these into LevelDB at `packs/mantis-manor-scenes/` when the module loads.

### Local setup

Symlink the repo into your Foundry modules directory:

```bash
ln -s /path/to/marks-motm-maps \
  ~/Library/Application\ Support/FoundryVTT/Data/modules/mantis-manor
```

### Editing scenes

1. Launch Foundry -- it compiles `_source/` into `packs/mantis-manor-scenes/`
2. Edit scenes in Foundry as normal
3. Use *Compendium > Export* to write changes back to `_source/`
4. Commit both `packs/_source/` and `packs/mantis-manor-scenes/`

### Releasing

Push a version tag to trigger the GitHub Actions release workflow:

```bash
git tag v3.0.0
git push origin main --tags
```

The workflow stamps the version into `module.json`, builds `mantis-manor.zip`, and creates a GitHub release.
