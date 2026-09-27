# Swiss Alps - a custom map for Nuclear Option

Western Switzerland at true scale: 199,680 m square, from Geneva across to Zurich and south to
Mont Blanc. The terrain is the real one, built from the Copernicus GLO-30 elevation model - Lake
Geneva is the map's sea level, the Alps rise 4.4 km above it, and the valleys and passes are where
they are on the chart. Roads come from swisstopo's national survey: about 5,100 km of
motorway, expressway and main road for ground AI to drive, 5,800 km of road surface in
all, meshed as ribbons you can drive on and follow at low level.

| | |
|---|---|
| Size | 199,680 m square, 1,521 terrain tiles of 5,120 m |
| Bounds | 6.04–8.66 °E, 45.70–47.50 °N |
| Terrain | Copernicus DEM GLO-30, 51.2 m vertex pitch, datum at Lake Geneva's surface (368 m ASL) |
| Highest point | 4,437.5 m above the datum (Mont Blanc) |
| Water | Lake Geneva as real engine water; fourteen more lakes as raised surfaces at their true heights |
| Roads | swissTLMRegio, ~5,100 km in the pathing network and ~5,800 km drawn, with bridges and tunnels |
| Trees | 2.6 million |
| Buildings | about 68,000, in the real towns |
| Bundle | `swissalps-0.3.0.nomap`, about 1.3 GB, attached to the release |

The map ships six airfields: Geneva and Zurich (big), Payerne and Meiringen (medium), Sion and
Bern (small). Payerne, Meiringen, Sion and Bern lie on their real runways' lines; Geneva stands
about 6 km north of its real runway, turned north-south to keep off the map's coast, and Zurich
stands on the Reuss plain, since Kloten lies in the map's coastal sea. Each has the ground levelled
under it and its taxiways and aprons laid out after the real ones as swisstopo surveyed them, and
Zurich has Kloten's other two runways as well. Elsewhere the ground is levelled under the roads and
dug out where they run in cuttings. The rest follows the elevation model, reshaped only for water:
the outer 9 km or so at every edge slopes down into the map's coastal sea, the lake beds are carved
out and their shores shaped, and dry ground lower than Lake Geneva's surface is lifted just clear of
it. A mission can add further airbases through the game's own mission editor, so pick flat ground
for them: this is the Alps, and most of it is not flat.

## What you need

- **Nuclear Option** (the map is a mod; it does nothing on its own).
- **BepInEx 5** for Nuclear Option.
- **NOCustomMaps**, the plugin that registers `.nomap` bundles as playable maps, borrows the game's
  own materials, grass, trees and buildings onto them, and rebuilds the battlefield grid. Use
  release v1.1.0 or later, from <https://github.com/BatongMaster/NOCustomMaps/releases>: this map's
  airbase data is in a newer format, and an older release, v1.0.0 of 20 September 2026 included,
  loads the map without any of its airbases. The plugin writes its version to
  `BepInEx/LogOutput.log` when the game starts, in a line that reads `v1.1.0 ready.` for that
  release.

## Installing

1. Download `swissalps-0.3.0.nomap` from this repository's releases. It is about 1.3 GB.
2. Copy it into `BepInEx/plugins/NOCustomMaps/maps/` under your Nuclear Option installation.
   (`CustomMaps/` under the game's persistent data path works too; the plugin looks in both.)
3. Start the game once and look in `BepInEx/LogOutput.log` for the line the plugin prints when it
   registers the map:

   ```
   swissalps-0.3.0.nomap -> cm.swissalps.<hash8> ("Swiss Alps", 199680x199680 m)
   ```

   The `cm.swissalps.<hash8>` name is how missions refer to the map. The eight hex digits are the
   start of the bundle's SHA-256, so they identify this exact build.
4. In a mission, set `MapKey.Path` to that name and `MapKey.Type` to `GameWorldPrefab`. Missions
   live in `%USERPROFILE%\AppData\LocalLow\Shockfront\NuclearOption\Missions\<name>\<name>.json`.

**Multiplayer:** the server and every client need the identical `.nomap` file. The hash in the
registered name is the version handshake - a client with a different build of the map fails to
match and is told so at join time, instead of silently disagreeing about where the ground is.

## Licence and credits

The map itself, meaning its meshes, textures, placements and arrangement, is by **BatongMaster**
and is licensed **CC BY 4.0** ([LICENSE](LICENSE)); attribute it as *"Swiss Alps for Nuclear
Option" by BatongMaster, CC BY 4.0*, with a link to the licence
(<https://creativecommons.org/licenses/by/4.0/>) and to this repository
(<https://github.com/BatongMaster/NOSwissAlps>). The data it was built from keeps its own terms:
the terrain carries the Copernicus DEM notices, and the road network and the airfields' paving,
both from swisstopo, ask for a line of credit to swisstopo. [NOTICE.md](NOTICE.md) is the full set
of attributions and duties, including which shipped asset comes from which source. Carry it with
the map if you pass the map on.

The same credit is inside the map, not only in this repository: it is the `credits` field of the
manifest the bundle carries, and it is stamped onto the tactical chart you open in flight, whose
small pixel font draws each © as (c). Word for word, it reads:

> produced using Copernicus WorldDEM-30 © DLR e.V. 2010-2014 and © Airbus Defence and Space GmbH
> 2014-2018 provided under COPERNICUS by the European Union and ESA; all rights reserved.
> © swisstopo.

The manifest carries a second field, `notice`, which nothing draws. It holds what the Copernicus
licence asks for beyond the credit, so those obligations travel inside the file as well, and it
names the swisstopo data sets the map is built from: swissTLMRegio for the road network and
swissTLM3D for the airfields' paving.

The Copernicus licence also has this project make sure that everyone it lets pass the map on or
show it to the public, which is everyone who receives it, is bound by these obligations: to carry
its notice and its liability sentence when they do, and not to give the public the impression that
their activities, what they do with the map among them, are officially endorsed by Airbus Defence
and Space, the Copernicus licensor or anyone else in charge of Copernicus or of delivering its data.
Its sentence, word for word:
*The organisations in charge of the Copernicus programme by law or by delegation do not incur any
liability for any use of the Copernicus WorldDEM-30*. And in this project's words: Airbus Defence
and Space, DLR, ESA, the European Union and Copernicus do not endorse this map, its author or any
use made of it.

## Disclaimer

> This project is an unofficial community modification and is not affiliated with, sponsored by, or
> endorsed by Shockfront Studios Pty Ltd. Original Nuclear Option assets, vehicle designs, audio,
> and code are Copyright (c) 2026 Shockfront Studios Pty Ltd. All rights reserved. Nuclear Option
> and Shockfront Studios are trademarks or registered trademarks of Shockfront Studios Pty Ltd.
> Original mod content and all other trademarks belong to their respective owners.

It is free and it is not a standalone product. Nuclear Option's EULA, in the version that takes
effect on 1 January 2027 or on downloading or launching version 0.35 of the game, a beta or
public-test branch of it included, if that comes first, forbids selling or monetising mods, and
this is a mod: that restriction comes from Shockfront, not from the licence above, and from then it
binds everyone bound by that agreement, anyone who downloads, installs, copies or plays the game.

**It contains no Nuclear Option assets.** The bundle ships placeholder materials with no textures
and no shaders in them; the plugin swaps each one for the equivalent material from the player's own
copy of the game when the map loads. The same goes for the trees, the grass and the buildings - the
map says where they stand, the game provides what stands there. Nothing here works, or is of any
use, without the game.
