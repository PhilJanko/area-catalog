# Format of the area catalog

`AreasCatalog.sqlite` is a SQLite 3 database (schema version 3, see table `catalog_metadata`). The tables are:

- `areas`: ID, level, parent, codes, land area and a representative point,
- `area_names`: primary, German and English names,
- `area_continent_memberships`,
- `area_bound_parts` with the R*Tree index `area_bounds`,
- `area_geometries`: one polygon geometry per area in column `geometry`.

Each geometry is encoded as TLQG version 1:

- **Header (8 bytes):** ASCII `TLQG`, format version `1`, decimal precision `p` (5, 6 or 7), flags `1` (rings are stored without their closing point), reserved `0`.
- **Counts:** an unsigned LEB128 polygon count. For each polygon, an unsigned LEB128 ring count (exterior ring first, then holes). For each ring, an unsigned LEB128 point count, followed by that many longitude/latitude pairs.
- **Coordinates:** each value is a ZigZag-encoded (`2n` for `n ≥ 0`, `−2n − 1` for `n < 0`), unsigned LEB128 delta from the previous value of the same axis in the same ring. Both axes start at 0 for every ring. Divide the running sums by `10^p` to get longitude and latitude in EPSG:4326.
- **Closing rings:** append the first point to the end of each ring.
