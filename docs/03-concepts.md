# Concepts

Status: **collecting ideas.** The proper comparison (Phase 3) happens after the
Phase 2 measurements, because the numbers decide which mechanism is strong
enough.

## What the owner wants from the mechanism (2026-09-25)

- **The crushed bottle is the star.** As thin and airless as possible,
  "something you could never do with your hands". The finished puck or strip
  should be satisfying to look at.
- **Only the threaded neck sticks out**, just enough to screw the cap back on.
- **You feel it.** Powered by hand, with real feedback, so you feel strong
  while crushing. The owner likes the classic lever juicer: a long handle
  turning a gear that drives a toothed bar (a rack) down onto the fruit.
- **Compact** is still wanted, and the owner knows the juicer shape is tall.

## Ideas to compare in Phase 3

| # | Idea | How it works, in plain words | First thoughts |
| --- | --- | --- | --- |
| A | Lever juicer (rack and pinion) | A handle turns a small gear, which pushes a toothed bar down onto the bottle | The owner's favourite. Great feel. Problem: see "stroke vs force" below |
| B | Lever juicer with a ratchet | The same, but you pump the handle 3 or 4 times, with a click each time, like a car jack | Solves the stroke problem and adds satisfying clicks. Slower per bottle |
| C | Toggle lever | A lever and a link that straighten out at the bottom, like a wall can crusher. The force gets bigger right at the end, where the bottle is hardest to squash | Strong finish in one pull. Hard to make the end of the stroke very thin |
| D | Screw press | You turn a wheel or crank, a big screw drives a plate down | Enormous force and very thin results. Compact. But slow: many turns per bottle |
| F | **Two-speed hydraulic pump (owner's idea, lead candidate)** | Pump a handle like a car jack. Oil pushes a piston that lifts the crushing plate: fast at first, then slow and very strong. A release knob drops it back in a second | See the full write-up below |
| E | Sideways flattener | Squashes the bottle flat on its side into a strip | Less height needed. The neck is harder to reach for recapping |

## The key trade-off: stroke vs force

To crush a bottle lengthwise, the plate has to travel almost the whole bottle
height, roughly 280 mm (ASSUMED). Near the end it also has to push very hard,
because a folded stack of plastic is stiff.

A single lever swing of about 150 degrees can give you **either** a long
travel **or** a big force multiplication, not both:

- If one swing must travel 280 mm, the gear needs a radius of about 107 mm.
  With a 400 mm handle, your hand force is multiplied only about 3.7 times.
- If the hand force should be multiplied 15 times, one swing travels only
  about 70 mm, so you need about 4 swings, which means a ratchet (idea B) or a
  two-speed design.

This is why the bathroom-scale measurements matter. If the last few
millimetres need 150 kg of force, a single swing cannot deliver it
comfortably. If they need 40 kg, it might.

All numbers here are rough and use ASSUMED dimensions. Phase 4 redoes them with
measured values and a safety factor.

## Idea F in detail: two-speed hydraulic pump (2026-09-25)

The owner's idea: pump a handle with the same comfortable effort every time,
and let hydraulics turn that into speed at the start and huge force at the
end. Then release quickly so the bottle comes out without waiting.

### How hydraulics multiply force

Oil cannot be squeezed. If a small piston pushes oil into a cylinder with a
bigger piston, the pressure is the same everywhere, but the bigger piston has
more area for that pressure to push on. So it pushes harder, and moves less.
A car jack works this way: many small, easy pumps lift a car a little at a
time.

### How "fast then strong" works: a two-speed pump

This is a real, off-the-shelf design, used in workshop hand pumps. The pump
has two pistons side by side, driven by the same handle:

1. **Fast stage.** While the bottle offers little resistance, both pistons
   push oil. Lots of oil per pump means the plate moves a lot per pump.
2. **Automatic switch.** When the pressure rises past a set point, because the
   bottle is starting to fight back, a spring-loaded valve (an "unloading
   valve") sends the big piston's oil back to the tank. It does nothing for
   the rest of the stroke.
3. **Strong stage.** Only the small piston keeps working. Little oil per pump
   means the plate moves only a little per pump, with much more force, and
   your hand still pushes with about the same effort.

You get what you described: the handle always feels about the same, the plate
races up at the start and then grinds slowly and powerfully at the end.

### Fast release

- A **release valve** (a knob or a small lever) opens a path from the cylinder
  back to the tank.
- A **return spring** inside the cylinder pushes the piston back down. Ready-made
  "single-acting, spring-return" cylinders do exactly this.
- The plate drops in about a second, and the puck sits loose on it.

### A bonus that fits "cap back on" (decision 001)

A hydraulic cylinder **holds its position by itself** until you open the
release valve. After the last pump, the bottle stays squeezed with both hands
free. You screw the cap on while it is still crushed, then open the valve.

### Proposed layout (to sketch in Phase 5)

- The cylinder sits in the base and pushes the crushing plate **upward**.
- The bottle stands neck-up. The fixed top plate has a hole just big enough
  for the threaded neck to poke through.
- When the crush finishes, the neck sticks out of the top. Put the cap back
  on from above, open the valve, and take the puck out of the door.

### Rough sizing (every number ASSUMED until Phase 2 and Phase 4)

Assume the final squeeze needs about 3,000 N, about the weight of 300 kg.

| Part | Assumed size | What it gives |
| --- | --- | --- |
| Main cylinder | 20 mm bore, 290 mm stroke | 3,000 N needs about 95 bar of oil pressure, which is low for hydraulics |
| Fast piston | 25 mm bore, 40 mm stroke | About 60 mm of plate travel per pump |
| Strong piston | 10 mm bore, 40 mm stroke | About 10 mm of plate travel per pump |
| Handle | 8 : 1 leverage | About 10 kg of hand effort, in both stages |

A 1.5 L bottle would take roughly 4 fast pumps and 3 or 4 strong pumps, about
8 pumps in total, and then a twist of the release knob. That is roughly 10 to
15 seconds.

### Safety: this is the strongest idea, so it needs the most care

A hydraulic press can easily crush a finger, and the pump makes the force
feel effortless. Proposed guards:

- **Fully enclosed chamber with a door.** No way to reach the plate.
- **Door interlock:** while the door is open, it holds the release valve open,
  so no pressure can build and the plate cannot rise. This is a simple
  mechanical link, with no electronics.
- **Pressure relief valve** set just above what a bottle needs, so the device
  can never push harder than, for example, 4,000 N, even if something jams.
- **Pinch points to check:** the plate against the chamber walls (inside the
  enclosure), the door hinge edge, and the pump handle pivot.

### Honest downsides

- **Oil in a kitchen.** Seals can weep over the years. A drip tray and
  food-safe hydraulic oil would help.
- **Ready-made parts are industrial.** Off-the-shelf pumps and cylinders are
  usually rated at 5 tonnes or more. They are heavy, grey, and far stronger
  than needed. Fine for a prototype, but a nice-looking version would need a
  custom, compact pump and cylinder unit.
- **Assembly is harder than screws and glue.** It needs hose fittings tightened
  with a spanner, filling with oil, and bleeding out the air. It is doable at
  home, but it is the least "kit-like" option. A pre-filled, sealed unit would
  fix that for a sellable version.
- **Weight and cost** are higher than a lever. The owner said budget is not the
  constraint.

### Fallback

The same "fast then strong" feel can also be made mechanically, without oil:
for example, a ratchet with two gear speeds, or a lever whose leverage grows
toward the end of the stroke (idea C). Keep this as plan B if oil in the
kitchen turns out to be a problem.

### Sources checked 2026-09-25

- Two-speed hand pumps and how the switch works:
  https://sarum-hydraulics.co.uk/blog/two-speed-hydraulic-hand-pump/ and
  https://www.sunhydraulics.com/model/YRES/LANAV
- Spring-return cylinders exist with strokes up to about 360 mm, from about
  5 tonnes up: https://www.fpt-worldwide.com/en/product/single-acting-hydraulic-cylinders-with-spring-return/
- No prices checked yet.
