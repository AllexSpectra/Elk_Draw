# Elk_Draw — third-party notices

Elk_Draw is written from scratch. The components below are not written by its author; they are
included in the program as published by their authors, under the licences named here. This file and
the `licenses` folder next to it are shipped with every build of Elk_Draw.

Checked against the package list (`dotnet list ChemEditor.sln package --include-transitive`) and the
licence files in the NuGet packages on 15 October 2026. When a package is added or updated, check
this file again (see the end).

---

## Components and licences

| Component | Version | Used for | Licence | Copyright | Full text |
|---|---|---|---|---|---|
| .NET runtime and libraries | 10.0 | the program's runtime (inside the self-contained, Mac and Native AOT builds) | MIT | © .NET Foundation and Contributors | `licenses/DotNet-LICENSE.txt`; parts by others: `licenses/DotNet-THIRD-PARTY-NOTICES.txt` |
| Avalonia, Avalonia.Desktop, Avalonia.Themes.Fluent, Avalonia.Skia, Avalonia.Win32, Avalonia.Native, Avalonia.X11, Avalonia.FreeDesktop, Avalonia.Remote.Protocol | 11.3.22 | user interface | MIT | Copyright 2013-2026 © The AvaloniaUI Project | MIT text below |
| Avalonia.Fonts.Inter | 11.3.22 | package that carries the Inter typeface | MIT | Copyright 2013-2026 © The AvaloniaUI Project | MIT text below |
| Inter typeface (inside Avalonia.Fonts.Inter) | 3.019 | user-interface font | SIL Open Font License 1.1 | Copyright 2020 The Inter Project Authors (https://github.com/rsms/inter). "Inter" is a trademark of rsms. | `licenses/Inter-OFL.txt` |
| Avalonia.Angle.Windows.Natives (ANGLE, `av_libglesv2.dll`) | 2.1.25547.20250602 | Avalonia's OpenGL layer on Windows | BSD 3-Clause | Copyright 2018 The ANGLE Project Authors; package © 2013-2025 The AvaloniaUI Project | `licenses/ANGLE-LICENSE.txt` |
| SkiaSharp (+ SkiaSharp.NativeAssets.*) | 2.88.9 | 2D drawing | MIT | Copyright (c) 2015-2016 Xamarin, Inc.; Copyright (c) 2017-2018 Microsoft Corporation | MIT text below |
| HarfBuzzSharp (+ HarfBuzzSharp.NativeAssets.*) | 8.3.1.1 | text shaping | MIT | Copyright (c) 2015-2016 Xamarin, Inc.; Copyright (c) 2017-2018 Microsoft Corporation | MIT text below |
| Native libraries inside SkiaSharp and HarfBuzzSharp: Skia, HarfBuzz, ANGLE, FreeType, libpng, zlib, expat, libjpeg-turbo, libwebp, ICU, sfntly, piex, DNG SDK and others | as shipped in the packages above | drawing, fonts and images | various (BSD, MIT, "Old MIT", FreeType, zlib, libpng, ICU, Apache-2.0, …) | their authors, as listed in the file | `licenses/SkiaSharp-HarfBuzzSharp-NOTICES.txt` (Microsoft's own notice file from the packages, unchanged) |
| MicroCom.Runtime | 0.11.0 | Avalonia's native interop | MIT | Copyright 2021 © Nikita Tsukanov | MIT text below |
| Tmds.DBus.Protocol | 0.21.3 | Avalonia on Linux only | MIT | Copyright Tom Deseyn | MIT text below |
| InChIKey hashing procedure (ported into InchiKey.cs) | — | computing InChIKeys | MIT | © IUPAC and InChI Trust | MIT text below |

### Not shipped (used only to build or test)

- Avalonia.BuildServices 11.3.2 (MIT, © The AvaloniaUI Project) — build-time only.
- Test packages: xunit 2.9.2 with xunit.core, xunit.assert, xunit.extensibility.core,
  xunit.extensibility.execution 2.9.2, xunit.abstractions 2.0.3, xunit.analyzers 1.16.0,
  xunit.runner.visualstudio 2.8.2 (Apache-2.0); Microsoft.NET.Test.Sdk, Microsoft.CodeCoverage,
  Microsoft.TestPlatform.ObjectModel, Microsoft.TestPlatform.TestHost 17.11.1 (MIT);
  Newtonsoft.Json 13.0.1 (MIT).
- RDKit (BSD 3-Clause) — continuous-integration checks only.
- The HarfBuzzSharp/SkiaSharp WebAssembly assets are in the package list but not used by any
  Elk_Draw build.

### External programs (not included)

Elk_Draw can start these if the user has installed them, but does **not** include them: MOPAC
(Apache-2.0), xtb (LGPL-3.0), Python and its packages. If any of them is ever shipped with Elk_Draw,
add its licence here.

---

## MIT License

Applies to every component listed above as MIT, each under its own copyright line from the table.

```
MIT License

Copyright (c) <the copyright holders listed in the table above>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Other licences

The full texts of the BSD (ANGLE), SIL Open Font License (Inter) and all licences of the native
libraries inside SkiaSharp/HarfBuzzSharp and the .NET runtime are in the `licenses` folder:

| File | Contents |
|---|---|
| `licenses/DotNet-LICENSE.txt` | .NET MIT licence |
| `licenses/DotNet-THIRD-PARTY-NOTICES.txt` | components inside the .NET runtime |
| `licenses/ANGLE-LICENSE.txt` | ANGLE BSD licence (Avalonia's copy) |
| `licenses/Inter-OFL.txt` | SIL Open Font License 1.1 for Inter |
| `licenses/SkiaSharp-HarfBuzzSharp-NOTICES.txt` | Skia, HarfBuzz, FreeType, libpng, zlib and the other native libraries |

The Inter font is not modified and not sold on its own.

---

## Trademarks

ChemDraw is a registered trademark of Revvity Signals Software, Inc. Elk_Draw reads and writes the CDX and
CDXML file formats, from their published specification, to exchange drawings with other programs; it is not
affiliated with, endorsed or sponsored by Revvity. Other names used to identify file formats or programs may
be trademarks of their owners.

## Keeping this file correct

1. After adding or updating a NuGet package, run in the project folder:
   `dotnet list ChemEditor.sln package --include-transitive > packages.txt`
   — every package listed under Chem.UI ends up in the program and needs a row above.
2. The licence of each package is in `%USERPROFILE%\.nuget\packages\<package>\<version>\` (the
   `.nuspec` file names the licence and copyright; some packages also have LICENSE or
   THIRD-PARTY-NOTICES files — copy those into `licenses`).
3. `src/Chem.UI/Chem.UI.csproj` copies this file and the `licenses` folder into every build
   (all publish scripts, Windows and Mac), so nothing has to be copied by hand.
