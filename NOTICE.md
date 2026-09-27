# Notices and attributions

Swiss Alps is real terrain, real roads and real airfields. Public data made that possible, and the
two providers whose data needs a credit ask for something in return. This file is what they ask
for: it travels with the map, and with anything made from the map that still holds data derived
from the Copernicus DEM, and anything made from the map that still holds data derived from
swisstopo's owes swisstopo the same credit. Keep it beside the bundle wherever the bundle goes.

---

## Terrain: Copernicus DEM GLO-30

The heightfield is derived from the Copernicus DEM, instance GLO-30, in its free, full and open
form (`COP-DEM-GLO-30-F`) as published in the public AWS bucket
`https://copernicus-dem-30m.s3.amazonaws.com/`. The terrain here is adapted from it (resampled,
re-datumed, lowlands compressed, lake beds cut, a coastline added, and the ground cut and levelled
for the airfields and the roads), so it carries the licence's **modified-data** notice:

> produced using Copernicus WorldDEM-30 © DLR e.V. 2010-2014 and © Airbus Defence and Space GmbH
> 2014-2018 provided under COPERNICUS by the European Union and ESA; all rights reserved

Article 6 of the same licence, on the user's obligations, asks for three more things, which are as
much a part of this notice as the line above. Only the first comes with a sentence to copy; the
other two are duties that set no wording, and the statements given for them are how this map meets
them:

- **Liability.** The licence dictates this sentence, and it is quoted here word for word:

  > The organisations in charge of the Copernicus programme by law or by delegation do not incur
  > any liability for any use of the Copernicus WorldDEM-30

- **No endorsement.** Nobody who receives this map, or anything made from it that still holds data
  derived from the Copernicus DEM, may give the public the impression that their activities, what
  they do with this map among them, are officially endorsed by Airbus Defence and Space (the data's
  provider), the body that offers the DEM under the Copernicus licence (its Licensor), or anyone
  else in charge of Copernicus or of delivering its data. None of them endorses it: Airbus Defence
  and Space, DLR, ESA, the European Union and Copernicus do not endorse this map, its author or any
  use made of it. It is a game map, not a survey product, and nothing in it should be taken as
  authoritative elevation data.
- **Flow-down.** Whoever got the data from the Licensor, as this map's author did, and lets others
  distribute it or show it to the public has to make sure they are bound by the obligations above.
  The author lets everyone who receives the map pass it on and show it: the map itself under CC BY
  4.0, which offers it to every recipient, and the Copernicus-derived data in it on these
  obligations. So anyone who receives this map, or anything made from it that still holds data
  derived from the Copernicus DEM, is bound by the modified-data notice, the liability sentence and
  the no-endorsement duty, and this file is how they reach you. Pass it on with the map.

Licence text:
<https://documentation.dataspace.copernicus.eu/APIs/SentinelHub/Data/DEM/resources/license/License-COPDEM-30.pdf>

Citation, where one is wanted: <https://doi.org/10.5270/ESA-c5d3d65>.

The restricted instance of the same product (`-R`) carries a non-commercial clause. It is not what
this map was built from, and its terms do not apply here, but if you rebuild the terrain from
tiles of your own, check which instance you fetched.

---

## Roads and airfields: swissTLMRegio and swissTLM3D, Federal Office of Topography swisstopo

The road network is derived from swissTLMRegio (its 2025 edition, downloaded on 20 September 2026),
swisstopo's generalised landscape model, and so, in part, is the built-up field that decides where
towns and farmland go: it is worked out from the density of those roads and a short table of town
centres. Despite its name, swissTLMRegio is not limited to Switzerland: it covers the bordering
countries too, which is why the French and Italian quarter of this map has roads on it.

The paving of the airfields (Geneva, Zurich, Payerne, Meiringen, Sion and Bern) is derived from
swissTLM3D (release 2026-02, version 2.4), swisstopo's detailed landscape model: its surveyed
taxiways and aprons, and the end pads where a real runway runs on past the map's, fitted to each map
runway by the real runway and redrawn in simpler shapes. At Zurich the survey also gives Kloten's
other two runways, 16/34 and 10/28, moved and turned with the rest of its layout. Each field's main
runway is not swisstopo's; the table below says where it comes from. Both products come under the
same terms, so the one source reference below covers both.

> © swisstopo

swisstopo publishes both as open government data. The one condition its terms of use set themselves
is naming the source:

> The free geodata and geoservices of swisstopo may be used, distributed and made accessible.
> Furthermore, they may be enriched and processed and also used commercially.

with the condition that

> In the case of digital or analogue representations and publications, as well as in the case of
> dissemination, one of the following source references must be attached in any case

The reference given above, `© swisstopo`, is the shortest of the six accepted forms: the terms print
it `©swisstopo` and swisstopo's own FAQ `© swisstopo`. The others are the office's name in German,
French, Italian, Romansh and English, the English being *Federal Office of Topography swisstopo*.
For data derived from theirs, as this is, the requirement is the same and the reference may be
preceded by "derived from".

The same terms bring in the general terms of use of the Federal Spatial Data Infrastructure FSDI,
which ask that processed data be published under the name of the data user, meaning whoever
obtained the data from the FSDI. This map's author obtained it, and the map is published under the
author's name, as LICENSE says; swisstopo did not make it and does not endorse it.

Terms of use: <https://www.swisstopo.admin.ch/en/terms-of-use-free-geodata-and-geoservices>.
The FSDI's general terms: <https://www.geo.admin.ch/en/general-terms-of-use-fsdi>.
Where the reference belongs, including their guidance for video games:
<https://www.swisstopo.admin.ch/en/source-reference-ogd-swisstopo>.
The products themselves: <https://www.swisstopo.admin.ch/en/landscape-model-swisstlmregio> and
<https://www.swisstopo.admin.ch/en/landscape-model-swisstlm3d>.

There is no share-alike here. Nothing in swisstopo's terms constrains what you license your own work
under, and nobody downstream inherits from them a condition on the map as a whole. The one thing
that does carry is the source reference itself: swisstopo asks the same of derived data as of its
own, so anyone who passes the map on, or builds a further work from these roads or airfields, owes
swisstopo the same line of credit.

### Where the credit is

Not only in this file. The bundle carries it too, in the manifest as the `credits` field of the
TextAsset `map`, and stamped into the chart image a player opens in flight, where the chart's small
font draws each © as (c). That attaches the reference to every copy of the file, which is what
swisstopo's terms ask of dissemination. Their guidance for video games calls it ideal to put the
source beside the data wherever it appears, and acceptable to name it where the game lists its
source references; this game gives a map neither, and the chart is the nearest it has.

---

## Which shipped asset comes from where

Asset names are the names inside the bundle.

| Asset | What it is | Source |
|---|---|---|
| `tile_<tx>_<tz>`, 6,084 meshes over 1,521 tiles | the terrain surface: LOD0, LOD1, LOD2 and a collider per 5,120 m tile | **Copernicus**, modified. Heights are the DEM less a 368 m datum, sampled at 51.2 m, with the lowlands compressed, the lake beds cut and a coastal ramp cut at the map's edge. The ground is also shaped from **swisstopo** data: levelled for each airfield inside an outline drawn round its runways and swissTLM3D paving and eased into the land around it, and levelled under the swissTLMRegio roads and dug out where they run in cuttings. LOD0 and the colliders leave out any ground standing inside a road tunnel |
| `swissalps_roads`, TextAsset | the road network the game paths and drives on | **swisstopo**, re-projected from LV95 and re-classified |
| `road_<tx>_<tz>` and their `_LOD1`, `_LOD2`; `bridge_<n>_deck`, `_concrete`, `_parapets` and their LODs; `tunnel_<n>_deck`, `_liner`, `_portals`, `_shell`; `junction_<n>_liner`, `_portals`, `_shell` | the road ribbons you see and drive on, and the bridges, tunnels and tunnel junctions that carry them | meshed from the same **swisstopo** geometry. The survey flags its bridges and tunnels; the ground then decides which are built as such, and where tunnels meet |
| `runway_<field>_<n>` | each field's main runway | ours: a strip between two thresholds set for the map. Payerne, Meiringen (slid 186 m east), Sion and Bern lie on their real runways' lines, taken from OurAirports' public-domain runway data; Geneva's was first drawn by hand in the map editor, about 5.8 km north of the real runway, then turned north-south and moved 300 m east to keep its blend off the map's coastal sea, and Zurich stands on the Reuss plain because Kloten lies in that sea |
| `runway_zurichairport_1_2` (16/34), `runway_zurichairport_1_3` (10/28) | Zurich's other two runways | **swisstopo**'s swissTLM3D runways, each as long as its surveyed paving (3,749 m and 2,636 m), moved and turned with the rest of Kloten's layout; their 45 m width, the main runway's, is ours |
| `tarmac_<field>_<n>_0_concrete`, `tarmac_<field>_<n>_1_asphalt` | aprons (concrete) and taxiways (asphalt) | **swisstopo**'s swissTLM3D paving, with the end pads where a real runway runs on past the map's, fitted to each map runway and redrawn in simpler shapes |
| `floor_<field>_<n>` | an invisible collider over each field's outline | ours, the outline drawn round the runways and the **swisstopo**-derived paving |
| `swissalps_airbases`, TextAsset, `NOAIRB05` | each airbase's name, side, main runway, outline and other runways; the plugin builds the game's airbases from it when the map loads | ours, with Zurich's other runways and every outline derived from **swisstopo**'s swissTLM3D |
| `swissalps_macro`, 8192² | macro ground colour | our rendering of the **Copernicus**-derived terrain, coloured by height, with a built-up wash over the towns from the urban field (the density of the **swisstopo** road network and a short table of town centres). No road is painted into it; the ribbons draw them |
| `swissalps_map`, 2048² | the tactical chart, with the data credit stamped on it | our rendering of the **Copernicus**-derived terrain (relief, 500 m contours, coast and lake shores), with the **swisstopo** road network and the built-up wash drawn on it |
| `swissalps_cities`, `NOCITY01` | where buildings stand | ours. The road network and the table of town centres decide where towns are dense; the roads keep buildings off carriageways and set the angle each one faces |
| `swissalps_trees` | where trees stand | ours, from the same density model, with a clearance kept along every road |
| `swissalps_splat_grass` / `_rock` / `_lush` / `_fields`, 4096² each | ground-cover weights | ours, from terrain and the same density model |
| `swissalps_color` 1024², `swissalps_ocean_basecolor` and `swissalps_ocean_depth` 2048² | terrain colour lookup, ocean colour and depth | ours, derived from the terrain |
| `map`, TextAsset | the manifest: sizes, grid, lakes, asset names, credit, notice | ours, except the lakes' surface levels and extents, which are measured from the **Copernicus** DEM; their names are ours |
| `SwissAlps` prefab with `Terrain`, `Water`, `Roads` and `Airfields`; the lake surfaces `lake_<name>_<n>` under `Water/Lake_<name>` | the map's structure and its water | ours; each lake surface follows the outline, and sits at the level, that the **Copernicus** DEM shows |
| `__BORROW__…` materials | placeholders, one per surface kind | ours. They hold no texture and no shader from the game; the plugin swaps each for the player's own copy of the game's material at load |

`NOROAD01` (roads), `NOCITY01` (buildings) and `NOAIRB05` (airbases) are this project's own
little-endian formats, written by its tools and read by the plugin. Nothing in them comes from the
game except, in the airbase file, the names of the game's two factions, Boscali and Primeva, which
each airbase belongs to.

No Nuclear Option asset is in the bundle. Every material the map needs at runtime is borrowed from
the player's installation when the map loads, which is why the placeholders exist and why a player
without the game has nothing of the game in these files.

---

## Nuclear Option

Nuclear Option's end-user licence agreement, in the version that takes effect on 1 January 2027 or
on downloading or launching version 0.35 of the game, a beta or public-test branch of it included,
if that comes first, requires any mod that uses the game's assets, code or trademarks to display
this prominently, and it is quoted here word for word:

> This project is an unofficial community modification and is not affiliated with, sponsored by, or
> endorsed by Shockfront Studios Pty Ltd. Original Nuclear Option assets, vehicle designs, audio,
> and code are Copyright (c) 2026 Shockfront Studios Pty Ltd. All rights reserved. Nuclear Option
> and Shockfront Studios are trademarks or registered trademarks of Shockfront Studios Pty Ltd.
> Original mod content and all other trademarks belong to their respective owners.

In the project's own words: this map is not a standalone product, it does nothing without a copy of
Nuclear Option that the player already owns, and it ships no file belonging to the game. The same
version of the EULA forbids selling or monetising mods, so this one is given away; that restriction
is Shockfront's and from that version's effective date binds everyone bound by that agreement,
anyone who downloads, installs, copies or plays the game, whatever CC BY 4.0 permits in the
abstract. Read the current agreement at
<https://store.steampowered.com/eula/2168680_eula_0>: the version quoted here was current when this
was written, and until it takes effect the previously published version governs, so check which one
binds you.

---

## Summary of licences

| What | Licence |
|---|---|
| The map as a produced work: meshes, textures, placements, arrangement | CC BY 4.0, see LICENSE |
| Terrain heights, and the lakes' outlines and levels, as Copernicus-derived data | Copernicus DEM licence, notices above |
| Road network and airfield paving, and what is derived from them, as swisstopo-derived data (swissTLMRegio, swissTLM3D) | swisstopo open government data, source reference above |
| Main runway lines at Payerne, Meiringen, Sion and Bern | OurAirports runway data, public domain |
| Nuclear Option itself | Shockfront Studios. Not distributed here |
