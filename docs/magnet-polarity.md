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
both joints need. With the magnet pushers (below) this takes care of itself: the **N** pusher
fills the bottom face (six seats), the **S** pusher the top face (four seats). From the stack
instead, fill the top face first. Then turn the ring over to fill the bottom face, and **turn the
stack over with it**: the bottom face's magnets then go in the other way up as you see them,
which is the same way up in the ring. Check each face with a compass (below).

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

## Installing the magnets

There are two ways: the magnet pushers, which pick the pole for you, and the stack method, which
needs nothing printed. The pushers are new and not yet tried on the parts themselves: if one does not reach
a seat, or will not leave a magnet in it, use the stack method for that part.

### With the two magnet pushers

Two printed hand tools, one per pole. Each has one magnet glued into its tip. A loose magnet
jumps onto the tip the right way round, and the tool presses it into its seat. **The letter on a
pusher is the pole that the magnet it seats leaves facing out.**

| Pusher | Letters | Use it for |
| :--- | :--- | :--- |
| **N** | red | The fixed side, which presents North: the base's tool pockets, the interface ring's **bottom** face (six seats), the vertical cage dock |
| **S** | blue | The removable side, which presents South: every tool head, the interface ring's **top** face (four seats) |

**Where to start: make both pushers and check them before any magnet goes into a part.**

1. **Print both.** For each pusher, load its body and its two letters together in your slicer as
   one object with several parts (`MagnetPusherN_Body.stl`, `MagnetPusherN_LetterFront.stl`,
   `MagnetPusherN_LetterBack.stl`; the same three for S, in
   [`hardware/models/stl/`](../hardware/models/stl)), and give the letters red (N) or blue (S).
   Print them lying flat, as the files are oriented. On a single-colour printer, print the body
   alone: the letter is then a recess, still readable. `MagnetPusherSleeve.stl` is optional
   (step 6); print it open end down, with a brim.
2. **Fit the tip magnet.** The pocket in the tip may print a little small. If a magnet does not go
   in, clear the hole with a 4.2 mm drill turned by hand, only down to the bottom of the hole:
   the magnet's face must end up level with the tip's face. Put a drop of glue in the pocket and
   press one magnet in. The two tip magnets come from the spares: the [BOM](../BOM.md) lists 100
   magnets for the 92 seats.
3. **Check its pole with a compass before the glue sets.** First make sure the compass points
   north when nothing magnetic is near. Then bring the tip in slowly from the side of the needle,
   from about 10 cm away, and stop as soon as the needle moves. **The N pusher's tip must pull
   the needle's marked (north-seeking) end towards it; the S pusher's tip must push it away.** If
   a tip does the opposite, take its magnet out and put it back the other way up, then check
   again. Then let the glue set.
4. **Cross-check:** the two tips must snap together. If they push apart, one of the checks in
   step 3 was misread: do it again on both.
5. **Work one pole at a time, N first.** With only the N pusher on the bench, fill every base
   pocket, the bottom face of every interface ring and the vertical cage dock. Put it away, then
   take the S pusher and fill every tool head and the top face of every ring. Before starting on
   a ring, count the seats on the face that is up: six is an N face, four is an S face. For each
   magnet, slide one off the stack onto a non-steel surface, touch the tip to it so it jumps on,
   hold the pusher upright over the seat, press straight down until it stops, and lift straight
   up. A magnet that comes loose goes back on the tip, never in by finger: by hand it can go in
   upside down.
6. **If the pusher lifts a magnet back out of its seat or chips its edge,** glue the sleeve over
   the tip. It holds the magnet more gently, and its narrow nose pushes the magnet flush or just
   below the surface. If magnets still come out, fill that part from the stack instead.

Then check each array, as below.

### Without the pushers: from the stack

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

Check one magnet per array. Both methods put every magnet of an array in the same way round, so
one check settles the array, as long as no magnet was put back by hand.

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
