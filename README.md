# UsefulSkripts

**Lightweight Minecraft Skript utilities for survival servers.** Install the features you want without having to run a complete custom gamemode.

**Version:** 0.2.0-beta.2 | **Scripts:** 19 | **Categories:** 6

## Features

| Category | Skripts |
| --- | --- |
| [Mining](./Mining/) | [Telepathy](./Mining/Telepathy.sk), [Universal Fortune](./Mining/UniversalFortune.sk), [VeinMiner](./Mining/VeinMiner.sk), [AutoSmelt](./Mining/AutoSmelt.sk), [AutoCompress](./Mining/AutoCompress.sk) |
| [Farming](./Farming/) | [TreeCapitator](./Farming/TreeCapitator.sk), [AutoReplant](./Farming/AutoReplant.sk), [HarvestHoe](./Farming/HarvestHoe.sk) |
| [Inventory](./Inventory/) | [ItemLock](./Inventory/ItemLock.sk), [InventorySorter](./Inventory/InventorySorter.sk), [PickupFilter](./Inventory/PickupFilter.sk), [AutoRefill](./Inventory/AutoRefill.sk) |
| [Player Utilities](./PlayerUtilities/) | [DurabilityAlerts](./PlayerUtilities/DurabilityAlerts.sk), [DeathLocation](./PlayerUtilities/DeathLocation.sk), [AFKSystem](./PlayerUtilities/AFKSystem.sk) |
| [Server Administration](./ServerAdministration/) | [EntityCleanup](./ServerAdministration/EntityCleanup.sk), [ChatClear](./ServerAdministration/ChatClear.sk) |
| [Gameplay](./Gameplay/) | [SleepVoting](./Gameplay/SleepVoting.sk), [CustomCrafting](./Gameplay/CustomCrafting.sk) |

Each folder includes a short guide and links to its individual scripts.

## Requirements

- A compatible modern Paper or Spigot server. Minecraft 1.21.4+ is the target for the current block aliases.
- [Skript](https://docs.skriptlang.org/) 2.13+ is recommended for the complete collection.
- [SkBee](https://github.com/ShaneBeee/SkBee) 3.0+ is required **only** for `Gameplay/CustomCrafting.sk`. Install a SkBee build compatible with your server.
- A permissions plugin is recommended to manage restricted abilities.

## Installation

1. Download the `.sk` files you want from their category folders.
2. Copy them into `plugins/Skript/scripts/` on your server.
3. Install SkBee if you are using CustomCrafting.
4. Run `/sk reload all` or `/sk reload <filename>`.
5. Review console output for reload errors and check commands in-game.
6. Use a test world before enabling scripted mining or area harvesting on a protected server.

Scripts can be installed individually. The following optional integrations work when both corresponding files are present:

- **Telepathy + UniversalFortune:** Direct pickup of Universal Fortune's generated drops.
- **Telepathy + PickupFilter:** The restored original Telepathy uses its own direct item collection and does not check PickupFilter. Disable Telepathy when a pickup blacklist must be enforced.
- **AutoSmelt + Telepathy:** AutoSmelt processes standard block drops before direct pickup when the handlers run in their intended event order.
- **AutoCompress + Telepathy:** With AutoCompress enabled, inventory-slot changes trigger a single count-based compression pass. No repeating timer is used.

## Commands

| Command | Purpose |
| --- | --- |
| `/telepathy` [on|off]` | Toggle direct collection of mined drops |
| `/autosmelt` [on|off]` | Toggle automatic raw ore smelting |
| `/compress` | Compress eligible materials immediately |
| `/autocompress` [on|off]` | Toggle periodic inventory compression |
| `/pickupfilter [item]` | Toggle a held material or type a name, such as `diamond sword` |
| `/autorefill` [on|off]` | Toggle automatic hotbar stack refill |
| `/itemlock` | Toggle Q-drop protection for the held item material |
| `/sort` | Sort only main inventory slots 9-35 and leave the hotbar unchanged |
| `/deathloc` | Show the last saved death coordinates |
| `/afk` | Toggle AFK status |
| `/cleardrops` | Clean up older dropped items with a warning |
| `/clearchat` | Push previous public chat messages out of view |

Other features operate automatically or activate when sneaking with the appropriate tool.

## Permissions

| Permission | Feature |
| --- | --- |
| `usefulskripts.veinminer` | VeinMiner |
| `usefulskripts.treecapitator` | TreeCapitator, only when `require-permission: true` is enabled |
| `usefulskripts.harvesthoe` | HarvestHoe |
| `usefulskripts.admin.cleardrops` | EntityCleanup |
| `usefulskripts.admin.clearchat` | ChatClear |

Permissions are not granted by this repository. Assign them through your server's permissions system.

## Configuration and compatibility

Each script contains an `options:` section when it has configurable settings. Edit those options, save the file, and reload that script.

- **VeinMiner, TreeCapitator and HarvestHoe** perform additional scripted block breaks. TreeCapitator now works by default while sneaking with an axe, without a permission or leaves requirement. Its `require-permission` and `require-leaves` options can be enabled for stricter use. Verify all three scripts with claim and protection plugins.
- **UniversalFortune** uses an ore-style multiplier rather than reproducing every vanilla loot table.
- **AutoCompress** counts each eligible material once per pass, converts full groups of nine in a single batch, and checks for output space before removing inputs. `/autocompress` is triggered by inventory changes, not a repeating timer.
- **AutoReplant and HarvestHoe** replant crops without consuming additional seeds.
- **AutoRefill and ItemLock** compare material types. They are not full metadata-aware item management systems.
- **InventorySorter** only touches the three main storage rows, not hotbar, armor or offhand slots.
- **PickupFilter** accepts item names as text, plus `list` and `clear` subcommands. The original Telepathy can still directly collect items that PickupFilter would otherwise block.
- **PickupFilter** prevents ordinary ground pickup and is also honored by Telepathy.
- **CustomCrafting** registers a sample name tag recipe. Change its recipe ID if you add more recipes.

Compatibility depends on the server, Skript version and other installed plugins. Review script reload errors and verify item quantities and protections before production deployment.

## Releases

See [CHANGELOG.md](./CHANGELOG.md) for version history, feature summaries and changes.

## Contributing

Bug reports, compatibility findings and improvements are welcome through GitHub Issues and pull requests. Include the Minecraft, Skript and addon versions and the relevant console errors when reporting a problem.
