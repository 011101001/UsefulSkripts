# UsefulSkripts

A collection of lightweight, useful, and configurable Minecraft **Skript** utilities to improve your server.

> **Work in progress.** The repository currently contains 2 scripts imported from the starter ZIP (not yet independently tested) and 10 clearly labeled *planned* starter files. A planned file is **not a working script**.

## Categories and script roadmap

| Category | Scripts | Current status |
| --- | --- | --- |
| [Mining](./Mining/) | `telepathy.sk`, `universal_fortune.sk` | 2 provided (untested) |
| [Farming](./Farming/) | `TreeCapitator.sk`, `AutoReplant.sk` | 2 planned placeholders |
| [Inventory](./Inventory/) | `ItemLock.sk`, `InventorySorter.sk` | 2 planned placeholders |
| [PlayerUtilities](./PlayerUtilities/) | `DurabilityAlerts.sk`, `DeathLocation.sk` | 2 planned placeholders |
| [ServerAdministration](./ServerAdministration/) | `EntityCleanup.sk`, `ChatClear.sk` | 2 planned placeholders |
| [Gameplay](./Gameplay/) | `SleepVoting.sk`, `CustomCrafting.sk` | 2 planned placeholders |

## Installation (implemented scripts only)

1. Install a compatible version of [Skript](https://docs.skriptlang.org/) on your Minecraft server.
2. Download an implemented `.sk` file and place it in `plugins/Skript/scripts/`.
3. Run `/sk reload <filename>` in-game or from the server console, and check for errors.
4. Test on a non-production server before using live. The initial mining scripts have **not** been verified against a specific Minecraft or Skript version.

Do **not** install the files marked `STATUS: PLANNED — NOT IMPLEMENTED` expecting them to work; they contain only comments and TODOs.

## Contribution goals

Each completed script should be standalone where practical, include configuration and permissions if relevant, and document tested server/Skript versions, conflicts, and anti-duplication considerations.

## Original mining scripts

- [Telepathy](./Mining/telepathy.sk) — from the uploaded `telepathy.sk`
- [Universal Fortune](./Mining/universal_fortune.sk) — from the uploaded `universal_fortune.sk`

These two files are kept under their original filenames because their code mentions each other's filenames.
