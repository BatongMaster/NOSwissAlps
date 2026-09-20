# Swiss Alps - a custom map for Nuclear Option

Western Switzerland at true scale: 199,680 m square, from Geneva across to Zurich and south to
Mont Blanc. The terrain is the real one, built from the Copernicus GLO-30 elevation model - Lake
Geneva is the map's sea level, the Alps rise 4.4 km above it, and the valleys and passes are where
they are on the chart. Roads come from swisstopo's national survey: about 1,470 km of motorway and
expressway through the passes for ground AI to drive, with the cantonal main roads drawn beside
them, 5,800 km of road surface in all, meshed as ribbons you can drive on and follow at low
level.

| | |
|---|---|
| Size | 199,680 m square, 1,521 terrain tiles of 5,120 m |
| Bounds | 6.04–8.66 °E, 45.70–47.50 °N |
| Terrain | Copernicus DEM GLO-30, 51.2 m vertex pitch, datum at Lake Geneva's surface (368 m ASL) |
| Highest point | 4,437.5 m above the datum (Mont Blanc) |
| Water | Lake Geneva as real engine water; fourteen more lakes as raised surfaces at their true heights |
| Roads | swissTLMRegio, ~1,470 km in the pathing network and ~5,800 km drawn, with bridges and tunnels |
| Trees | 2.6 million |
| Buildings | 65,000, in the real towns |
| Bundle | `swissalps-0.2.0.nomap`, about 1.5 GB, attached to the release |

The map ships one airfield, Geneva Airport, with the ground levelled under it. Everywhere else the
terrain stays as the elevation model has it. A mission adds whatever other airbases it needs
through the game's own mission editor, so pick flat ground for them: this is the Alps, and most of
it is not flat.

## What you need

- **Nuclear Option** (the map is a mod; it does nothing on its own).
- **BepInEx 5** for Nuclear Option.
- **NOCustomMaps**, the plugin that registers `.nomap` bundles as playable maps, borrows the game's
  own materials, grass, trees and buildings onto them, and rebuilds the battlefield grid.

## Installing

1. Download `swissalps-0.2.0.nomap` from this repository's releases. It is about 1.5 GB.
2. Copy it into `BepInEx/plugins/NOCustomMaps/maps/` under your Nuclear Option installation.
   (`CustomMaps/` under the game's persistent data path works too; the plugin looks in both.)
3. Start the game once and look in `BepInEx/LogOutput.log` for the line the plugin prints when it
   registers the map:

   ```
   swissalps-0.2.0.nomap -> cm.swissalps.<hash8> ("Swiss Alps", 199680x199680 m)
   ```

   The `cm.swissalps.<hash8>` name is how missions refer to the map. The eight hex digits are the
   start of the bundle's SHA-256, so they identify this exact build.
4. In a mission, set `MapKey.Path` to that name and `MapKey.Type` to `GameWorldPrefab`. Missions
   live in `%USERPROFILE%\AppData\LocalLow\Shockfront\NuclearOption\Missions\<name>\<name>.json`.

**Multiplayer:** the server and every client need the identical `.nomap` file. The hash in the
registered name is the version handshake - a client with a different build of the map fails to
match and is told so at join time, instead of silently disagreeing about where the ground is.

## Licence and credits

The map itself, meaning its meshes, textures, placements and arrangement, is by **`<YOUR NAME>`**
and is licensed **CC BY 4.0** ([LICENSE](LICENSE)); attribute it as *"Swiss Alps for Nuclear
Option" by `<YOUR NAME>`, CC BY 4.0*. The data it was built from keeps its own terms: the terrain
carries the Copernicus DEM notices, and the road network asks for a line of credit to swisstopo
and nothing more. [NOTICE.md](NOTICE.md) is the full set of attributions and duties, including
which shipped asset comes from which source. Carry it with the map if you pass the map on.

The same credit is inside the map, not only in this repository: it is the `credits` field of the
manifest the bundle carries, and it is stamped onto the tactical chart you open in flight. Word
for word, it reads:

> produced using Copernicus WorldDEM-30 © DLR e.V. 2010-2014 and © Airbus Defence and Space GmbH
> 2014-2018 provided under COPERNICUS by the European Union and ESA; all rights reserved. Roads:
> © swisstopo.

The manifest carries a second field, `notice`, which nothing draws: it holds what the Copernicus
licence asks for beyond the credit, so those obligations travel inside the file as well.

The Copernicus licence also asks that these travel with the map. Its own sentence, word for word:
*The organisations in charge of the Copernicus programme by law or by delegation do not incur any
liability for any use of the Copernicus WorldDEM-30*. And in this project's words: Airbus, DLR,
ESA, the European Union and Copernicus do not endorse this map or any use made of it, and anyone
you give the map to takes it on these same obligations.

## Disclaimer

> This project is an unofficial fan modification not affiliated with, sponsored by, or endorsed by
> Shockfront Studios. All original Nuclear Option assets and code are Copyright © 2026 Shockfront
> Studios. Shockfront Studios and Nuclear Option are trademarks of Shockfront Studios. All other
> trademarks and original mod content belong to their respective owners.

It is free and it is not a standalone product. Nuclear Option's EULA forbids selling or monetising
mods, and this is a mod: that restriction comes from Shockfront, not from the licence above, and it
binds anyone who passes the map on.

**It contains no Nuclear Option assets.** The bundle ships placeholder materials with no textures
and no shaders in them; the plugin swaps each one for the equivalent material from the player's own
copy of the game when the map loads. The same goes for the trees, the grass and the buildings - the
map says where they stand, the game provides what stands there. Nothing here works, or is of any
use, without the game.
