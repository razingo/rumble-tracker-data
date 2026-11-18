# Notices

## Not affiliated with Blizzard Entertainment

Rumble Collection Tracker is an unofficial fan tool. It is not affiliated with, endorsed, sponsored or approved by
Blizzard Entertainment, Inc. Warcraft, Warcraft Rumble and Blizzard Entertainment are trademarks or registered
trademarks of Blizzard Entertainment, Inc. in the U.S. and/or other countries.

## What the MIT license covers

The MIT license in `LICENSE` covers the tracker's own source code only: the files under `poc/` that make up the app
(server, page scripts, styles) and the build scripts under `research/gamedata/`.

It does **not** cover the material below, which belongs to its owners and is included only so the tracker can show
your collection in a recognisable way.

## Game art and data © Blizzard Entertainment

These are extracted from the game's files by `research/gamedata/` and shipped in `poc/static/` or in data packs:

- images: mini portraits (`static/art`), talent icons (`static/talents`), card frames, boards and textures
  (`static/ui`), faction, trait and tag icons (`static/icons`), event tickets (`static/events`), event reward icons
  (`static/rewards`), shop art (`static/store`) and currency icons;
- data: mini names, descriptions, traits, talents and stats (`minis.json`), event schedules, reward trees and ticket
  totals (`events.json`), shop offers and G.R.I.D. prices (`store.json`), army boards and unit IDs (`minis.json`,
  `unit_ids.json`, `army_code_minis.json`).

© Blizzard Entertainment, Inc. All rights reserved. If Blizzard asks for any of it to be removed, it will be.

## The player's own data

The tracker reads Warcraft Rumble's saved settings from the Windows registry on the player's own PC, read-only, and
keeps everything it stores in its own data folder on that PC. It sends nothing anywhere. The only network request it
makes is the optional data-pack check (see README), which downloads files and sends no player data.
