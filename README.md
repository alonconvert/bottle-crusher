# Bottle Crusher

A countertop device that crushes empty 1.5 L PET drinking bottles, designed and
manufactured in Thailand with Claude as the design partner.

The goal is the whole journey, from idea to a working product on the kitchen
counter:

1. Decide what the crusher must do.
2. Explore mechanisms and pick one.
3. Model every part as parametric CAD code.
4. Print a cheap prototype and test it with real bottles.
5. Get quotes from online fabrication services: laser cutting, CNC, 3D printing.
6. Order the parts, assemble them, and use the result.

## Where things live

| Path | What is in it |
| --- | --- |
| `START-HERE.md` | Current phase, last decision, and next action |
| `PROJECT-LOG.md` | Dated log of what happened in each session |
| `docs/` | The process, requirements, research, and vendor notes |
| `docs/decisions/` | One short file per design decision and why it was made |
| `cad/` | Parametric CAD models written in Python with CadQuery |
| `bom/` | The bill of materials: every part, its source, and its cost |
| `photos/` | Measurements, prototypes, and test results |
| `orders/` | Quotes, order confirmations, and shipping notes |

## Working with Claude

Open a Claude Code session on this repository. For a fresh start, paste
`docs/kickoff-prompt.md` as the first message. Claude reads `START-HERE.md`
and `PROJECT-LOG.md` to pick up where the last session stopped.

## Current phase

**Phase 1: Requirements.** See `docs/00-process.md` for all phases and
`docs/01-requirements.md` for the open questions.

## Working on the CAD

```bash
cd cad
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python bottle_reference.py   # writes out/bottle_reference.step and .stl
```

STEP files go to CNC and sheet-metal vendors. STL files go to 3D printing.
DXF files go to laser cutting.

## License

MIT. Build one yourself.
