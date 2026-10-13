# DCS Operations

Desktop tool that reads ship Data Collection System (DCS) Excel exports and
analyses and plots the operational data.

## Overview

Open a DCS workbook, read its company and date range, and inspect the data
through charts. Useful for post-voyage review of logged operational parameters.

## Features

- Open `.xlsx` / `.xls` DCS exports
- Company, start and end date metadata
- Charting with OxyPlot
- Numeric analysis with MathNet.Numerics

## Tech stack

- WPF, .NET Framework 4.7.2
- OxyPlot, MathNet.Numerics
- Microsoft Office Interop (Excel)

## Repository layout

```
WPF_DCSOperations/
  Info.cs, Observable.cs
  MainWindow.xaml / MainWindow.xaml.cs
  Measurements.*.apk     (bundled legacy mobile build)
WPF_DCSOperations.sln
```

## Notes

The bundled `Measurements.*.apk` files are a legacy mobile build and are kept
only for reference.
