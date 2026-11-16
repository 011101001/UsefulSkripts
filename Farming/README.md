# Farming

Crop and tree gathering helpers.

| Script | Feature | Usage |
| --- | --- | --- |
| [TreeCapitator.sk](./TreeCapitator.sk) | Break matching connected logs after the first log | Sneak with an axe |
| [AutoReplant.sk](./AutoReplant.sk) | Replant mature crops automatically | Automatic |
| [HarvestHoe.sk](./HarvestHoe.sk) | Break and replant mature nearby crops | Sneak with a hoe; `usefulskripts.harvesthoe` |

TreeCapitator now works by default without an extra permission or a nearby leaves check. Set `require-permission: true` or `require-leaves: true` in its options if your server needs them. It only follows matching connected log types and has a maximum log count and distance.

Scripted block-breaking features should be checked with land claims or protection plugins.

[Back to the main README](../README.md).
