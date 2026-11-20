# Changelog

## 1.0.2
- Added native Folia server compatibility (`folia-supported: true`) via a dual-compatible scheduler (`FoliaScheduler`), supporting both Folia regional schedulers and standard Paper/Leaf.
- Updated project and repository license to All Rights Reserved (ARR).

## 1.0.1
- Added `allow-hopper-extraction` (default `false`) config option to prevent hoppers and hopper minecarts from draining structure loot containers.
- Registered containers on `LootGenerateEvent` so hoppers cannot siphon and clear unopened loot tables before players discover them.
- Fixed natural double-chest partner discovery: properly discovers and tracks chests when structures assign the loot table to only one half, while preserving distinct loot tables per half.
- Fixed sneak-click interaction to align with vanilla behavior (sneaking with items in either hand skips opening).
- Scoped countdown and reset announcements to players inside the resetting world in `PER-WORLD` mode.

## 1.0.0
- Shared structure loot that re-rolls on a timed cycle (`GLOBAL` or `PER-WORLD`).
- Configurable `tracked-containers` (incl. copper chests).
- New `wipe-player-items` option and `lootcycle.bypass` permission.
- Fixed: countdown burst when starting inside the countdown window.
- Fixed: disabled worlds no longer protect loot containers.
- Fixed: guard against an uninitialised reset clock; `/lootcycle reload` now anchors clocks when switching to PER-WORLD.
- `plugin.yml` version now comes from the Maven project version.
