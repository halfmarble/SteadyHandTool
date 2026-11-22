# Printable parts

Every file in this folder is ready to slice. Quantities and build order are in the
[assembly guide](../../../docs/assembly-guide.md); the [BOM](../../../docs/BOM.md) is the shopping
list for everything you cannot print.

| File | What it is |
| :--- | :--- |
| `Pillar.stl` | Upright strut — carries the pivot pins the arm swings on |
| `Spacer.stl` | The "fat" spacer, ⌀10.8 body on a ⌀8 spigot. One per bearing set |
| `SpacerSmall.stl` | The "thin" spacer, same three diameters. One per bearing set |
| `Stopper.stl` | Split clamp collar for an 8 mm rod, M3 cross screw |
| `Aligner.stl` | Horizontal stop |
| `InterfaceRing.stl` | The ring the tool head couples to, with a knurled band round its neck, a knurled rim and a plain curved flare under the rim (Step 11) |
| `PlateSteadyHandTool.stl` | Name plate (Optional Step 13) |
| `PlateHalfLogoMarble.stl` | Logo plate (Optional Step 13) |
| `InterfaceTweezers.stl` | Tweezer head |
| `InterfaceManualVacuumPen.stl` | Manual vacuum pen head |
| `InterfaceTemplate.stl` | The blank — start your own tool head from this one |
| `MagnetPusherNBody.stl`, `MagnetPusherNLetterFront.stl`, `MagnetPusherNLetterBack.stl` | The **N** magnet pusher: body and its two inlay letters (red). Seats magnets north face out — base pockets, ring bottom faces, the cage dock |
| `MagnetPusherSBody.stl`, `MagnetPusherSLetterFront.stl`, `MagnetPusherSLetterBack.stl` | The **S** magnet pusher: body and its two inlay letters (blue). Seats magnets south face out — tool heads, ring top faces |
| `MagnetPusherSleeve.stl` | Sleeve for a pusher's tip: print two, one for each pusher. How to use them: the [magnets guide](../../../docs/magnets.md) |
| `MagnetCouponMouthUp.stl`, `MagnetCouponMouthDown.stl` | The two magnet coupons: 25 magnet seats each, ⌀3.70 to ⌀4.18 mm, to check how your printer prints the ⌀4 seats before you print the parts. How to read them: the [magnets guide](../../../docs/magnets.md#1-dial-in-your-printer-first-the-two-magnet-coupons) |
| `MagnetRigPuck.stl`, `MagnetRigPusher.stl`, `MagnetRigCap.stl` | The magnet rig: a puck that sits in a base tool pocket, a pusher and its flat cap. An optional guide for seating the base's magnets, not yet used on a printed base. How to use it: the [magnet rig](../../../docs/magnets.md#9-the-magnet-rig-the-bases-tool-pockets-guided) |

Adapters for third-party tools are one level up, in [`3rdParty/`](../3rdParty). Print plates, which
carry orientation and slicer settings rather than geometry, are in [`3mf/`](../3mf).

## Not in this folder yet: the carriage and the base

Six printable parts are still to come, so you will not find them here:

| Part | Where it is used |
| :--- | :--- |
| Horizontal cage | Assembly guide, Steps 5–6 |
| Vertical cage — three parts | Steps 7–8 |
| Base — the printed cup and screw-in top, filled with steel shot to 785 g | Step 1 |

**Every 3D model will be published when the campaign funds** — that is the commitment, and it is
part of what backing it pays for.

They are documented in the meantime, so the design is not a black box while you wait:

- the [assembly guide](../../../docs/assembly-guide.md) shows how the carriage and the base go
  together, in the order you would build them;
- the [BOM](../../../docs/BOM.md) lists what goes inside them — including the ballast, 1/4 in steel
  balls filled by weight;
- the [magnets guide](../../../docs/magnets.md) is the whole specification a
  tool head has to match. Nothing about it waits on the campaign, so a tool head of your own
  design is something you can build today, with `InterfaceTemplate.stl` as the starting blank.

[The campaign is on Crowd Supply.](https://www.crowdsupply.com/halfmarble/steady-hand-tool)
