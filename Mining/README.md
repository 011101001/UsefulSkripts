# Mining

Tools for gathering, processing and storing resources.

| Script | Feature | Use |
| --- | --- | --- |
| [Telepathy.sk](./Telepathy.sk) | Collect mined drops and briefly follow the player when inventory is full | `/telepathy` |
| [UniversalFortune.sk](./UniversalFortune.sk) | Custom Fortune multiplier for ordinary blocks | Automatic |
| [VeinMiner.sk](./VeinMiner.sk) | Sneak-mine connected ores | `usefulskripts.veinminer` permission |
| [AutoSmelt.sk](./AutoSmelt.sk) | Convert raw ore drops into ingots | `/autosmelt` |
| [AutoCompress.sk](./AutoCompress.sk) | Compress groups of 9 resource items, based on their actual counts | `/compress`, `/autocompress` |

### AutoCompress

`/compress` converts available materials once. `/autocompress on` converts immediately and again after an inventory-slot change. Each eligible material is counted once per conversion, with one batch per material. There are no repeating world timers or per-block conversion loops.

### Telepathy

Telepathy uses the original item-spawn detection, recent block tracking, and short overflow-follow mechanism. It works alongside UniversalFortune. As an original-code restoration, it does not yet consult PickupFilter, so items caught by Telepathy directly can bypass the pickup blacklist. If you use both scripts, turn Telepathy off when you need PickupFilter to enforce an item restriction.

VeinMiner performs additional scripted block breaks. Confirm land protection behavior in your server configuration before granting its permission. Test combined drop handling with your server version.

[Back to the main README](../README.md).
