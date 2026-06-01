# Schemas

Schema strings are stable contracts; additive fields may appear, breaking
changes bump the `vN` suffix.

- `monscope.decentralization.v1` — full daily decentralization snapshot
  (`metrics.stake`, `commission`, `active_set`, `geo`, `foundation`, `top_validators`).
- `monscope.decentralization.history.v1` — compact headline series (`series.json`).
- `monscope.foundation.v1` — per-validator Foundation delegation breakdown.
- `monscope.foundation.graph.v1` — delegation-map nodes/links (`graph.json`).
- `monscope.mip-adoption.v2` — MIP adoption snapshot.

`provenance` = `{ methodology_version, generated_at, sources }`.
`fleet_hash` (foundation) = order-independent hash of the tracked wallet set;
a change signals the fleet itself changed (e.g. a rebalance), not just amounts.
