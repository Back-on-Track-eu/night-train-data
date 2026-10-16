# night-train-data

This repository provides a version of static data from the Back-on-Track night trains database which can be used for various purposes including the [night train map](https://back-on-track.eu/night-train-map/) on the BoT website.

Data is currently stored in a Google Sheets and this can be extracted as .json files for use with the night train map and other resources. 

A Google Apps script has been developed to extract the Google Sheets data, which can be found here: [code.gs](./scripts/code.gs).

A hosted version of the script is [here](https://script.google.com/macros/s/AKfycbwY9zNQFq0urCHsTstWRKxLe0SstWrwyY04tSuDIVb_yRCtTs_HDlRARS-5fqltgEZr/exec) and can be used for one-off .json file creation.

## How to update the data held in this repository
There are several options for updating the data
1. For developers (mainly): If you are using git locally you can get update with this python script - [get_snapshot.py](./scripts/get_snapshot.py) which uses the currently hosted version of the script. Then create a pull request with the new files and they will get merged when approved, or if youv'e got the permissions and feeling brave, just commit.
2. Manual approach: Click the following links for the data you want:
- [view_ontd_map](https://script.google.com/macros/s/AKfycbwY9zNQFq0urCHsTstWRKxLe0SstWrwyY04tSuDIVb_yRCtTs_HDlRARS-5fqltgEZr/exec?table=view_ontd_map)
- [view_ontd_list](https://script.google.com/macros/s/AKfycbwY9zNQFq0urCHsTstWRKxLe0SstWrwyY04tSuDIVb_yRCtTs_HDlRARS-5fqltgEZr/exec?table=view_ontd_list)
- [agencies](https://script.google.com/macros/s/AKfycbwY9zNQFq0urCHsTstWRKxLe0SstWrwyY04tSuDIVb_yRCtTs_HDlRARS-5fqltgEZr/exec?table=agencies)
- [stops](https://script.google.com/macros/s/AKfycbwY9zNQFq0urCHsTstWRKxLe0SstWrwyY04tSuDIVb_yRCtTs_HDlRARS-5fqltgEZr/exec?table=stops)
- [routes](https://script.google.com/macros/s/AKfycbwY9zNQFq0urCHsTstWRKxLe0SstWrwyY04tSuDIVb_yRCtTs_HDlRARS-5fqltgEZr/exec?table=routes)
- [trips](https://script.google.com/macros/s/AKfycbwY9zNQFq0urCHsTstWRKxLe0SstWrwyY04tSuDIVb_yRCtTs_HDlRARS-5fqltgEZr/exec?table=trips)
- [trip_stop](https://script.google.com/macros/s/AKfycbwY9zNQFq0urCHsTstWRKxLe0SstWrwyY04tSuDIVb_yRCtTs_HDlRARS-5fqltgEZr/exec?table=trip_stop)
- [calendar](https://script.google.com/macros/s/AKfycbwY9zNQFq0urCHsTstWRKxLe0SstWrwyY04tSuDIVb_yRCtTs_HDlRARS-5fqltgEZr/exec?table=calendar)
- [calendar_dates](https://script.google.com/macros/s/AKfycbwY9zNQFq0urCHsTstWRKxLe0SstWrwyY04tSuDIVb_yRCtTs_HDlRARS-5fqltgEZr/exec?table=calendar_dates)
- [translations](https://script.google.com/macros/s/AKfycbwY9zNQFq0urCHsTstWRKxLe0SstWrwyY04tSuDIVb_yRCtTs_HDlRARS-5fqltgEZr/exec?table=translations)
- [classes](https://script.google.com/macros/s/AKfycbwY9zNQFq0urCHsTstWRKxLe0SstWrwyY04tSuDIVb_yRCtTs_HDlRARS-5fqltgEZr/exec?table=classes)

When you have the data, upload using the GitHub user interface.
For further details on using the GitHub user interface see this article: https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files

## Licence

The night train data in this repository (everything under `data/`, and the same database served through the sheet and the API) is the **Open Night Train Database** by Back-on-Track Europe. It is licensed under the **[Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/)**, see [`LICENSE-DATA`](LICENSE-DATA). The individual contents of the database are licensed under the **[Database Contents License (DbCL) 1.0](https://opendatacommons.org/licenses/dbcl/1-0/)**, see [`LICENSE-DATA-CONTENTS`](LICENSE-DATA-CONTENTS). This is the same set-up OpenStreetMap uses; part of our station coordinates come from OpenStreetMap.

In practice: you can use the data, also commercially, as long as you credit **Back-on-Track Europe** with a link to [back-on-track.eu](https://back-on-track.eu/), and if you share an adapted version of the database, you share it under the ODbL as well.

Suggested attribution: `Night train data © Back-on-Track Europe, Open Night Train Database (ODbL 1.0), back-on-track.eu`

The code in this repository (`scripts/` and the workflow files) is licensed under the **GNU General Public License v3.0**, see [`LICENSE`](LICENSE).

The night train **map artwork** on back-on-track.eu is not part of this repository and stays under **CC BY-NC-ND 4.0**, credit "Juri Maier / Back-on-Track.eu".

Decided by the Back-on-Track Europe board, 2026.
