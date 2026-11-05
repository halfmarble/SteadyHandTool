# Print list

Every 3D-printed part of one Steady Hand Tool, and how many copies to print. Fasteners, bearings,
rods, magnets and the base ballast are not printed: they are in the [BOM](BOM.md), and the
fastener counts are in the [assembly guide](docs/assembly-guide.md#-preparation-fasteners-sorting).

```
+----+------------------------+-------------------------------------------+-----+------------+
| #  | Part                   | File                                      | Qty | Published  |
+----+------------------------+-------------------------------------------+-----+------------+
|  1 | Base, printed cup      | base_PRINTED_v23_topplug_cup.stl          |   1 | On funding |
|  2 | Base, printed top      | base_PRINTED_v23_topplug_top.stl          |   1 | On funding |
|  3 | Horizontal cage        | SteadyHandTool-CageH_2.stl                |   2 | On funding |
|  4 | Vertical cage          | SteadyHandTool-CageV.stl                  |   1 | On funding |
|  5 | Vertical cage, top     | SteadyHandTool-CageVTop.stl               |   1 | On funding |
|  6 | Vertical cage, bottom  | SteadyHandTool-CageVBottom.stl            |   1 | On funding |
|  7 | Spacer, fat            | SteadyHandTool-Spacer.stl                 |  14 | Yes        |
|  8 | Spacer, thin           | SteadyHandTool-SpacerSmall.stl            |  14 | Yes        |
|  9 | Pillar                 | SteadyHandTool-Pillar.stl                 |   3 | Yes        |
| 10 | Aligner                | SteadyHandTool-Aligner.stl                |   1 | Yes        |
| 11 | Stopper                | SteadyHandTool-Stopper.stl                |   1 | Yes        |
| 12 | Interface ring         | SteadyHandTool-InterfaceRing.stl          |   4 | Yes        |
| 13 | Tool head              | InterfaceTweezers.stl                     |   4 | Yes        |
| 14 | Name plate             | SteadyHandTool-Plate_STEADY_HAND_TOOL.stl |   1 | Yes        |
| 15 | Logo plate             | SteadyHandTool-Plate_half_LOGO_marble.stl |   1 | Yes        |
+----+------------------------+-------------------------------------------+-----+------------+
|    | Total, printed base    |                                           |  50 |            |
|    | Total, machined base   |                                           |  48 |            |
+----+------------------------+-------------------------------------------+-----+------------+
```

- **Base.** Print the cup and the top only for the printed version. The machined aluminium base
  is not a printed part, so a tool built on it needs 48 printed parts. The assembly guide, the
  BOM and the READMEs still describe the earlier one-piece printed base, with no cover and a fill
  socket; they will be updated for the screw-in top.
- **Spacers.** One fat and one thin spacer per bearing set, 14 sets.
- **Tool heads.** Four, one for each pocket in the base. Any of them can be
  `InterfaceManualVacuumPen.stl` instead, or a head of your own made from `InterfaceTemplate.stl`.
  Every head has to follow the [Magnet Polarity Standard](docs/magnet-polarity.md).
- **Optional.** The adapter for the third-party PixelPump pen in `hardware/models/3rdParty/` is
  not counted above.
- **On funding** parts are not in this repository yet. Every 3D model is published when the
  campaign funds.

The published parts in the table are in [`hardware/models/stl/`](hardware/models/stl/).

## Slicing in PETG-GF

The parts are tuned for PETG-CF. To print them in PETG-GF, start from your slicer's PETG-CF
profile, change the values below, then calibrate on your own spool. The values are for a
direct-drive printer, with option names as in Bambu Studio and OrcaSlicer; where your slicer
has no such option, skip only that option.

```
+----------------------+------------------------------------------------------------+
| Setting              | Value                                                      |
+----------------------+------------------------------------------------------------+
| Nozzle               | 0.4 mm, hardened steel. Glass fibre is abrasive            |
| Layer height         | 0.20 mm                                                    |
| Nozzle temperature   | 250 - 260 °C; start at 255. The spool's label wins         |
| Bed                  | Textured PEI, 70 °C (65 °C first layer)                    |
| Max volumetric speed | 9 mm³/s to start, then run a max-flow test                 |
| Flow ratio           | Calibrate on the GF spool. Do not reuse a PETG-CF value    |
| Pressure advance     | Calibrate on the GF spool                                  |
| Part cooling fan     | 0 - 30 %, overhangs 90 %, off for the first 3 layers       |
| Retraction           | 0.4 - 0.8 mm on direct drive; on Bowden keep your own      |
| Walls                | 3 - 4 on the cages, spacers, pillars, rings and tool heads |
| Outer wall           | Precise outer wall on; about 100 mm/s on the parts above   |
| Infill               | 35 %, 3D honeycomb, on the arm parts                       |
| Supports             | Tree, automatic                                            |
+----------------------+------------------------------------------------------------+
```

- **Keep the 0.4 mm nozzle.** The small features are sized for it, so do not switch to the
  0.6 mm nozzle often suggested for fibre-filled filament.
- **Dry the spool first**, about 65 °C for 6 - 8 h. Wet PETG-GF strings and prints weak.
- **Avoid a smooth PEI plate.** PETG can bond to it hard enough to pull the coating off.
- **Test the fits before printing the set.** PETG-GF shrinks differently from PETG-CF, so holes
  come out a little different in size. Print one horizontal cage and check that its bearings
  seat, and print one tool head and check that it homes in its pocket. If you print the base,
  check that the top threads into the cup before you fill it.
- **The printed cup and top get heavier.** PETG-GF is usually denser than PETG-CF, so they
  weigh more and the base needs less shot. Weigh the base, as
  [Step 1 of the assembly guide](docs/assembly-guide.md#step-1-weight-the-base) says.
