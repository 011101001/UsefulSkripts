# Changelog

Notable changes to UsefulSkripts are documented here.

## 0.2.0-beta.1 - 2026-11-15

### Added

- **VeinMiner** - bounded ore vein mining with sneak activation and a permission.
- **AutoSmelt** - toggleable conversion of raw iron, gold and copper drops.
- **AutoCompress** - manual and periodic compression of common resources into storage blocks.
- **HarvestHoe** - area crop harvesting and replanting with a permission.
- **PickupFilter** - per-player ground item material blacklist.
- **AutoRefill** - refill empty hotbar stacks from stored materials.
- **AFKSystem** - manual AFK status and inactivity detection.

### Changed

- Telepathy checks the PickupFilter material blacklist before direct pickup.
- AutoCompress checks for space for the output block before removing inputs.
- Updated all six category guides with commands and feature descriptions.
- Refreshed script headers and repository documentation for a public-facing version.
- Committed each category separately to keep the GitHub folder history meaningful.

### Compatibility

- Target platform: modern Paper/Spigot, with Minecraft 1.21.4+ aliases.
- Recommended Skript: 2.13+.
- SkBee: required only for CustomCrafting.

### Installation

Download the individual scripts you need and place them in `plugins/Skript/scripts/`. Follow the [README](./README.md) for commands, permissions and compatibility guidance. Use a staging server to verify reloads and interactions with other plugins.

## 0.1.0 - Initial collection

- Mining: Telepathy and Universal Fortune.
- Farming: TreeCapitator and AutoReplant.
- Inventory: ItemLock and InventorySorter.
- Player Utilities: DurabilityAlerts and DeathLocation.
- Server Administration: EntityCleanup and ChatClear.
- Gameplay: SleepVoting and CustomCrafting.
