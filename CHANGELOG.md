# Changelog

All notable changes to this project will be documented in this file.

## v0.3.6 (2026-04-16)
* **NEPAC Support**: Added ability to parse the Northeast and North Central Pacific HURDAT2 dataset.
    * New `basin` argument in `Hurdat2` class (defaults to `'atl'`, supports `'nepac'`).
    * Updated `_get_data_from_url` to handle both 6-digit (`MMDDYY`) and 8-digit (`MMDDYYYY`) date formats found on the NHC server.
    * Updated cache filenames to include the basin name (`hurdat2_{basin}_latest.txt`) to prevent Atlantic and Pacific data from overwriting each other.

* Moved the full version history from `README.md` to this dedicated `CHANGELOG.md` file.

## v0.3.5 (2026-01-22)
* Added logo to `README.md`.

## v0.3.4 (2026-01-15)
* Minor updates to `README.md`.
* **Initial release** on [GitHub](https://github.com/andy-theia/hurdat2py).

## v0.3.3 (2026-01-15)
* Major overhaul of `README.md` to include API reference tables and additional information.

## v0.3.2 (2026-01-12)
* Minor updates to `README.md`.

## v0.3.1 (2026-01-12)
* **Initial release** on [PyPI](https://pypi.org/project/hurdat2py/).