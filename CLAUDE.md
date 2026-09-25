# CLAUDE.md: Bottle Crusher

This repository takes a physical product from idea to a working object:
a countertop crusher for empty 1.5 L PET bottles, built by an owner in
Thailand. Claude is the design partner. The owner makes the final call on every
decision and does all physical work: measuring, printing, ordering, assembling.

## How to work here

- **Start every session by reading `START-HERE.md` and `PROJECT-LOG.md`.**
  End every session by updating both.
- **Follow the phases in `docs/00-process.md`.** Do not jump to CAD before the
  requirements are agreed, and do not order parts before a prototype passed.
- **Ask before assuming.** Anything that depends on the owner's kitchen, bottles,
  budget, or tools is a question for the owner, not a guess.
- **Record every decision** as a short file in `docs/decisions/`, numbered
  `NNN-short-title.md`, with the options considered and why one won.
- **Keep the owner's explanations plain.** The owner is not a mechanical engineer.
  Explain forces, tolerances, and materials in everyday terms.

## Engineering conventions

- Units are millimetres, newtons, and Thai baht unless a file says otherwise.
- All CAD is parametric Python in `cad/` using CadQuery. Every dimension that
  comes from a real measurement lives at the top of the file as a named constant
  with a comment saying where it came from.
- A value that has not been measured is marked `# ASSUMED` until the owner
  measures it.
- Every part file exports what its manufacturing process needs: STEP for CNC,
  STL for 3D printing, DXF for laser cutting.
- Show force and strength calculations in `docs/`, with the numbers and a
  safety factor, not just a conclusion.

## Vendors and prices

Vendor capabilities, prices, and shipping to Thailand change. Never state a
price or lead time as fact without checking the vendor's site that day, and
write the date next to any quote in `bom/bom.csv`.

## Safety

This device concentrates force near fingers. Every mechanism proposal must say
where the pinch points are and how they are guarded. The device must not be
able to crush a hand, and it must handle a bottle that still has its cap on or
liquid inside without spraying or breaking.
