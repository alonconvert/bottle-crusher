# Requirements

Status: **round 1 answered, round 2 questions waiting for the owner.**

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

## Draft requirements

These come from the answers above. They become "agreed" when the owner confirms
them and the round 2 questions fill in the numbers.

| # | Requirement | Target | Status |
| --- | --- | --- | --- |
| R1 | Crushes Chang and Singha 1.5 L water bottles | Every time, no jams | Draft |
| R2 | Also crushes smaller bottles | Sizes to confirm (Q3) | Draft |
| R3 | Crushed bottle is as small as possible | Target volume set after Phase 2 | Draft |
| R4 | Fits on the counter | Max footprint to confirm (Q18) | Draft |
| R5 | Looks like a designed kitchen object | Owner approves renders before prototype | Draft |
| R6 | Cheap to make | Budget to confirm (Q19) | Draft |
| R7 | Cannot hurt a hand | No gap a finger can enter while force is applied | Draft |
| R8 | Safe with a capped bottle or leftover water | No spraying, no bursting, no broken parts | Draft |
| R9 | Assembled at home with household tools | Screwdriver, hex key, glue; no drilling, cutting, or welding | Draft |
| R10 | Survives Bangkok heat and humidity | No rust, no warping in a hot kitchen | Draft |
| R11 | Could later become a sellable kit | Flat-pack friendly, parts that can be made in batches | Draft, nice to have |

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

Lengthwise crushing looks more compact but needs more force, because the base
and the shoulder of a bottle are stiff. Phase 2 measurements will confirm these
numbers. Phase 3 will compare the mechanisms properly.

### Why the cap matters for safety

Air cannot escape a capped bottle. Squeezing a sealed bottle to a quarter of
its volume raises the air pressure inside to about 4 times normal. Water
bottles are thin, because unlike soda bottles they are not built to hold
pressure. Squeezing one hard can make the cap shoot off or the bottle split,
and leftover water can spray. The design will have to handle this (R8). Q16
asks how the owner uses caps today.

## Open questions, round 2 (for the owner)

16. **Caps:** today, do you throw bottles away with the cap on or off? Would
    you accept "cap off, crush, then screw the cap back on"? That trick keeps
    the bottle from springing back open.
17. **Volume:** roughly how many bottles a day, and how often is the bin
    emptied?
18. **Space:** how much counter space can it take: width, depth, and the
    height up to the cupboard above, in centimetres? Height matters, because a
    standing 1.5 L bottle is about 32 cm tall before it is crushed.
19. **Money:** what is your budget in baht for the first working prototype?
    If you ever sold it, what price do you imagine it would sell for?
20. **Power:** hand lever, or a motor? A hand lever is cheaper, quieter,
    simpler to build, and easier to make finger-safe. A motor feels more like
    an appliance but costs more and adds electrical safety work.

## Still open from round 1

These are for later rounds, or they get answered along the way:

3. Which smaller sizes exactly? For example 600 ml, 500 ml, or 350 ml.
5. Crushed lengthwise or sideways? This will be decided in Phase 3 with numbers.
6. Should crushed bottles drop into a bin, or do you pick them out?
9. Wall-mounted or free-standing? The answer so far is countertop.
12. Colour and material preferences: wood, steel, aluminium, plastic?
14. Do you own or have access to a 3D printer?
15. Tools: is a drill available if ever needed, or strictly no drilling?

## Agreed requirements

To be filled in after the owner confirms the draft table above.
