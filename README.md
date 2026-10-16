# Open Night Train Database (ONTD)

The Open Night Train Database is [Back-on-Track](https://back-on-track.eu/about/)'s database of night trains in Europe. Volunteers keep it up to date, and it powers our [night train map](https://back-on-track.eu/night-train-map/).

This repository holds a copy of the data. It is refreshed automatically twice a day, so anyone can download it, build on it, or help us improve it.

Back-on-Track is a European network of people and organisations who campaign for more and better night trains. You can read [how we work](https://back-on-track.eu/how-we-work/) and find a [group near you](https://back-on-track.eu/groups/).

## At a glance

In October 2026 the database lists **about 200 night train routes** run by **about 30 operators**, from Inverness to Istanbul and from Kyiv to Palermo. The exact numbers change as trains start, stop or change, so check `data/latest/` for the current state.

## Find your way

| I want to… | Go here |
|---|---|
| See the night trains on a map | [Night train map](https://back-on-track.eu/night-train-map/) |
| Read about the database | [Open Night Train Database](https://back-on-track.eu/open-night-train-database/) and the [editors' guide](https://back-on-track.eu/how-to-open-night-train-database-ontd/) |
| Download the data | [`data/latest/`](data/latest/) (JSON files) |
| Report a mistake or a missing train | [Open an issue](../../issues/new/choose) |
| Help as a volunteer or developer | [CONTRIBUTING.md](CONTRIBUTING.md) and our [open tasks](https://back-on-track.eu/open-tasks/) |
| Design the night train network of 2032 | [Target Network tool](https://targetnetwork.back-on-track.eu/) ([about the project](https://back-on-track.eu/project-target-network-2032/)) |
| Book a night train | [How to book a night train](https://back-on-track.eu/how-to-book-a-night-train/) |

## What's in the data

The structure is inspired by [GTFS](https://gtfs.org/), the common format for public transport timetables. Every file in [`data/latest/`](data/latest/) is a JSON object keyed by its ID.

| File | What it holds |
|---|---|
| `agencies.json` | The train operators |
| `routes.json` | Night train routes, one per line (for example Vienna to Hamburg) |
| `trips.json` | The trips on each route, usually one per direction, with times, travel classes and on-board facilities |
| `trip_stop.json` | The stops of each trip, with arrival and departure times |
| `stops.json` | Stations. A large reference list, not only the stations night trains call at |
| `calendar.json`, `calendar_dates.json` | When the trains run, and the exceptions |
| `classes.json` | Travel classes (seat, couchette, sleeper) |
| `translations.json` | Names of operators and stations in other languages |
| `view_ontd_map.json`, `view_ontd_list.json`, `view_ontd_details.json`, `view_ontd_cities.json` | Ready-made views used by the map and the lists on our website |

## How the data gets here

1. Volunteers edit the database in a shared Google Sheet.
2. A small Apps Script ([`scripts/code.gs`](scripts/code.gs)) serves each sheet as JSON.
3. A GitHub Action runs [`scripts/get_snapshot.py`](scripts/get_snapshot.py) every day at 02:00 and 14:00 UTC and saves the result in [`data/latest/`](data/latest/).

Because the files in `data/` are overwritten twice a day, please don't edit them by hand. If something is wrong, [open an issue](../../issues/new/choose) and we'll fix it in the sheet.

If you need a fresh copy right away, run `python3 scripts/get_snapshot.py`, or download a single table from the hosted script:
`https://script.google.com/macros/s/AKfycbwY9zNQFq0urCHsTstWRKxLe0SstWrwyY04tSuDIVb_yRCtTs_HDlRARS-5fqltgEZr/exec?table=<name>`, where `<name>` is one of the file names above without `.json`.

## Licence

The night train data in this repository (everything under `data/`, and the same database served through the sheet and the API) is the **Open Night Train Database** by Back-on-Track Europe. It is licensed under the **[Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/)**, see [`LICENSE-DATA`](LICENSE-DATA). The individual contents of the database are licensed under the **[Database Contents License (DbCL) 1.0](https://opendatacommons.org/licenses/dbcl/1-0/)**, see [`LICENSE-DATA-CONTENTS`](LICENSE-DATA-CONTENTS). This is the same set-up OpenStreetMap uses; part of our station coordinates come from OpenStreetMap.

In practice: you can use the data, also commercially, as long as you credit **Back-on-Track Europe** with a link to [back-on-track.eu](https://back-on-track.eu/), and if you share an adapted version of the database, you share it under the ODbL as well.

Suggested attribution: `Night train data © Back-on-Track Europe, Open Night Train Database (ODbL 1.0), back-on-track.eu`

The code in this repository (`scripts/` and the workflow files) is licensed under the **GNU General Public License v3.0**, see [`LICENSE`](LICENSE).

The night train **map artwork** on back-on-track.eu is not part of this repository and stays under **CC BY-NC-ND 4.0**, credit "Juri Maier / Back-on-Track.eu".

Decided by the Back-on-Track Europe board, 2026.

## Who looks after this

Back-on-Track volunteers. Questions about the data: [open an issue](../../issues/new/choose). Anything else: [contact us](https://back-on-track.eu/contact/). Want to support our work? [Become a member](https://back-on-track.eu/become-a-member/) or [donate](https://back-on-track.eu/donate/).
