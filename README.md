# Elk_Draw

Elk_Draw is an editor for chemical structures and reactions on Windows, macOS and Linux:
the whole editor, free for private use, teaching and non-commercial academic research
(see [LICENSE.txt](LICENSE.txt)).

This repository only holds the downloads. Get the latest version under
**[Releases](../../releases)**.

## What Elk_Draw does

- Drawing structures, reactions, brackets, text and shapes; templates and a fragment library: rings,
  functional and protecting groups (including silyl groups); acids (including HBF4 and HBPh4), bases,
  reagents, peptide coupling reagents and solvents; cages
  and macrocycles drawn in 3D perspective (adamantane, triptycene, POSS, cucurbit[n]urils, cyclodextrins,
  calixarenes, porphyrins; cucurbiturils also from the side, for host–guest drawings with a guest placed in
  the cavity and drawn in depth); metal complexes with coordinate bonds (ferrocene, Ir(ppy)3, Ir(ppy)2(acac),
  Gd contrast agents, Eu and Tb diketonates); natural products (caffeine, cholesterol); dyes and pigments
  (coumarins, Nile Red, aza-BODIPY, rhodamine B, perylene diimide, DPP, HPTS).
- Properties panel: formula, molecular weight, exact mass, logP, TPSA, H-bond donors and acceptors,
  rotatable bonds, Fsp3, rule of five, SMILES; selected values can be inserted as text.
- Analyze menu: structure information, estimated physical properties (Joback), structure check, formula and
  geometry optimisation (force field).
- Structures in Microsoft Word: insert them, double-click to edit them in Elk_Draw.
- Files: Elk_Draw's own format and common chemistry formats (MOL/SDF, SMILES, CDXML and others);
  export as pictures.

The quantum-chemical calculations (MOPAC, xtb, TD-DFT) and NMR prediction are shown in the menus
but are part of Elk_Draw Pro only.

## Installing

Nothing else needs to be installed on any of the systems: no .NET, no administrator rights.

### Windows

Windows 10 or 11, 64-bit.

- **Elk_Draw.msi** – installer. Installs for your Windows user into
  `%LocalAppData%\Programs\Elk_Draw`, adds a Start menu and a desktop shortcut and registers
  Elk_Draw for Word. Remove it under *Settings › Apps*. A newer installer updates an older one.
  Settings are kept in `%APPDATA%\Elk_Draw`.
- **Elk_Draw.zip** – portable copy. Unzip anywhere and start `Elk_Draw.exe`. Settings are kept in
  the `Data` folder next to the program. To use it with Word, run `Register in Word.cmd` once.

Windows may warn that the installer comes from an unknown publisher (it is not code-signed yet):
choose *More info › Run anyway*.

### macOS and Linux – preview

> **Preview, not yet tested on a real Mac or Linux PC.** The programs are built automatically and
> compile cleanly, but nobody has started them yet. Please report problems as an
> [issue](https://github.com/AllexSpectra/Elk_Draw/issues).

### macOS

macOS 14 (Sonoma) or newer.

- **Elk_Draw-mac-AppleSilicon.zip** – for Macs with M1, M2, M3 or M4 chips.
- **Elk_Draw-mac-Intel.zip** – for older Macs with Intel chips.

Unzip and move **Elk_Draw.app** to *Applications*. The app is not signed by Apple yet, so the first
time right-click (or Control-click) it and choose *Open*, then *Open* again. If macOS only offers
*Move to Bin*, open *System Settings › Privacy & Security* and click *Open Anyway* next to Elk_Draw.
Settings are kept in `~/Library/Application Support/Elk_Draw`. The zip also contains
`Elk_Draw.dotm`, which adds an Elk_Draw tab to Word for Mac (see *READ ME FIRST.txt*).

### Linux

64-bit (x64) Linux with a desktop.

- **Elk_Draw-linux-x64.tar.gz** – unpack it anywhere (`tar -xzf Elk_Draw-linux-x64.tar.gz`) and
  start `./Elk_Draw` in the `Elk_Draw` folder. Settings are kept in `~/.config/Elk_Draw`.

Word integration is available on Windows and macOS only. On macOS and Linux, descriptors and InChI use
Elk_Draw's own code.

Up to version 0.9.7 this edition was called **Elk_Draw ELG** (files `Elk_Draw-ELG.msi` and
`Elk_Draw-ELG.zip`, installed into `%LocalAppData%\Programs\Elk_Draw ELG`). Those releases keep their old names.

## Licence

Copyright © 2026 Oleksandr Karasyov. Free for private use, teaching and non-commercial academic
research; commercial use needs permission. The full terms (German, binding, and English) are in
[LICENSE.txt](LICENSE.txt). Components by others and their licences:
[THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) and the [licenses](licenses) folder.

ChemDraw is a registered trademark of Revvity Signals Software, Inc. Elk_Draw reads and writes the CDX
and CDXML file formats to exchange drawings; it is not affiliated with, endorsed or sponsored by Revvity.
Other names may be trademarks of their owners.

Contact: alexkarasyov0@gmail.com
