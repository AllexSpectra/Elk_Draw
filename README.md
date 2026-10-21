# Elk_Draw ELG

Elk_Draw is an editor for chemical structures and reactions on Windows. **ELG** is its light edition:
the whole editor, free for private use, teaching and non-commercial academic research
(see [LICENSE.txt](LICENSE.txt)).

This repository only holds the downloads. Get the latest version under
**[Releases](../../releases)**.

## What ELG does

- Drawing structures, reactions, brackets, text and shapes; templates and a fragment library: rings,
  functional and protecting groups; acids (including HBF4 and HBPh4), bases, reagents and solvents; cages
  and macrocycles drawn in 3D perspective (adamantane, triptycene, POSS, cucurbit[n]urils, cyclodextrins,
  calixarenes, porphyrins); metal complexes with coordinate bonds (ferrocene, Ir(ppy)3, Ir(ppy)2(acac),
  Gd contrast agents, Eu and Tb diketonates); natural products (caffeine, cholesterol); dyes and pigments
  (coumarins, Nile Red, aza-BODIPY, rhodamine B, perylene diimide, DPP, HPTS).
- Properties panel: formula, molecular weight, exact mass, logP, TPSA, H-bond donors and acceptors,
  rotatable bonds, Fsp3, rule of five, SMILES; selected values can be inserted as text.
- Analyze menu: structure information, estimated physical properties (Joback), structure check, formula and
  geometry optimisation (force field).
- Structures in Microsoft Word: insert them, double-click to edit them in Elk_Draw.
- Files: Elk_Draw's own format and common chemistry formats (MOL/SDF, SMILES, CDXML and others);
  export as pictures.

The quantum-chemical calculations of the full edition (MOPAC, xtb, TD-DFT) and NMR prediction are
shown in the menus but are not part of ELG.

## Installing

Windows 10 or 11, 64-bit. Nothing else is needed: no .NET, no administrator rights.

- **Elk_Draw-ELG.msi** – installer. Installs for your Windows user into
  `%LocalAppData%\Programs\Elk_Draw ELG`, adds a Start menu and a desktop shortcut and registers
  Elk_Draw for Word. Remove it under *Settings › Apps*. A newer installer updates an older one.
  Settings are kept in `%APPDATA%\Elk_Draw`.
- **Elk_Draw-ELG.zip** – portable copy. Unzip anywhere and start `Elk_Draw.exe`. Settings are kept in
  the `Data` folder next to the program. To use it with Word, run `Register in Word.cmd` once.

Windows may warn that the installer comes from an unknown publisher (it is not code-signed yet):
choose *More info › Run anyway*.

## Licence

Copyright © 2026 Oleksandr Karasyov. Free for private use, teaching and non-commercial academic
research; commercial use needs permission. The full terms (German, binding, and English) are in
[LICENSE.txt](LICENSE.txt). Components by others and their licences:
[THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) and the [licenses](licenses) folder.

Contact: alexkarasyov0@gmail.com
