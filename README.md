English | [简体中文](README.zh-CN.md)

# AKG K712 PRO Headband Repair (3D-Printed Parts + Hair Ties as Elastic Loops)

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

![Repair finished](images/16_final_front.jpg)

This repository documents a DIY repair of the headband of an **AKG K712 PRO** open-back studio headphone: the aged factory rubber loops (official name *Rubber loop*, part 6) were replaced with two braided hair ties (elastic cord), and 3D-printed parts replace the **Cover (part 3)** and **Locking knob (part 7)**, which have to be broken or pried out during disassembly. The repo contains process photos, ready-to-slice 3MF files, and the official service manual as a structural reference.

> Note: part numbers and names in this document come from the official AKG K612/K712 service manual (see [`ref/`](ref/)). What the photos directly show is described as such; anything not visible in the photos and inferred from model dimensions or the manual is marked **(inferred)**.

---

## Contents

- [Background: the K712 headband structure](#background-the-k712-headband-structure)
- [Repair process](#repair-process)
- [Cautions](#cautions)
- [3D printing notes](#3d-printing-notes)
- [Folder structure](#folder-structure)
- [Index](#index)
- [References](#references)
- [License](#license)

---

## Background: the K712 headband structure

According to the exploded view and parts list in the official service manual (Service Manual #2458Z00XXX, 10/2015), the parts relevant to this repair are:

| No. | English name | German name | Description |
|---|---|---|---|
| 1 | Outer headband compl. | Bügel kpl. | Outer headband (two insulated steel wires, ends attached to the ear cups) |
| 2 | Headband compl. | Bügelband kpl. | Leather headband (the strap that rests on your head) |
| 3 | Cover | Abdeckung | Round decorative cover on the outside of the slider |
| 4 | Inner slider | Gleitstück innen | Inner slider |
| 5 | Outer slider | Gleitstück außen | Outer slider (slides along the two steel wires) |
| 6 | Rubber loop | Gummischlaufe | Rubber loop: pulls the headband up and provides the self-adjusting tension |
| 7 | Locking knob | Schnappniet | Snap rivet that locks the inner/outer sliders and the headband together |
| 9 / 20 | Cover left (+MiniXLR) / Cover right | Deckel | Ear-cup lid (the steel wires snap into it) |
| 8 / 22 | Grid cover | Gitterdeckel | Outer grille of the ear cup |
| 10 | Screw Ejot 22x5 | Schraube | Two screws under the grille that hold the lid |

The K712's self-adjusting headband relies on the rubber loops (6) on each side to pull the leather strap upward. Over time the rubber ages, loses its elasticity or snaps — a common failure on this family of AKG headbands.

The manual's official procedure for replacing the rubber loops is: **break out the cover (3) by inserting a screwdriver into the notch below the CE sign, then push out the locking knob (7) while depressing its latches.** In other words, the cover is basically destroyed after one removal, and the locking knob breaks easily — which is why this project 3D-prints replacements.

---

## Repair process

### 1. Preparation: ask your wife for two new hair ties

![Hair ties](images/01_hair_ties_preparation.jpg)

The elastic that replaces the rubber loops (6) is simply an ordinary **braided hair tie** — thickness, stretch and length are just right, and you can even pick an orange one to match the K712. So step one: **ask your wife for two new hair ties** (make sure they're *new* ones, and ask permission first 😉). The jar in the photo is the "parts bin".

### 2. Print the replacement "knob + cover"

![Printed caps](images/02_printed_pin_caps.jpg)

Three two-color logo caps were printed (black body + orange logo inlay, matching the K712's black-and-orange color scheme); these are the `k712pro_top` parts in `3d/k712pro_pin_v2.3mf`. The caps are about 15 mm in diameter.

![Brass inserts on the back of the caps](images/03_pin_caps_heat_set_inserts.jpg)

There is a boss in the middle of the back of each cap with a **brass heat-set insert** melted in (two are already installed in the photo, one is not yet), and the boss has a notch on its side. **(Inferred)** The boss takes the role of the original locking knob's (7) shaft, passing through the holes in the headband and sliders; the notch provides clearance for internal features or acts as a locator.

### 3. Check the screw size

![Screw gauge](images/04_screw_size_check.jpg)

A printed screw gauge was used to check the diameter and length of the fixing screw. The screw is **M2 × 6 mm** (the center hole of the inner disc is about Ø2.4 mm, a clearance fit for M2). Mind the torque when tightening — see [Cautions](#cautions).

### 4. Assemble the slider: disc + screw + cap

![Inner side of slider](images/05_slider_inner_side_screw.jpg)

Inner side of the slider: the printed round disc (`Body1` in `3d/k712pro_pin_v2.3mf`, about 13 mm in diameter and 4.5 mm thick, with a textured surface) presses from the inside, and a screw in the middle threads into the brass insert of the outer cap, clamping the headband, inner slider (4) and outer slider (5) together — replacing the original locking knob (7).

![Outer side of slider](images/06_slider_outer_side_logo_cap.jpg)

Outer side of the slider: the cap with the orange logo replaces the original cover (3). The original rubber loop (6) has been replaced by an **orange braided hair tie**, which exits through the slots on both sides of the slider and forms a loop below.

![Both sliders](images/07_sliders_with_elastic_cord.jpg)

The left and right slider assemblies (removed). The left one already has the hair tie routed through the slider's grooves; the right one doesn't yet.

### 5. Open the ear cup and anchor the end of the hair tie

![Removing the grille](images/08_grille_removal_tweezers.jpg)

Remove the outer grille (8/22) as described in the manual: insert pointed tweezers into two grille holes as far apart as possible and turn the whole grille **counter-clockwise** until the latches release. Under the grille are the two screws (10) that hold the lid.

![Hair tie at the ear cup](images/09_cord_routing_at_earcup.jpg)

With the ear-cup lid (9/20) removed you can see the end block of the outer headband's (1) two steel wires. The hair tie runs down from the slider along the wires and is anchored around two corners of the end block, taking the place where the original rubber loop attached. The driver leads (red, white, etc.) soldered to the terminals are visible nearby — don't pull on them.

![Lid opened](images/10_earcup_lid_opened.jpg)

The lid flipped open: the hair tie is held down inside the end block, and the inner structure of the lid and the driver leads (yellow, purple/red, white) are clearly visible.

### 6. Measure and balance both sides

![Measurement A](images/11_cord_routing_measure_a.jpg)
![Measurement B](images/12_cord_routing_measure_b.jpg)

Use a steel ruler to compare the distance from the slider to the ear-cup end block on the left and right sides.

The **C-shaped spacers** printed from `3d/k712_inserts.3mf` are used in this step: they are **adjustment shims** that clip onto the end of the steel wire near the ear-cup end block, compensating for differences between the two sides. The procedure is: **measure both sides by hand first, then insert spacers on the shorter side as needed until both sides match.** In this repair, all the spacers ended up on **one side**.

> ⚠️ Warning: in these two measurement photos, spacers are fitted on both sides — that was only an intermediate state during measurement. **If you copy the photos and fit spacers on both sides, the headband will end up asymmetric.** Don't follow the photos literally — measure first, then add spacers as needed until both sides are symmetric.

### 7. Reassemble and try on

![Reassembled, side](images/13_reassembled_side.jpg)
![Reassembled, front](images/14_reassembled_front.jpg)
![In hand](images/15_reassembled_in_hand.jpg)

After refitting the lid, the screws (10) and the grille. The caps, sliders and orange hair ties blend in with the headphone's original black-and-orange look. The manual recommends a listening test after reassembly: use a **mono** signal (not a sine wave) to check that the sound image is centered — especially if you desoldered any driver leads.

### 8. Done

![Finished, front](images/16_final_front.jpg)
![Finished, side](images/17_final_side.jpg)

---

## Cautions

1. **Use new, braided hair ties with good elasticity**, ideally two of the same kind so both sides pull equally.
2. **The cover (3) is basically destroyed on removal**: the official method is to pry it out from the notch below the CE sign — a destructive step. Have the replacement parts (the caps in this repo) ready before you start.
3. **Locking knob (7)**: you have to press the latches inward while pushing the knob outward; too much force will break it.
4. **The grille (8/22) is latched and turns counter-clockwise** — don't pry it off. Insert pointed tweezers into two holes as far apart as possible and turn evenly, without scratching the mesh.
5. **The ear-cup lid (9/20) is also snapped onto the two steel wires**: first undo the two screws (10) under the grille, then squeeze the sides of the lid until the latches show, press the latches in with a small flat screwdriver, and pull the lid off.
6. **The driver leads are thin**: there are red/yellow/white leads (and the Mini XLR on the left side) under the lid — don't pull on them when opening it. If you replace a driver, the manual says to tighten screws 15 with moderate force only and to make sure the phasing (polarity) is correct.
7. **Heat-set inserts**: don't run the soldering iron too hot, and press the insert in straight, so the boss doesn't deform.
8. **Mind the torque on the M2 × 6 mm screw — don't overtighten!** Layer adhesion in 3D-printed parts is weak; overtightening can split the cap boss or the disc along the layer lines. Tighten just until it clamps and the slider doesn't wobble.
9. **Symmetry comes from measuring + spacers**: measure both sides with a ruler first, then add C-shaped spacers (`k712_inserts.3mf`) on one side as needed until both sides match. **Don't copy the measurement photos, where spacers are fitted on both sides**, or the result will be asymmetric. In this repair they all went on one side.
10. **The ear pads (19) have a bayonet lock** and come off by turning them counter-clockwise (per the manual); this repair doesn't necessarily require removing them.
11. This is a personal repair log. Disassembly is at your own risk and may void your warranty.

---

## 3D printing notes

Both files are **Bambu Studio** project files (3MF with slicer settings), set up for a Bambu Lab A1 with a 0.4 mm nozzle; other slicers (e.g. PrusaSlicer / OrcaSlicer) can usually import the geometry.

| File | Content | Dimensions (measured from model geometry) |
|---|---|---|
| `3d/k712pro_pin_v2.3mf` | **Knob/cover replacement**: 3 × `k712pro_top` (cap, body + 0.6 mm logo inlay, two colors), 4 × `Body1` (inner disc) | Cap Ø15 × approx. 10 mm; logo inlay approx. 9.4 × 10 × 0.6 mm; disc Ø13 × 4.5 mm, center hole approx. Ø2.4 mm |
| `3d/k712_inserts.3mf` | 4 × C-shaped split spacers: **shims for balancing left/right dimensions**, clipped onto the end of the steel wire and added to the shorter side as needed after measuring (not a fixed 2 per side; in this repair all went on one side) | OD Ø4 mm, ID approx. Ø1.6 mm, length 5.8 mm, slotted |

Settings saved in the project files (for reference only):

- Material: in `k712pro_pin_v2` the caps and discs are assigned to **PETG** slots (black body + orange logo, Bambu PETG HF, 240 °C nozzle). In `k712_inserts` the spacers are assigned to slot 1 (PLA Basic), but the thumbnail shows them in orange — choose the material yourself.
- Layer height **0.08 mm** ("0.08mm High Quality" preset), 2 walls, 15% gyroid infill.
- `k712pro_pin_v2` has supports enabled (normal/auto); `k712_inserts` has no supports.
- The plates print more parts than needed (one headphone needs 2 sets of cap + disc); keep the extras as spares.

You'll also need: brass heat-set inserts matching M2 screws, **M2 × 6 mm** screws (one per side), and two braided hair ties (orange in the photos).

---

## Folder structure

```
akg-k712-pro-repair/
├── README.md              English documentation (shown by default on GitHub; this file)
├── README.zh-CN.md        Chinese documentation
├── LICENSE                CC BY-NC-SA 4.0 legal code
├── 3d/
│   ├── k712pro_pin_v2.3mf Cap + disc (replaces parts 3 and 7)
│   └── k712_inserts.3mf   C-shaped spacers (for left/right balancing)
├── images/                Process photos 01–17 (metadata stripped, some areas blurred)
└── ref/
    ├── NOTICE.md          Copyright notice for third-party documents
    ├── Manuale-AKG-K712PRO.pdf
    └── AKGK712.pdf
```

---

## Index

| Path | Description |
|---|---|
| `README.md` | Repair documentation (English, this file) |
| `README.zh-CN.md` | Repair documentation (Chinese) |
| `LICENSE` | Full text of CC BY-NC-SA 4.0 |
| `3d/k712pro_pin_v2.3mf` | Logo cap + inner disc, Bambu Studio project |
| `3d/k712_inserts.3mf` | 4 × C-shaped spacers (added to one side as needed after measuring, to balance left/right), Bambu Studio project |
| `images/01_hair_ties_preparation.jpg` | Preparation: a jar of braided hair ties (to replace the rubber loops) |
| `images/02_printed_pin_caps.jpg` | The three finished two-color caps |
| `images/03_pin_caps_heat_set_inserts.jpg` | Back of the caps, brass heat-set inserts |
| `images/04_screw_size_check.jpg` | Checking the screw size with a gauge (M2 × 6 mm) |
| `images/05_slider_inner_side_screw.jpg` | Inner side of the slider: disc + screw |
| `images/06_slider_outer_side_logo_cap.jpg` | Outer side of the slider: logo cap + hair tie |
| `images/07_sliders_with_elastic_cord.jpg` | Left and right slider assemblies, hair-tie routing |
| `images/08_grille_removal_tweezers.jpg` | Turning the grille counter-clockwise with tweezers |
| `images/09_cord_routing_at_earcup.jpg` | Ear-cup end: hair tie wrapped around the wire end block |
| `images/10_earcup_lid_opened.jpg` | Lid opened, inner structure and leads |
| `images/11_cord_routing_measure_a.jpg` | Measuring left/right dimensions (spacers on both sides here are only a measuring state — don't copy) |
| `images/12_cord_routing_measure_b.jpg` | Measuring left/right dimensions (same as above — don't copy spacer placement) |
| `images/13_reassembled_side.jpg` | Reassembled, side view (background screen blurred) |
| `images/14_reassembled_front.jpg` | Reassembled, front view (background screen blurred) |
| `images/15_reassembled_in_hand.jpg` | Reassembled, in hand |
| `images/16_final_front.jpg` | Finished (front) |
| `images/17_final_side.jpg` | Finished (side) |
| `ref/NOTICE.md` | Copyright notice for the third-party PDFs |
| `ref/Manuale-AKG-K712PRO.pdf` | AKG K712 PRO cutsheet + official K612/K712 service manual (exploded view, parts list, repair hints). **© AKG / HARMAN, not covered by this repo's license** |
| `ref/AKGK712.pdf` | K712 measurement sheet (frequency response, impedance, THD, etc.). **© Source Interlink Media, not covered by this repo's license** |

---

## References

- **AKG K612 / K712 Service Manual** (#2458Z00XXX, 10/2015) and **K712 PRO Cutsheet** — `ref/Manuale-AKG-K712PRO.pdf`. Part numbers, names and the disassembly method in this document are based on this manual. Official site: <https://www.akg.com>
- **AKG K712 Headphone Measurements** — `ref/AKGK712.pdf` (third-party measurements; impedance @1 kHz approx. 67 Ω, approx. 0.237 Vrms needed for 90 dB SPL).

---

## License

The **author's original content** in this repository — the photos (`images/`), the text (`README.md`, `README.zh-CN.md`) and the 3D models (`3d/`) — is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/). See [`LICENSE`](LICENSE) for the full legal code.

- ✅ You may: share, repost, adapt and print for personal use, with attribution and under the same license.
- ❌ You may not: use it for **any commercial purpose** (including selling prints, model files or otherwise profiting from this content).

**The PDFs in `ref/` are not covered by the license above.** They are third-party copyrighted documents (© AKG Acoustics GmbH / HARMAN International; measurement sheet © Source Interlink Media), included as-is for repair reference only. All rights belong to their respective owners, and they will be removed upon request by the rights holder. See [`ref/NOTICE.md`](ref/NOTICE.md).

AKG and K712 are trademarks of AKG Acoustics GmbH. This project is not affiliated with or endorsed by AKG / HARMAN.
