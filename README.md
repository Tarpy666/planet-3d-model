# Planet 3DModel

Sculpt brush model, retopology decimation plan, texture paint channels.

Part of the Counted fleet (planet-3d-model), generated from `seeds/seeds.yaml`.

## Architecture

- `src/modules.ts` — SculptBrush, DecimationPlanner, PaintChannels
- `src/index.ts` — public API (`SPEC`, `MODULES`, Registry)
- `src/rng.ts` — deterministic seeded PRNG (mulberry32)
- `tests/index.test.ts` — deterministic behavior suite

## Usage

```bash
npm install
npm run typecheck   # strict TS, zero errors
npm test            # deterministic, seeded
npm run build
```

## Determinism

All outputs are seeded; identical inputs produce identical results on any runtime.
