# Magnet Polarity Standard

Magnet orientation is the one part of this design that **cannot be recovered from a model
file**. An STL describes a magnet seat; it says nothing about which way the magnet in that seat
faces. Two people can print the same adapter from the same file, populate it correctly by every
visible measure, and end up with parts that push each other away.

This document fixes that, so a tool head designed by one person clicks into a tool built by
another.

## The rule

> **Fixed parts present NORTH. Removable parts present SOUTH.**

Every magnetic joint in the tool has a fixed side and a removable side:

| Joint | Fixed side, presents **North** | Removable side, presents **South** |
| :--- | :--- | :--- |
| Tool head in the base | Base tool pocket, facing up | Tool head |
| Tool head on the carriage | Interface ring, bottom face, facing down | Tool head |
| Interface ring at the vertical cage | Vertical cage dock, facing down | Interface ring, top face, facing up |

**Every magnet in a single array shares the same pole.** There is no alternating pattern and no
keyed position. Any rotation seats correctly.

**The interface ring is on both sides of a joint**, the fixed side to the tool head below it and
the removable side to the vertical cage above it. All ten of its magnets go in the same way up,
**north face down**: the bottom face then presents North and the top face South, which is what
both joints need. Fill the top face first, from the stack as below. Then turn the ring over to
fill the bottom face, and **turn the stack over with it**: the bottom face's magnets then go in
the other way up as you see them, which is the same way up in the ring. Check each face with a
compass (below).

## Where the magnets are

| Part | Magnets | Pattern |
| :--- | :---: | :--- |
| Base, each of the four tool pockets | 6 | ⌀18 mm bolt circle, 60° apart |
| Tool head (tweezers, vacuum pen, or one of your own) | 6 | ⌀18 mm bolt circle, 60° apart |
| Interface ring, bottom face | 6 | ⌀18 mm bolt circle, 60° apart |
| Interface ring, top face | 4 | on the ⌀18 mm circle |
| Vertical cage dock | 4 | ⌀18 mm bolt circle, 90° apart |

The magnets are ⌀4 × 2 mm neodymium throughout. One tool takes 92: 24 in the base, 24 in four
tool heads, 40 in four interface rings and 4 in the vertical cage (the [BOM](../BOM.md)).

The seats are not all the same size. The base's are ⌀4 mm and 2 mm deep, so a magnet sits flush
with the pocket floor. On the other parts they are ⌀4.2 mm and about 2.1 to 2.5 mm deep — about
2.1 mm in the tool heads — so a magnet sits flush or just below the face.

```
        pocket, viewed from above          side view, one seat

              N     N                      ___________________
           N           N                   |    magnet   |     <- N face up, flush
              N     N                      |_____________|
                                           |   air relief
        all six the same pole              |
        ⌀18 bolt circle, 60 deg apart      v  ballast chamber
```

The small hole under each seat is air relief — it lets a magnet press home instead of riding on
trapped air. Its size differs from part to part. In the base it is not a through-hole to the
outside.

## Installing without a compass

Neodymium magnets ship as a stack, uniformly polarised. **Do not separate the stack and sort the
magnets.** Slide one magnet off the end of the stack at a time and drop it straight into its
seat without turning it over. Every magnet then lands the same way round, and you only have to
verify the array once rather than six times.

If a magnet flips itself as it approaches the seat, it was already attracted to a neighbour in
the wrong orientation — take it out and start that seat again.

## Verifying the array

**Against known-good hardware, which is the easy case.** Offer a factory-built tweezers head to
a base pocket or to the bottom of an interface ring. If it snaps flat and stays put at every
rotation, the array is correct. If it pushes away or sits proud on one side, the array is
inverted.

**With a compass, for a first build.** A compass needle's marked, north-seeking end is a magnetic
*north* pole, so it is attracted to a magnet's *south* pole. Hold the compass over one seated
magnet of the array:

- On a part that presents **North** (a base pocket, the ring's bottom face, the cage dock), the
  marked end should be **pushed away**. If it is pulled in, the array is inverted.
- On a part that presents **South** (a tool head, the ring's top face), the marked end should be
  **pulled in**. If it is pushed away, the array is inverted.

Check one magnet per array. Because the stack method makes them all identical, one check settles
the array.

## If you get it wrong

A fully inverted array is harmless and reversible — the part simply will not stick, and the
magnets press out from the relief hole with a pin. A *single* reversed magnet among five correct
ones is the case worth avoiding: the part still holds, but it rocks on the odd magnet and the
holding force drops noticeably. That is why the whole array shares one pole. There is no phase to
get right, and a mistake is obvious rather than subtle.

## Hardware built before this standard

This document fixes the convention going forward. Prototypes assembled before it exists may be
polarised either way, because nothing recorded which way they went — that is the whole reason for
writing it down.

**Build production hardware to the standard above, not to a prototype.** If an old base and a new
tool head push apart, the old base predates the convention; it is not evidence that the
convention is wrong.

Re-polarising an existing part is straightforward and reversible. Push each magnet out through
its air-relief hole with a pin, turn it over, and press it back in. There is no adhesive and
nothing to damage.

## For tool head designers

Build to **south exposed** and your head will seat in any base pocket and on any interface ring
built to this standard, at any rotation. Copy the seat pattern from `InterfaceTemplate.stl` rather than re-deriving it —
the ⌀18 bolt circle with six seats 60° apart is what makes the parts interchangeable, and the
polarity rule above is what makes them interchangeable *between owners*.

## Why not alternating poles

Alternating north and south around the ring would hold harder, because flux closes between
neighbours, and it would key the head to three rotational positions. It was rejected: a
mis-phased head would actively *repel* its base, which is a poor failure mode for someone seating
a tool one-handed with a tremor. Uniform polarity trades some holding force for an interface that
cannot be assembled out of phase.
