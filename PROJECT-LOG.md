# Project log

Newest entry first.

## 2026-09-25, session 2

**Done:** Recorded the owner's round 1 answers: Bangkok household, many Chang
and Singha 1.5 L water bottles a day, a bin that fills too fast. The owner
wants a small, good-looking countertop crusher for 1.5 L and smaller bottles
that crushes them as compact as possible, is finger-safe, is cheap, and can be
assembled at home with household tools like a kit. Selling it online later is
a possibility. Wrote a draft requirements table (R1 to R11) with rough
compaction estimates and an explanation of why a capped bottle is a safety
risk.

**Decided:** The requirements stay a draft until the owner confirms them.

**Decided later in the session:** Decision 001, cap off, crush, cap back on.
The device must still be safe if someone forgets the cap. Decision 002: manual
power, no motor. Decision 003: no special features for a forgotten cap,
because only two adults use it; the enclosed chamber contains any mistake.
The owner then set priorities: the crushed result is the top priority (as
thin and airless as possible, only the neck sticking out), crushing should be
felt by hand, up to 12 bottles a day, and usability matters more than budget.
Started `docs/03-concepts.md` with the owner's lever-juicer idea and four
alternatives, plus the stroke vs force trade-off. Added neck, hand-crush, and
bottle-size steps to the Phase 2 measurements.

Then the owner proposed a hydraulic pump, like a car jack: fast at the start,
strong at the end, with a quick release. Wrote it up as idea F in
`03-concepts.md`, with how a two-speed pump works, rough sizing (about 8
pumps per bottle and 10 kg of hand effort, all ASSUMED), finger-safety guards
(an enclosure, a door interlock on the release valve, a pressure relief
valve), and honest downsides (oil in the kitchen, industrial-looking parts,
harder assembly). Added R16, fast release.

The owner then pointed out that this was too early: this stage is about
principles and brainstorming, not specifications or part models. Restructured
`03-concepts.md` as a brainstorm map with five links (hand, force shaper,
carrier, bottle action, result and show), options for each, and example
combinations, including shaped results such as stars, the spiral origami fold,
and stackable pucks. Parked the hydraulic detail for later.

**Lesson for future sessions:** follow the owner's pace. While brainstorming,
offer options and principles, not sizes, part searches, or decisions.

**Next:** Keep brainstorming. The owner can do the Phase 2 measurements
whenever convenient.

## 2026-09-25, session 1

**Done:** Created the project structure, the 10-phase process, the
requirements questionnaire, the vendor candidate list, and a reference CAD
model of an uncrushed 1.5 L bottle with assumed dimensions.

**Decided:** CAD is written as parametric Python with CadQuery. Project files
live in this repository, and work happens in Claude Code sessions, not Cowork.

**Next:** Owner answers the first requirement questions and measures real
bottles.
