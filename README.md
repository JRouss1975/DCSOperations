# DCS Operations

Windows desktop tool that reads ship **Data Collection System (DCS)** Excel
exports and analyses and plots the logged operational data.

---

## At a glance

| | |
| --- | --- |
| **Type** | Windows desktop app (WPF) |
| **Built with** | C# · .NET Framework 4.7.2 |
| **Status** | Stable: no recent changes (published May 2022) |

---

## Features

- **Open DCS workbooks** (`.xlsx` / `.xls`) and read the company name and reporting period.
- **Charts** of the operational parameters (OxyPlot).
- **Numeric analysis** of the logged data (MathNet.Numerics).
- Useful for post-voyage review of fuel and operational data.

---

## Requirements

| | |
| --- | --- |
| Operating system | Windows 10 or 11 |
| Runtime | .NET Framework **4.7.2** or newer |
| Build | Visual Studio 2019 or 2022 with the **.NET desktop development** workload |
| Other | Microsoft Excel, to read the DCS workbooks (Office Interop) |

---

## Building and running

1. Open `WPF_DCSOperations.sln` in Visual Studio.
2. NuGet packages restore automatically on the first build.
3. Build and run with **F5**, then open a DCS export.

---

## Project structure

```
WPF_DCSOperations.sln
WPF_DCSOperations/
├─ Info.cs                  workbook metadata (company, dates)
├─ Observable.cs            property-change base class
├─ MainWindow.xaml(.cs)     main window, reading and charting
└─ Measurements.*.apk       legacy mobile builds, kept for reference
Ref.7z                      reference material
```

---

## Dependencies

| Package | Used for |
| --- | --- |
| OxyPlot.Wpf | Charts |
| MathNet.Numerics | Numeric analysis |
| Extended.Wpf.Toolkit (Xceed) | Data grids |
| Microsoft.Office.Interop.Excel | Reading DCS workbooks |

---

## Notes

The `Measurements.*.apk` files in the project folder are an old build of the
[Measurements Mobile](https://github.com/JRouss1975/Measurements_Mobile_Xamarin) app and
are not used by this application.

---

## License

Copyright © JRouss1975. All rights reserved.

No license is granted to use, copy, modify or distribute this code without written permission.
