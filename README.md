# TerraLumen area catalog

This repository provides the area catalog included in the iPhone app TerraLumen, free of charge and without sign-in, as the Open Database License requires.

## License

`AreasCatalog.sqlite` is made available under the Open Database License 1.0 (ODbL): https://opendatacommons.org/licenses/odbl/1-0/

## Sources

- © Overture Maps Foundation and contributors: Overture Maps, theme “divisions”, release 2026-07-22.0, ODbL 1.0. Attribution details: https://docs.overturemaps.org/attribution/
- © OpenStreetMap contributors, ODbL 1.0: https://www.openstreetmap.org/copyright
- geoBoundaries, Esri Community Maps contributors and Land Information New Zealand (LINZ), CC BY 4.0: https://creativecommons.org/licenses/by/4.0/
- Unicode CLDR 48 (assignment of countries to continents), Unicode License v3: see `LICENSE-Unicode-3.0.txt`
- Natural Earth (continent boundaries), public domain: https://www.naturalearthdata.com/about/terms-of-use/

## Changes from the sources

The catalog keeps only land areas of continents, countries and regions, plus local areas for Germany and the United States. Geometries are simplified and quantized, continents are built from country land, and names are limited to the primary, German and English names.

## File

| File | Size | SHA-256 |
| --- | --- | --- |
| `AreasCatalog.sqlite` | 101,724,160 bytes | `ac40421577722a4142c03c59c30dec4d480066876d79c47122ce412e58e5feea` |

Included in TerraLumen 1.0 and later until a new catalog is released here.

## Format

`AreasCatalog.sqlite` is a SQLite 3 database. Its tables and the encoding of its geometries are described in [FORMAT.md](FORMAT.md).
