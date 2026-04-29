# Changelog & Roadmap

*All notable changes to this project will be documented in this file*

## 🗺️ Roadmap

* **Improved Plotting Functionality**: Add/improve plotting functions.
    * Expected: Summer 2026
* **Wind Radius Implementation**: Add support for and methods utilizing wind radius data included with modern records in the Hurdat2 dataset.
    * Expected: Fall 2026
* **Statistics Improvements**: Implement new statistics functionality for `Storm` and `Season` objects.
    * Expected: Fall 2026

## 📜 Changelog

## v0.4.0 (2026-04-29)
* The **`TropicalCyclone`** class has been renamed to **`Storm`**. The old name remains as an alias but will be removed in v0.5.0.

* **Minimum Python Version**: 
    * Increased the minimum requirement to Python 3.9+.
    * Explicitly declared support for Python versions 3.9 through 3.13 within the package metadata.

* **`rank_seasons_by_ace`** is now deprecated, and will be removed in v0.5.0.
    * To keep the package lightweight and focused on data access, specialized ranking functions are being phased out in favor of user-driven analysis via `to_dataframe()`.

* **`to_dataframe()`**: Enhanced the DataFrame output for `Storm` and `Season` objects to make analysis more powerful for users.
    * Added `year` column and a pre-calculated `ace` column to each track entry to facilitate easier seasonal analysis.
    * Implemented strict dtypes (`string`, `float64`) for all DataFrame exports. This silences FutureWarning messages in modern Pandas (2.1+) and ensures consistency across historical records with missing data.

* `plot_storms`: Added the ability to plot a custom list of `Storm` objects.
	* Added a new `plot_storms` function to [`plot.py`](plot.py) featuring a `title` keyword argument for custom map labeling.
	* Updated the `_add_default_titles` helper function to recognize and display the custom title.
	* Exposed `plot_storms` in [`__init__.py`](__init__.py) to allow it to be called directly as `hurdat2py.plot_storms()`. 

* Added Trove Classifiers to [pyproject.toml](pyproject.toml) to improve searchability in the Atmospheric Science and GIS categories.

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