# Helping with the Open Night Train Database

Thanks for wanting to help! The database is kept up to date by volunteers, and most ways to help need no coding at all.

## Spotted a mistake?

A wrong time, a train that no longer runs, a missing stop: [open an issue](../../issues/new/choose) with the **Data error** form. Please add a source if you have one, like the operator's website or a timetable. That makes the fix quick.

## Know a night train that's missing?

Use the **Missing night train** form in the [issues](../../issues/new/choose). Tell us where it runs, who runs it, and where you found it.

## Want to help keep the data up to date?

Our volunteers edit the database in a shared sheet, and we always welcome more hands. Open an issue to say hello, or have a look at Back-on-Track's [open tasks](https://back-on-track.eu/open-tasks/). We'll show you how it works and give you access.

## Are you a developer?

The code here is small: a Python script ([`scripts/get_snapshot.py`](scripts/get_snapshot.py)), an Apps Script ([`scripts/code.gs`](scripts/code.gs)) and a GitHub Action that runs twice a day.

1. Fork the repository and create a branch.
2. Make your change and describe it in a pull request.
3. Please don't change the files in `data/` by hand: the Action overwrites them twice a day. Data fixes go through the sheet, so report them as an issue.

Ideas and questions are welcome in the issues too.

## Other ways to help Back-on-Track

- Join a [local group](https://back-on-track.eu/groups/)
- Pick up an [open task](https://back-on-track.eu/open-tasks/)
- [Become a member](https://back-on-track.eu/become-a-member/) or [donate](https://back-on-track.eu/donate/)

## Be kind

We're all volunteers. Be friendly and patient with each other, and assume good intentions.

By contributing data, you agree that it is published under the [ODbL 1.0](LICENSE-DATA), like the rest of the database. Code contributions are published under the [GPL-3.0](LICENSE).
