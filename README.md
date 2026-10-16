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

The catalog keeps only land areas of continents, countries and regions, plus local areas for Germany and the United States. Geometries are simplified and quantized, continents are built from country land, and names are limited to the primary name and the German, English, French, Spanish, Italian and Japanese names; the continents' French, Spanish, Italian and Japanese names were added by the developer.

## File

| File | Size | SHA-256 |
| --- | --- | --- |
| `AreasCatalog.sqlite` | 102,412,288 bytes | `bd70d6ed2ac3ca4e5a9c6f19a173eca5ba4c5cc256733c1df6db325ce2b39734` |

Included in TerraLumen 1.0 and later until a new catalog is released here.

## Format

`AreasCatalog.sqlite` is a SQLite 3 database. Its tables and the encoding of its geometries are described in [FORMAT.md](FORMAT.md).
