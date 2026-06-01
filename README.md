# monscope-data

Public, append-only data archive published by [monscope](https://monscope.xyz).
Daily snapshots of Monad decentralization metrics, MIP adoption, and the
identified Monad Foundation delegation fleet. The application source is private;
this repository is the durable, citable record of the underlying data.

## Layout

- `decentralization/` — daily `YYYY-MM-DD.json` snapshots, `latest.json`,
  and `series.json` (compact headline time-series).
- `mip-adoption/` — daily `YYYY-MM-DD.json` snapshots, `latest.json`, `state.json`,
  and `contracts.ndjson.gz` (compressed contract enumeration).
- `foundation/` — daily `YYYY-MM-DD.json` per-validator MF breakdown, `latest.json`,
  and `graph.json` (delegation-map nodes/links).

Each record carries a `schema` string and (going forward) a `provenance` stamp
(`methodology_version`, `generated_at`, `sources`). See `SCHEMA.md`.

## License & attribution

Data is licensed under [CC BY 4.0](LICENSE) — free to use with attribution to
**monscope** (https://monscope.xyz).

The Foundation attribution is **forensically identified** (EOAs funded by a
common distributor, delegating in VDP tier amounts), **not** an official Monad
Foundation disclosure.
