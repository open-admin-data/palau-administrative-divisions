# Palau Administrative Divisions / Palau



## Overview

| Item | Details |
|------|---------|
| State | 16 |
| Hamlet | 77 |
| Coordinates | ✅ Included (all levels) |
| Formats | JSON, NDJSON, CSV |
| License | CC-BY-4.0 |
| Last Updated | 2026-09-02 |
| Website | [openadmindata.org/pw](https://openadmindata.org/pw/) |
| API | [openadmindata.org/api/pw](https://openadmindata.org/api/pw/) |
| Flag | [PNG](https://onlygames.me/flags-png/pw/) · [CDN](https://www.freeflags.org/cdn/) · [CSS](https://www.freeflags.org/css/) · [Collections](https://www.freeflags.org/collections/) |
| National Anthem | [🎵 Listen & Download Palau National Anthem MP3](https://onlygames.me/national-anthems/pw/) |

## Browse by State

| # | State | Hamlets | Link |
|---|----|----|------|
| 1 | Aimeliik | 6 | [Browse](divisions/aimeliik/) |
| 2 | Airai | 6 | [Browse](divisions/airai/) |
| 3 | Angaur | 4 | [Browse](divisions/angaur/) |
| 4 | Hatohobei | 1 | [Browse](divisions/hatohobei/) |
| 5 | Koror | 13 | [Browse](divisions/koror/) |
| 6 | Melekeok | 8 | [Browse](divisions/melekeok/) |
| 7 | Ngaraard | 5 | [Browse](divisions/ngaraard/) |
| 8 | Ngarchelong | 8 | [Browse](divisions/ngarchelong/) |
| 9 | Ngardmau | 3 | [Browse](divisions/ngardmau/) |
| 10 | Ngeremlengui | 8 | [Browse](divisions/ngeremlengui/) |
| 11 | Ngatpang | 0 | [Browse](divisions/ngatpang/) |
| 12 | Ngchesar | 4 | [Browse](divisions/ngchesar/) |
| 13 | Ngiwal | 3 | [Browse](divisions/ngiwal/) |
| 14 | Peleliu | 5 | [Browse](divisions/peleliu/) |
| 15 | Sonsorol | 1 | [Browse](divisions/sonsorol/) |
| 16 | Kayangel | 2 | [Browse](divisions/kayangel/) |

## Data Files

| File | Format | Description |
|------|--------|-------------|
| [all-state.json](data/all-state.json) | JSON | All 16 state records |
| [all-hamlet.json](data/all-hamlet.json) | JSON | All 77 hamlet records |
| [all-flat.json](data/all-flat.json) | JSON | Levels 1-1 flat array |
| [all-flat.ndjson](data/all-flat.ndjson) | NDJSON | Streaming format |
| [all-flat.csv](data/all-flat.csv) | CSV | Spreadsheet format |
| [hierarchy.json](data/hierarchy.json) | JSON | Nested tree |
| [schema.json](data/schema.json) | JSON Schema | Data schema |

## Quick Start

### Python

```python
import json

with open("data/all-state.json", "r", encoding="utf-8") as f:
    data = json.load(f)

for r in data:
    print(f"{r['name']['local']} ({r['name']['en']}) — {r['children_count']['hamlet']} hamlets")
```

### JavaScript

```javascript
import { readFileSync } from "fs";

const data = JSON.parse(readFileSync("data/all-state.json", "utf-8"));
console.log(`Total: ${data.length} states`);
```

## Schema

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique identifier |
| `level` | integer | 1=state, 2=hamlet |
| `level_name` | object | Level label (local + English) |
| `name.local` | string | Name in local script |
| `name.en` | string | English name |
| `name.slug` | string | URL-safe slug |
| `parent` | object/null | Parent division reference |
| `ancestors` | array | Full ancestor chain |
| `children_count` | object | Count of children per level |
| `zip_codes` | array | Postal codes (where available) |
| `geo.lat` | string | Latitude (WGS84) |
| `geo.lon` | string | Longitude (WGS84) |

Full schema: [data/schema.json](data/schema.json)

## Hierarchy Browse

```
divisions/{state-slug}/
```

Hamlets are listed inline in each state's README.

## AI Integration

- [llms.txt](docs/llms.txt) — Quick reference for AI agents
- [llms-full.txt](docs/llms-full.txt) — Summary with per-state links
- [Per-state data](docs/llms-full/) — Full data by state

## Citation

```
Palau Administrative Divisions Dataset (CC-BY-4.0)
URL: https://github.com/open-admin-data/palau-administrative-divisions
```

See [CITATION.cff](CITATION.cff) for machine-readable citation.

## License

- **Data**: [CC-BY-4.0](LICENSE)

## Related

- [Open Admin Data](https://openadmindata.org) — Browse, search and explore administrative divisions for every country
- [open-admin-data](https://github.com/open-admin-data) — GitHub organization with all country repos
- [ListBase](https://www.listbase.org) — Structured reference data for every country
- [FreeFlags.org](https://www.freeflags.org) — Free flag images for every country
- [Flag CDN](https://www.freeflags.org/cdn/) — Hotlink flag images directly
- [Flag CSS](https://www.freeflags.org/css/) — CSS flag sprites for web projects
- [Flag Collections](https://www.freeflags.org/collections/) — Curated flag image packs
