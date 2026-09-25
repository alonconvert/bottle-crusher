# The process

Each phase ends with a clear output and the owner's go-ahead. Skipping a phase
usually means paying for parts twice.

| # | Phase | Output | Done when |
| --- | --- | --- | --- |
| 1 | Requirements | `01-requirements.md` answered | Owner agrees what "working" means |
| 2 | Measure | Real bottle dimensions and crushing force | Numbers in `02-measurements.md` |
| 3 | Concepts | 3 to 5 mechanisms compared | One chosen, recorded in `decisions/` |
| 4 | Engineering | Forces, lever ratios, material choices | Calculations in `docs/` with a safety factor |
| 5 | CAD | Every part as a parametric model | Assembly fits in software |
| 6 | Prototype | Cheap 3D-printed version | It crushes real bottles on the counter |
| 7 | Design for manufacturing | Parts adapted to each process | Vendor rules checked for every part |
| 8 | Quotes | Prices from 2 or more vendors per part | Totals in `bom/bom.csv` |
| 9 | Order and build | Parts arrive, get assembled | Device is assembled |
| 10 | Test and iterate | 50 bottles crushed, issues logged | Owner is happy using it daily |

## Phase 2: how to measure crushing force at home

1. Put a bathroom scale on the floor.
2. Stand an empty, uncapped 1.5 L bottle on it.
3. Press down on the bottle with a flat board until it buckles.
4. Note the peak reading in kilograms. Multiply by 9.81 to get newtons.
5. Repeat for the same bottle crushed fully flat, and for 3 different brands.

Photograph each step into `photos/`.
