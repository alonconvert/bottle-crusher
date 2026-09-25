# Requirements

Status: **round 2 mostly answered. Waiting for Q18 (counter space) and Q5 (puck or strip).**

## What we know

- Crushes empty 1.5 L PET drinking bottles.
- Lives on a kitchen counter in Thailand, so it faces heat and humidity.
- Parts come from online fabrication services and 3D printing.

## Owner's answers, round 1 (2026-09-25)

In the owner's own words, summarised:

- **Why:** the household in Bangkok drinks only bottled water, many 1.5 L
  bottles a day, and the garbage bin fills up too fast. Friends in Thailand
  have the same problem.
- **Bottles:** 1.5 L, mostly Chang or Singha brand water. It must also handle
  bottles smaller than 1.5 L.
- **Result:** crush each bottle into the most compact form possible, so the bin
  fills up more slowly.
- **Size and place:** small footprint, on the countertop.
- **Look:** something you would *want* on your counter. It should look
  desirable, like a designed kitchen object, not a workshop tool.
- **Cost:** cheap to manufacture.
- **Safety:** it must never endanger the user's hands.
- **Build:** the owner orders the parts and assembles the prototype with common
  household tools: screwdrivers, glue, and similar. Think of it as a
  do-it-yourself kit.
- **Later:** if it works well, possibly sell it online as a branded product.
  For now it is a hobby project, and the process should be fun.

## Owner's answers, round 2 (2026-09-25)

- **Caps:** cap off, crush, cap back on (decision 001). Only the owner and one
  other adult use it, so no special forgotten-cap features (decision 003).
- **Power:** manual, no motor (decision 002). The owner likes the feel of a
  classic lever juicer, where a handle turns a gear that drives a toothed bar.
  Other mechanisms are welcome, because that shape is not compact. See
  `03-concepts.md`.
- **The result is the top priority.** The crushed bottle should be as thin and
  airless as possible, much flatter than anyone could crush it by hand, and
  satisfying to look at. Only the threaded neck should stick out, just enough
  to screw the cap back on.
- **Feel:** you crush it with your own strength and feel it happen.
- **How many:** up to 12 bottles a day.
- **Budget:** not the constraint. Usability comes first. Cheap manufacturing
  still matters later, if it is ever sold.

## Draft requirements

These come from the answers above. They become "agreed" when the owner confirms
them and the round 2 questions fill in the numbers.

| # | Requirement | Target | Status |
| --- | --- | --- | --- |
| R1 | Crushes Chang and Singha 1.5 L water bottles | Every time, no jams | Draft |
| R2 | Also crushes smaller bottles | Sizes to confirm (Q3) | Draft |
| R3 | **Top priority:** crushed bottle as thin and airless as possible, clearly better than crushing by hand | Target thickness set after Phase 2 | Draft |
| R4 | Fits on the counter | Max footprint to confirm (Q18) | Draft |
| R5 | Looks like a designed kitchen object | Owner approves renders before prototype | Draft |
| R6 | Usability before cost | No fixed prototype budget; cost matters again only for a sellable version | Draft |
| R7 | Cannot hurt a hand | No gap a finger can enter while force is applied | Draft |
| R8 | A capped bottle or leftover water makes no mess outside the device | Enclosed crushing chamber; no special cap features (decision 003) | Draft |
| R9 | Assembled at home with household tools | Screwdriver, hex key, glue; no drilling, cutting, or welding | Draft |
| R10 | Survives Bangkok heat and humidity | No rust, no warping in a hot kitchen | Draft |
| R11 | Could later become a sellable kit | Flat-pack friendly, parts that can be made in batches | Draft, nice to have |
| R12 | Normal use: cap off, crush, cap back on | Only the threaded neck sticks out, reachable while the bottle is held crushed | Accepted (decision 001) |
| R13 | Manually powered, no motor | Comfortable effort for one adult; the exact limit is set in Phase 4 | Accepted (decision 002) |
| R14 | Satisfying to use | You feel the bottle give way under your hand | Draft |
| R15 | Quick enough for daily use | Up to 12 bottles a day; one bottle, including recapping, in about 20 seconds (proposed) | Draft |

### What "most compact" can mean (rough, from ASSUMED dimensions)

An uncrushed 1.5 L bottle takes up about 1.7 L of bin space. The plastic
itself is only about 30 g, which is roughly 22 ml of solid PET, so there is a
lot of air to squeeze out. Rough guesses before any measurement:

| How it is crushed | Result looks like | Bin space | Share of original |
| --- | --- | --- | --- |
| Not crushed | Bottle | ~1.7 L | 100% |
| Flattened sideways | Long flat strip, ~320 x 110 x 20 mm | ~0.7 L | ~40% |
| Crushed lengthwise, like a can | Short puck, ~100 mm wide x 60 mm tall | ~0.5 L | ~28% |
| Lengthwise, then cap screwed back on | Same puck, but it cannot spring back | ~0.4 L | ~25% |
| **Goal: tight puck, pressed hard** | ~100 mm wide x 30 mm, plus the neck | ~0.25 L | ~15% |
| Physical limit: plastic with no air at all | Not reachable | ~0.02 L | ~1% |

At 12 bottles a day, that is the difference between about 20 L of bin space
uncrushed and about 3 L at the goal.

Lengthwise crushing looks more compact but needs more force, because the base
and the shoulder of a bottle are stiff. Phase 2 measurements will confirm these
numbers. Phase 3 will compare the mechanisms properly.

### Why the cap matters for safety

Air cannot escape a capped bottle. Squeezing a sealed bottle to a quarter of
its volume raises the air pressure inside to about 4 times normal. Water
bottles are thin, because unlike soda bottles they are not built to hold
pressure. Squeezing one hard can make the cap shoot off or the bottle split,
and leftover water can spray. The design will have to handle this (R8). Q16
asked how the owner uses caps. The answer is decision 001: cap off, crush, cap back on.

## Open questions, round 2 (for the owner)

16. ~~**Caps:**~~ **Answered 2026-09-25:** cap off, crush, cap back on. See
    `decisions/001-cap-off-crush-cap-on.md`.
17. ~~**Volume:**~~ **Answered 2026-09-25:** up to 12 bottles a day.
18. **Space:** how much counter space can it take: width, depth, and the
    height up to the cupboard above, in centimetres? Height matters, because a
    standing 1.5 L bottle is about 32 cm tall before it is crushed.
19. ~~**Money:**~~ **Answered 2026-09-25:** budget is not the constraint;
    usability is.
20. ~~**Power:**~~ **Answered 2026-09-25:** manual, no motor. See
    `decisions/002-manual-power.md`.

## Still open from round 1

These are for later rounds, or they get answered along the way:

3. Which smaller sizes exactly? For example 600 ml, 500 ml, or 350 ml.
5. Crushed lengthwise into a puck, or sideways into a flat strip? Which result looks more satisfying to the owner? Asked again in round 3.
6. Should crushed bottles drop into a bin, or do you pick them out?
9. Wall-mounted or free-standing? The answer so far is countertop.
12. Colour and material preferences: wood, steel, aluminium, plastic?
14. Do you own or have access to a 3D printer?
15. Tools: is a drill available if ever needed, or strictly no drilling?

## Agreed requirements

To be filled in after the owner confirms the draft table above.
