# 001: Cap off, crush, cap back on

Date: 2026-09-25
Status: accepted

## Question

What happens to the bottle cap when the owner crushes a bottle?

## Options considered

1. **Crush with the cap on.** The least effort for the user. But the air
   trapped inside cannot escape. Squeezing the bottle to a quarter of its size
   raises the pressure inside to about 4 times normal. Thin water bottles can
   split or fire the cap off, and leftover water sprays out.
2. **Cap off, crush, throw the cap away separately.** Safe, because the air
   escapes through the open neck. But a crushed bottle partly springs back
   open once released, so it takes more bin space.
3. **Cap off, crush, cap back on.** Safe for the same reason. Screwing the cap
   back on while the bottle is still squeezed traps it small, because outside
   air cannot get back in to re-inflate it. This is the most compact result.

## Decision

Option 3: the normal way to use the crusher is cap off, crush, cap back on.

## Why

It is the only option that is both safe and gives the smallest crushed bottle,
which is the owner's main goal. The cost is one extra step for the user.

## What this means for the design

- The neck of the bottle must stay reachable while the bottle is still held
  crushed, so the user can screw the cap back on before releasing it. That
  favours crushing the bottle lengthwise, with the neck exposed. Phase 3 will
  confirm this.
- Somewhere to put the cap during crushing, such as a small cap holder, would
  help.
- **People will sometimes forget to take the cap off.** Requirement R8 still
  applies: a capped bottle must not burst, spray, or break the device. Phase 3
  must show how each mechanism handles that, for example by limiting the force,
  venting the bottle, or making it impossible to close the crusher on a capped
  bottle.
