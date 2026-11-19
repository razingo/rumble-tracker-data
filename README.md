# Rumble Collection Tracker: game data

The game data used by the **[Rumble Collection Tracker](https://github.com/razingo/rumble-tracker-app)**, an unofficial
collection, army and event tracker for Warcraft Rumble on PC. After a game patch, new minis, events and shop offers
reach players through this repository, without a new version of the app.

**Not affiliated with or endorsed by Blizzard Entertainment.** The game art and data here belong to Blizzard; see
[NOTICE.md](NOTICE.md).

## What's in it

| What | Where |
|---|---|
| Minis: names, descriptions, traits, talents, stats | `minis.json`, `talents/` |
| Unit IDs and army codes | `unit_ids.json`, `army_code_minis.json` |
| Events: schedules, reward trees, ticket totals | `events.json`, `events/`, `rewards/` |
| Shop offers and G.R.I.D. prices | `store.json`, `store/` |
| Game rules: currencies, army slots, upgrade costs | `rules.json`, `currency/` |
| Mini portraits, icons, card frames and boards | `art/`, `icons/`, `ui/` |
| The list of files with their checksums, and the game build they come from | `manifest.json` |
| The signature of that list | `manifest.sig` |

The files are served as they are from GitHub Pages: <https://razingo.github.io/rumble-tracker-data/>.

## How the tracker uses it

The tracker checks `manifest.json` when it starts and every 6 hours. When the pack has changed, it downloads only the
files it doesn't already have and installs the new pack, but only when:

- `manifest.sig` is a valid Ed25519 signature of `manifest.json`, made with the key whose public half is built into
  the tracker, and
- every file matches the SHA-256 checksum listed in `manifest.json`.

So nobody else can push data to players' trackers, and a damaged or altered file is never used. The check downloads
files only: it sends nothing about the player.

This is also the only copy of the game data: to run or build the tracker from source, `npm run fetch-gamedata` (in
the [rumble-tracker-app](https://github.com/razingo/rumble-tracker-app) repository) downloads it into `gamedata/`
with the same checks.

## Problems

Wrong or missing game data (a mini, an event, a price)? Use **Report a problem** in the tracker, or open an issue in
[rumble-tracker-app](https://github.com/razingo/rumble-tracker-app/issues).
