# Steady Hand Tool

**A stabilizing pick-and-place arm for precision SMD assembly.**

[![Project Status](https://img.shields.io/badge/Status-Open%20Source-green.svg)](https://halfmarble.com/blogs/news/steady-hand-tool)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

<p align="center">
  <img src="media/hero-shot.jpg" alt="Steady Hand Tool v1" width="600">
  <br>
  <em>Steady Hand Tool — when you need help holding down really tiny parts.</em>
</p>

---

## 🛒 Bill of Materials (BOM)

The Steady Hand Tool is designed for easy sourcing. You can find the links and visual references for each component below (please notice that these are affiliate links).

### 🏗️ Structural Hardware

| Image | Item | Specification | Purpose |
| :---: | :--- | :--- | :--- |
| <img src="media/rods.jpg" width="100"> | [**Carbon Fiber Rods**](https://amzn.to/4jpyyZC) | 8mm Diameter x 300mm (**4 required**) | 2 horizontal rails, 1 vertical mast, 1 vertical tool rod |
| <img src="media/bearings.jpg" width="100"> | [**MR128ZZ Bearings**](https://amzn.to/42kMWMD) | 8x12x3.5mm (14 required) | Frictionless carriage movement |
| <img src="media/magnets.jpg" width="100"> | [**Magnets**](https://amzn.to/4hq1puZ) | 4mm x 2mm Neodymium (95 required, buy 100) | Magnetic tool coupler interface. **Orientation matters** — see the [Magnet Polarity Standard](docs/magnet-polarity.md) |
| | **Base Ballast** | Round steel shot, **1.5 - 2.0 mm** (nominal 2.0 mm). Approx. **517 g** per base | Fills the printed base to **680 g ± 10 g**. The machined aluminium base needs none. **Size is not a preference** — read the note below before you buy any |

**Magnet count, broken down:** 24 in the base (four tool pockets, six each), 24 in the four
tool adapters (six each), 40 in the four interface rings (six on the bottom face and four on the
top of each), 4 in the vertical cage and 3 in the stopper — 95 in total. Buy 100; they are
small, and one will find the floor.

**On the ballast, before you buy any.** The shot goes into the printed base through a **⌀8 mm
socket**, and that socket — not the chamber — is what governs. Granular flow arches when the
opening falls below roughly four particle diameters, so anything much over 2 mm bridges at the
mouth and leaves the outer chamber empty. At the other end, the chamber vents are ⌀1.5 mm and
finer shot runs straight back out. **So: 1.5 - 2.0 mm, nominal 2.0.** SAE **S-780** blasting shot
and **#9 steel reloading shot** both sit in that window.

**This entry used to link to 6.35 mm slingshot ammo, and it does not work.** A base filled with it
reaches about **619 g against the 680 g spec** — it bridges at the socket and packs to 49% where
a settled fill reaches 60%. The link has been removed rather than swapped, because the search
terms above are what you actually want. Fill by weighing the base, not by measuring the shot, and
tap or vibrate it between pours. Full method: [Step 1 of the assembly
guide](docs/assembly-guide.md#step-1-weight-the-base).

### 🔩 Fasteners

| Image | Item | Specification | Purpose |
| :---: | :--- | :--- | :--- |
| <img src="media/hardwareM3.jpg" width="100"> | [**M3 Hardware**](https://amzn.to/42phRHt) | Stainless steel. **32x M3x16, 3x M3x20, 1x M3x10, 8x M3x8, and 38 nuts** | Structural assembly of the arm |

Buy a few spares of each size. **Neither base takes a fastener of any kind** — every one of these
goes into the arm. The step-by-step breakdown is in the
[assembly guide](docs/assembly-guide.md#-preparation-fasteners-sorting).

### 🧩 Fasteners and magnets per part

Where each fastener and magnet above goes. **Qty** is how many of the part one tool has; the
printed parts are in the [print list](Print.md).

| Part | Qty | M3x8 | M3x10 | M3x16 | M3x20 | M3 nuts | Magnets |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Horizontal cage | 2 | – | – | 12 for the pair | – | 12 for the pair | – |
| Pillar | 3 | – | – | 2 each = 6 | – | 2 each = 6 | – |
| Vertical cage | 1 | – | – | 3 | – | – | 4 |
| Vertical cage, bottom | 1 | – | – | – | 3 | – | – |
| Vertical cage, top | 1 | – | 1 | – | – | 1 | – |
| Aligner (horizontal stop) | 1 | – | – | 2 | – | 2 | – |
| Stopper (vertical stop) | 1 | – | – | 1 | – | 1 | 3 |
| Interface ring | 4 | – | – | 2 each = 8 | – | 2 each = 8 | 10 each = 40 |
| Tool head (tweezers) | 4 | 2 each = 8 | – | – | – | 2 each = 8 | 6 each = 24 |
| Base (printed or machined) | 1 | – | – | – | – | – | 24 |
| **Total** | | **8** | **1** | **32** | **3** | **38** | **95** |

- 14 of the 32 M3x16 go through the bearing sets: 8 in the two horizontal cages and 6 in the
  pillars. Of the cages' other 4, two join the two cages to each other and one in each cage
  clamps the vertical mast.
- The 3 M3x16 of the vertical cage and the 3 M3x20 of its bottom form their own thread in the
  pillars and take no nut.
- The M3x8 and their nuts clamp the tweezers. A vacuum-pen or template head takes none.

### 🔧 Tools

| Image | Item | Specification | Purpose |
| :---: | :--- | :--- | :--- |
| <img src="media/tweezers.jpg" width="100"> | [**Reverse Tweezers**](https://www.amazon.com/dp/B07V8SLF2T?tag=halfmarble0f-20) | Reverse action (self-closing) — squeeze to open | Holding SMD parts during placement |
| <img src="media/tools.jpg" width="100"> | [**Ball-Hex Drivers**](https://amzn.to/4jlawie) | Metric Allen Key Set | Recommended for assembly |
