# Inventory

Utilities for handling and organizing items.

| Script | Feature | Command |
| --- | --- | --- |
| [ItemLock.sk](./ItemLock.sk) | Block Q-dropping selected material types | `/itemlock` |
| [InventorySorter.sk](./InventorySorter.sk) | Sort the main inventory only, preserving the hotbar | `/sort` |
| [PickupFilter.sk](./PickupFilter.sk) | Blacklist materials from ground pickup by hand or item name | `/pickupfilter [item]` |
| [AutoRefill.sk](./AutoRefill.sk) | Refill empty hotbar stacks from main storage | `/autorefill` |

InventorySorter only changes slots 9-35. Use `/pickupfilter diamond` or `/pickupfilter diamond sword` to toggle a material without holding it, or use `/pickupfilter` while holding an item. Use `/pickupfilter list` to view filters and `/pickupfilter clear` to reset them.

PickupFilter blocks normal ground pickup. The original Telepathy script has its own direct item collection and does not consult this blacklist.

[Back to the main README](../README.md).
