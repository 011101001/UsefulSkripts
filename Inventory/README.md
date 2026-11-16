# Inventory

Utilities for handling and organizing items.

| Script | Feature | Command |
| --- | --- | --- |
| [ItemLock.sk](./ItemLock.sk) | Block Q-dropping selected material types | `/itemlock` |
| [InventorySorter.sk](./InventorySorter.sk) | Sort player storage slots | `/sort` |
| [PickupFilter.sk](./PickupFilter.sk) | Blacklist materials from ground pickup | `/pickupfilter` |
| [AutoRefill.sk](./AutoRefill.sk) | Refill empty hotbar stacks from main storage | `/autorefill` |

PickupFilter protects against normal pickup and is also honored by Telepathy when that integration is enabled. AutoRefill transfers an existing matching stack only when the hotbar slot is empty.

[Back to the main README](../README.md).
