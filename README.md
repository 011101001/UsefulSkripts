# UsefulSkripts

Lightweight and configurable Minecraft Skript utilities for server owners.

> **Initial development release:** all 12 script files contain implementations, but none have been tested here on a live Minecraft server. Features and syntax may need adjustment for your Skript, Minecraft, and addon versions.

## Scripts

| Category | Skripts |
| --- | --- |
| [Mining](./Mining/) | `Telepathy.sk`, `UniversalFortune.sk` |
| [Farming](./Farming/) | `TreeCapitator.sk`, `AutoReplant.sk` |
| [Inventory](./Inventory/) | `ItemLock.sk`, `InventorySorter.sk` |
| [PlayerUtilities](./PlayerUtilities/) | `DurabilityAlerts.sk`, `DeathLocation.sk` |
| [ServerAdministration](./ServerAdministration/) | `EntityCleanup.sk`, `ChatClear.sk` |
| [Gameplay](./Gameplay/) | `SleepVoting.sk`, `CustomCrafting.sk` |

## Requirements

- Compatible Minecraft server and Skript 2.10+ for most scripts.
- **EntityCleanup** uses `time lived of entity`, available in Skript 2.13+.
- **CustomCrafting** requires the [SkBee](https://github.com/ShaneBeee/SkBee) addon (3.0+).
- Not all commands are meant for public use. Assign only the permissions you intend to grant.
- Back up the world and Skript variables before testing.

## Install and verify

1. Download the desired `.sk` files into `plugins/Skript/scripts/`.
2. Install SkBee if you choose `CustomCrafting.sk`.
3. Run `/sk reload <filename>` on a **test server**, then review the errors and warnings in console.
4. Verify drops, inventory stacks, permissions, and anti-dupe behavior with another player before live deployment.
5. Enable only the scripts you need. Test possible interactions with existing plugins.

## Important limitations

- **TreeCapitator**: permission `usefulskripts.treecapitator` is required. Scripted extra breaks may bypass protection plugins, and extra axe durability is not charged. Do not grant this permission on protected servers without checking the integration first.
- **AutoReplant**: replaces mature crops for free after breaking them, provided the position remains empty. It does not consume seeds.
- **ItemLock**: locks material types for each player and only prevents manual drops. It is not an item-by-item lock or a death-inventory protection feature.
- **InventorySorter**: sorts, but does not merge identical stacks. It leaves armor and offhand unchanged.
- **EntityCleanup**: manual only, staff permission `usefulskripts.admin.cleardrops`. Items younger than the minimum age are not removed.
- **ChatClear**: permission `usefulskripts.admin.clearchat`.
- **UniversalFortune**: intentionally differs from vanilla Fortune loot tables. Do not install alongside another Fortune override without testing.
- **Telepathy**: when inventory space is insufficient, items remain as world drops.

## Current status

- 12 script files with initial code.
- 6 category READMEs and this root README.
- Server reload / live gameplay tests: **not performed**.
- Recommended next steps: run reload checks, verify permissions, test inventory and crop behavior, then tag the first stable version.

## Reference

- [Skript documentation](https://docs.skriptlang.org/)
- [SkBee](https://github.com/ShaneBeee/SkBee)
