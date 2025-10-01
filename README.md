# SU WaterCam PCB

This repository contains the KiCad design files for a custom PCB for **SU-WaterCam**, integrating the FLIR Lepton thermal camera, Bosch BNO055 IMU, Multitech mDot LoRa module, and Witty Pi 4 RTC board. 

---

## 🔧 Design Overview

- **Layers**: 2-layer PCB (F.Cu, B.Cu)
- **Components**:
  - FLIR Lepton thermal imaging module
  - Bosch BNO055 9-DOF absolute orientation sensor
  - Multitech mDot LoRa module
  - Witty Pi 4 RTC and power manager
- **Power Domains**:
  - 3.3V and 5V rails with copper fill zones
  - Mounting via Witty Pi 4-compatible headers
- **Interfaces**:
  - FFC cutout for FLIR Lepton
  - I²C / UART routing for sensors
  - LoRa antenna trace or u.FL footprint

---

## Electrical & Layout Highlights

- **Trace widths**:
  - Signal: 0.25 mm
  - Power: 0.5 mm (5V rail)
- **Clearance**: 0.20 mm (net class default)
- **Mechanical**:
  - Slot for ribbon cable (Edge.Cuts layer)
  - Mounting holes aligned for case/enclosure compatibility

---

## Custom Libraries

The project uses custom symbols and footprints located in:

- `symbols/mDOT.kicad_sym`
- `footprints/FLIR Lepton.pretty`
- `footprints/MDOT.pretty`
- `footprints/Witty Pi 4.pretty`

Library tables (`fp-lib-table` and `sym-lib-table`) are included and use relative paths for portability.
