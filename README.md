# OpenStreetMap-derived address index — method (ODbL 4.6(b))

HouseRead locates U.S. home addresses with the National Address Database (U.S. DOT) first and OpenStreetMap when the
NAD has no match. For speed, OpenStreetMap addresses are read from an index built from an OpenStreetMap extract. That
index is a database derived from OpenStreetMap, and this repository offers, free of charge and in machine-readable
form, the method used to make it, as section 4.6(b) of the Open Database License requires.

**File:** [`osm-index-method.json`](osm-index-method.json) — sha256 `905879e8b801d1865fe4841f98f2f6568774ae567150c30800fce86fbea5ef35`

It contains:

- the build script (`osm_index_method_build.py`, Python 3 standard library and osmium);
- the street and house-number normalization rules it uses (`osm_normalization.py`);
- the exact reference of the OpenStreetMap extract (file name, planet date, sha256, size) and of the planet file it
  was taken from (official URL, published md5, sha256).

It does not contain address-matching logic, analyses, non-OpenStreetMap data, or any other HouseRead code. The index
itself contains OpenStreetMap data only.

To rebuild: write the two files from the `files` list of the JSON next to each other, then run the `build.command`
on the extract named in `source_extract`. Equivalent OpenStreetMap data: <https://planet.openstreetmap.org/>.

Data © OpenStreetMap contributors, available under the Open Database License:
<https://www.openstreetmap.org/copyright>.
