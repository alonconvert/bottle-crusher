# Project: Bottle Crusher

I want to design a physical product with your help and take it all the way
from idea to a working device on my kitchen counter. This is a personal
project. It has nothing to do with Converty OS or my agency work, so never
read, write, or reference any other repository.

## The product

A countertop device that crushes empty 1.5 litre PET drinking bottles.

- I live in Thailand, so it must handle heat and humidity, and parts and
  services must be orderable or deliverable here.
- I want to have the parts made by online fabrication services: laser
  cutting, CNC machining, sheet metal, and 3D printing. Local Thai workshops
  are fine too.
- Standard hardware like bolts, springs, and hinges can come from local
  hardware stores.

## How we work together

- **You are my design partner and project manager.** You research, propose
  options, calculate, write the CAD, prepare vendor files, and keep the project
  organised.
- **I make every decision and do all physical work.** I measure bottles, take
  photos, print or order parts, pay, assemble, and test.
- **Explain everything in plain language.** Assume I have no mechanical
  engineering background. When you mention force, torque, tolerance, or a
  material property, tell me what it means in everyday terms.
- **Ask me few questions at a time.** Three to five per round, never a wall of
  fifteen.
- **Never guess what only I can know.** My bottles, my counter, my budget, and
  my tools are questions for me.

## Where everything lives

All project files live in the GitHub repository alonconvert/bottle-crusher.
Claude Code cloud sessions are temporary, so commit and push to main at the
end of every session, or the work is lost. Use this structure:

    bottle-crusher/
    ├── START-HERE.md          What this project is and how to resume it
    ├── PROJECT-LOG.md         Dated log: what happened, what's next
    ├── docs/
    │   ├── 00-process.md      The 10 phases and where we are
    │   ├── 01-requirements.md Questions for me, then agreed requirements
    │   ├── 02-measurements.md Real bottle dimensions and crushing forces
    │   ├── 03-concepts.md     Mechanism options compared
    │   ├── 04-engineering.md  Force and strength calculations
    │   ├── vendors.md         Fabrication services and what each can do
    │   └── decisions/         One file per decision: 001-title.md, ...
    ├── cad/
    │   ├── requirements.txt   Python packages for the CAD
    │   ├── bottle_reference.py
    │   ├── parts/             One Python file per part
    │   └── out/               Exported STEP, STL, DXF, and preview images
    ├── bom/
    │   └── bom.csv            Bill of materials with prices and quote dates
    ├── photos/                My measurement, prototype, and test photos
    └── orders/                Quotes, order confirmations, shipping notes

### START-HERE.md

A one-page summary: the goal, the current phase, the last decision made, and
the next action. Update it at the end of every session.

### PROJECT-LOG.md

A dated, newest-first log. Each entry says what we did, what we decided, and
what's next. **At the start of every new session, read START-HERE.md and
PROJECT-LOG.md before doing anything else,** because you won't remember
earlier sessions.

### bom/bom.csv

Columns:

    part_id,name,qty,process,material,vendor,unit_price_thb,shipping_thb,quote_date,cad_file,status

### Decision files

Each file in docs/decisions/ records one decision:

    # 001: Title
    Date: YYYY-MM-DD
    Status: proposed | accepted | replaced by NNN
    ## Question
    ## Options considered
    ## Decision
    ## Why

## The 10 phases

Each phase ends with a clear output and my go-ahead. Don't skip ahead. Don't
start CAD before requirements are agreed, and don't let me order real parts
before a cheap prototype has crushed real bottles.

| # | Phase | Output | Done when |
|---|---|---|---|
| 1 | Requirements | 01-requirements.md answered | I agree what "working" means |
| 2 | Measure | Real bottle dimensions and crushing force | Numbers in 02-measurements.md |
| 3 | Concepts | 3 to 5 mechanisms compared | One chosen and recorded as a decision |
| 4 | Engineering | Forces, lever ratios, materials | Calculations shown with a safety factor |
| 5 | CAD | Every part as a parametric model | Assembly fits together in software |
| 6 | Prototype | Cheap 3D-printed or plywood version | It crushes real bottles on my counter |
| 7 | Design for manufacturing | Each part adapted to its process | Vendor rules checked for every part |
| 8 | Quotes | Prices from 2 or more vendors per part | Totals in bom.csv |
| 9 | Order and build | Parts arrive and get assembled | Device is assembled |
| 10 | Test and iterate | 50 bottles crushed, issues logged | I'm happy using it every day |

## Rules

### Measurements and units
- Millimetres, newtons, and Thai baht, unless a file says otherwise.
- Any number that hasn't been measured is marked **ASSUMED** until I measure
  it. Tell me exactly how to measure it with household tools.

### CAD
- Write all CAD as parametric Python using CadQuery, so any dimension can be
  changed in one place. Every measured dimension is a named constant at the
  top of the file with a comment saying where it came from.
- Export what each process needs: STEP for CNC and sheet metal, STL for 3D
  printing, DXF for laser cutting.
- Also export a preview image of every part and of the assembly, so I can see
  the design without CAD software.
- If CadQuery can't be installed in your environment, tell me and propose the
  closest alternative before writing any CAD.

### Engineering
- Show calculations with the actual numbers, not just conclusions.
- Use a safety factor and say what it is and why.

### Vendors and prices
- Prices, capabilities, and shipping to Thailand change. Never state a price
  or lead time as fact without checking the vendor's website that day, and
  write the date next to every quote.
- Compare total landed cost in baht: part price plus shipping plus Thai import
  duty and VAT.
- Candidates to evaluate, none verified yet:
  - International online services: JLCPCB and JLC3DP, PCBWay, Xometry,
    Protolabs.
  - Local Thai shops, found by searching in Thai: "ตัดเลเซอร์" for laser
    cutting, "งาน CNC" for CNC work, "รับปริ้น 3D" for 3D printing services.
  - Hardware: HomePro, Global House, and local hardware stores.

### Safety
This device concentrates force near fingers. Every mechanism proposal must:
- Show where the pinch points are and how they're guarded.
- Make it impossible to crush a hand.
- Handle a bottle that still has its cap on or some liquid inside without
  spraying, bursting, or breaking the device.

## Your first task in this session

1. If the folder already has these files, read them and continue from
   START-HERE.md instead of recreating anything. Otherwise, create the folder
   structure and all the files above. Fill 00-process.md
   with the phases, vendors.md with the candidates, bom.csv with its header
   row, and START-HERE.md and PROJECT-LOG.md with today's entry.
2. Write cad/bottle_reference.py: a simple model of an uncrushed 1.5 L bottle
   to design around. Mark every dimension ASSUMED. Run it if you can and
   export the STEP, STL, and a preview image.
   Exports in cad/out/ are not committed; regenerate them from the scripts.
3. Start Phase 1. Ask me the first 3 to 5 requirement questions. Cover these
   areas over the next few rounds:
   - **Bottles:** which brands I drink, cap on or off, other sizes too.
   - **Result:** how flat is flat enough, crushed lengthwise like a can or
     flattened sideways, where crushed bottles go.
   - **Use:** bottles per day or week, hand lever or foot pedal or motor,
     wall-mounted or free-standing, maximum counter space.
   - **Look:** kitchen-appliance look or workshop look, materials I like.
   - **Budget and tools:** total budget in baht, whether I have a 3D printer,
     which tools I own.
4. Give me the Phase 2 home measurement instructions early, so I can do them
   while we talk. For crushing force: put a bathroom scale on the floor, stand
   an empty uncapped bottle on it, press down with a flat board until it
   buckles, and read the peak in kilograms. Then again until it's fully flat.
   Repeat for 3 brands and photograph each step into photos/.
5. At the end of the session, update START-HERE.md and PROJECT-LOG.md,
   then commit and push to main.
