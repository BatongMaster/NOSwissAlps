# Notices and attributions

Swiss Alps is real terrain and real roads. Two public data sets made that possible, and both ask
for something in return. This file is what they ask for: it travels with the map, and with anything
made from the map. Keep it beside the bundle wherever the bundle goes.

---

## Terrain: Copernicus DEM GLO-30

The heightfield is derived from the Copernicus DEM, instance GLO-30, in its free, full and open
form (`COP-DEM-GLO-30-F`) as published in the public AWS bucket
`https://copernicus-dem-30m.s3.amazonaws.com/`. The terrain here is adapted from it (resampled,
re-datumed, coastline added) so it carries the licence's **modified-data** notice:

> produced using Copernicus WorldDEM-30 © DLR e.V. 2010-2014 and © Airbus Defence and Space GmbH
> 2014-2018 provided under COPERNICUS by the European Union and ESA; all rights reserved

The same licence asks for three more things, which are as much a part of this notice as the line
above:

- **Liability.** The licence dictates this sentence, and it is quoted here word for word:

  > The organisations in charge of the Copernicus programme by law or by delegation do not incur
  > any liability for any use of the Copernicus WorldDEM-30

- **No endorsement.** Airbus Defence and Space, DLR, ESA, the European Union and Copernicus do not
  endorse this map, its author or any use made of it. It is a game map, not a survey product, and
  nothing in it should be taken as authoritative elevation data.
- **Flow-down.** Anyone who receives this map, or anything derived from it, receives it on these
  same obligations and has to pass them on in turn. Redistributing the map means redistributing
  this file with it.

Licence text:
<https://documentation.dataspace.copernicus.eu/APIs/SentinelHub/Data/DEM/resources/license/License-COPDEM-30.pdf>

Citation, where one is wanted: <https://doi.org/10.5270/ESA-c5d3d65>.

The restricted instance of the same product (`-R`) carries a non-commercial clause. It is not what
this map was built from, and its terms do not apply here, but if you rebuild the terrain from
tiles of your own, check which instance you fetched.

---

## Roads: swissTLMRegio, Federal Office of Topography swisstopo

The road network, and the built-up field that decides where towns and farmland go, are derived from
swissTLMRegio, swisstopo's generalised landscape model. Despite the name it is not limited to
Switzerland: it covers the bordering countries too, which is why the French and Italian quarter of
this map has roads on it.

> © swisstopo

swisstopo publishes it as open government data. The whole of the obligation is naming the source:

> The free geodata and geoservices of swisstopo may be used, distributed and made accessible.
> Furthermore, they may be enriched and processed and also used commercially.

with the condition that

> In the case of digital or analogue representations and publications, as well as in the case of
> dissemination, one of the following source references must be attached in any case

`©swisstopo` is the shortest of the six accepted forms; the others are the office's name in
German, French, Italian, Romansh and English, the English being *Federal Office of Topography
swisstopo*. For data derived from theirs, as this is, the requirement is the same and the reference
may be preceded by "derived from".

Terms of use: <https://www.swisstopo.admin.ch/en/terms-of-use-free-geodata-and-geoservices>.
Where the reference belongs, including their guidance for video games:
<https://www.swisstopo.admin.ch/en/source-reference-ogd-swisstopo>.
The product itself: <https://www.swisstopo.admin.ch/en/landscape-model-swisstlmregio>.

There is no share-alike here and no database right asserted over the geometry. Nothing constrains
what you license your own work under, and nobody downstream inherits a condition on the map as a
whole. The one thing that does carry is the source reference itself: swisstopo asks the same of
derived data as of its own, so anyone who builds a further work from these roads owes swisstopo
the same line of credit. That is the entire obligation, in both directions.

### Where the credit is

Not only in this file. The bundle carries it too, in the manifest as the `credits` field of the
TextAsset `map`, and stamped into the chart image a player opens in flight. It travels with the map
even when this repository does not, which is what swisstopo's guidance for games asks for.

---

## Which shipped asset comes from where

Asset names are the names inside the bundle.

| Asset | What it is | Source |
|---|---|---|
| `tile_<tx>_<tz>`, 6,084 meshes over 1,521 tiles | the terrain surface: LOD0, LOD1, LOD2 and a collider per 5,120 m tile | **Copernicus**, modified. Heights are the DEM less a 368 m datum, sampled at 51.2 m, with the lowlands compressed and a coastal ramp cut at the map's edge |
| `swissalps_roads`, TextAsset | the road network the game paths and drives on | **swisstopo**, re-projected from LV95 and re-classified |
| `road_<tx>_<tz>` and their LODs, with bridge and tunnel geometry | the road ribbons you see and drive on | meshed from the same swisstopo geometry |
| `swissalps_macro`, 8192² | macro ground colour | our rendering, with the road network painted into it |
| `swissalps_map`, 2048² | the tactical chart, with the data credit stamped on it | our rendering, with the road network drawn on it |
| `swissalps_cities`, `NOCITY01` | where buildings stand | ours. The road network decides where towns are dense, keeps buildings off carriageways, and sets the angle each one faces |
| `swissalps_trees` | where trees stand | ours, from the same density model, with a clearance kept along every road |
| `swissalps_splat_grass` / `_rock` / `_lush` / `_fields`, 4096² each | ground-cover weights | ours, from terrain and the same density model |
| `swissalps_color` 1024², `swissalps_ocean_basecolor` and `swissalps_ocean_depth` 2048² | terrain colour lookup, ocean colour and depth | ours, derived from the terrain |
| `map`, TextAsset | the manifest: sizes, grid, lakes, asset names, credit, notice | ours |
| `SwissAlps` prefab, `Terrain`, `Roads`, `Lake_<name>` quads | the map's structure and its water | ours |
| `__BORROW__…` materials | placeholders, one per surface kind | ours. They hold no texture and no shader from the game; the plugin swaps each for the player's own copy of the game's material at load |

`NOROAD01` (roads) and `NOCITY01` (buildings) are this project's own little-endian formats, written
by the generator and read by the plugin. Nothing in either comes from the game.

No Nuclear Option asset is in the bundle. Every material the map needs at runtime is borrowed from
the player's installation when the map loads, which is why the placeholders exist and why a player
without the game has nothing of the game in these files.

---

## Nuclear Option

Nuclear Option's end-user licence agreement asks a mod to display this, and it is quoted here word
for word:

> This project is an unofficial fan modification not affiliated with, sponsored by, or endorsed by
> Shockfront Studios. All original Nuclear Option assets and code are Copyright © 2026 Shockfront
> Studios. Shockfront Studios and Nuclear Option are trademarks of Shockfront Studios. All other
> trademarks and original mod content belong to their respective owners.

In the project's own words: this map is not a standalone product, it does nothing without a copy of
Nuclear Option that the player already owns, and it ships no file belonging to the game. The EULA
forbids selling or monetising mods, so this one is given away; that restriction is Shockfront's and
applies to anyone who passes the map on, whatever CC BY 4.0 permits in the abstract. Read the
current agreement at <https://store.steampowered.com/eula/2168680_eula_0>: the version drafted when
this was written carried an effective date of 1 January 2027, so check which one binds you.

---

## Summary of licences

| What | Licence |
|---|---|
| The map as a produced work: meshes, textures, placements, arrangement | CC BY 4.0, see LICENSE |
| Terrain heights, as Copernicus-derived data | Copernicus DEM licence, notices above |
| Road geometry, as swisstopo-derived data | swisstopo open government data, source reference above |
| Nuclear Option itself | Shockfront Studios. Not distributed here |
