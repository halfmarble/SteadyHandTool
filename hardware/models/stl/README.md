# Printable parts

Every file in this folder is ready to slice. Quantities and build order are in the
[assembly guide](../../../docs/assembly-guide.md); the [BOM](../../../BOM.md) is the shopping
list for everything you cannot print.

| File | What it is |
| :--- | :--- |
| `SteadyHandTool-Pillar.stl` | Upright strut — carries the pivot pins the arm swings on |
| `SteadyHandTool-Spacer.stl` | The "fat" spacer, ⌀10.8 body on a ⌀8 spigot. One per bearing set |
| `SteadyHandTool-SpacerSmall.stl` | The "thin" spacer, same three diameters. One per bearing set |
| `SteadyHandTool-Stopper.stl` | Split clamp collar for an 8 mm rod, M3 cross screw |
| `SteadyHandTool-Aligner.stl` | Alignment jig used during assembly |
| `SteadyHandTool-InterfaceRing.stl` | The ring the tool head couples to (Step 11) |
| `SteadyHandTool-Plate_STEADY_HAND_TOOL.stl` | Name plate (Step 12) |
| `SteadyHandTool-Plate_half_LOGO_marble.stl` | Logo plate (Step 12) |
| `InterfaceTweezers.stl` | Tweezer head |
| `InterfaceManualVacuumPen.stl` | Manual vacuum pen head |
| `InterfaceTemplate.stl` | The blank — start your own tool head from this one |

Adapters for third-party tools are one level up, in [`3rdParty/`](../3rdParty). Print plates, which
carry orientation and slicer settings rather than geometry, are in [`3mf/`](../3mf).

## Not in this folder yet: the carriage and the base

Five printable parts are still to come, so you will not find them here:

| Part | Where it is used |
| :--- | :--- |
| Horizontal cage | Assembly guide, Steps 5–6 |
| Vertical cage — three parts | Steps 7–8 |
| Base — the printed shell, filled with steel shot to 680 g | Step 1 |

**Every 3D model will be published when the campaign funds** — that is the commitment, and it is
part of what backing it pays for.

They are documented in the meantime, so the design is not a black box while you wait:

- the [assembly guide](../../../docs/assembly-guide.md) shows how the carriage and the base go
  together, in the order you would build them;
- the [BOM](../../../BOM.md) lists what goes inside them — including the ballast, where the shot
  size is fussier than it looks and is worth reading before you buy any;
- the [magnet polarity standard](../../../docs/magnet-polarity.md) is the whole specification a
  tool head has to match. Nothing about it waits on the campaign, so a tool head of your own
  design is something you can build today, with `InterfaceTemplate.stl` as the starting blank.

[The campaign is on Crowd Supply.](https://www.crowdsupply.com/halfmarble/steady-hand-tool)
