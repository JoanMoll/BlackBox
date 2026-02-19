# BlackBox — Room Health / Environmental Monitoring PCB

A custom **KiCad PCB** for a battery-powered, ESP32-class device intended to monitor room/environment conditions and log data locally.

## What’s in this repo
This repository contains the **hardware design source files**:
- KiCad project: `.kicad_pro`
- Schematic: `.kicad_sch`
- PCB layout: `.kicad_pcb`
- 3D model export: `.step` (if included)

> Note: fabrication outputs (Gerbers, drill files, etc.) may be generated from the KiCad project. If present in the repo, they are provided for reference only.

## Intended system (high-level)
Planned functional blocks:
- **MCU / Wireless:** ESP32-class microcontroller
- **Sensors:** LDR (ambient light), ultrasonic (distance/proximity), plus analog sensor input(s)
- **Analog front-end:** LMV321 op-amp stage for conditioning/amplifying analog signals
- **Storage:** micro-SD card for local data logging
- **Power:** battery input (VBAT) with 3.3 V regulation and battery management/protection

## How to open the design
1. Install **KiCad** (v7+ recommended).
2. Open the `.kicad_pro` file in this repository.
3. From KiCad:
   - Open the schematic (`.kicad_sch`)
   - Open the PCB (`.kicad_pcb`)
   - Run **ERC** (schematic checks) and **DRC** (PCB checks) as needed.

## Status
- ✅ Schematic and PCB layout created
- 🔜 Final DRC/ERC pass and documentation polish
- 🔜 Order PCB and perform bring-up tests (power rails, SD, sensor IO)
- 🔜 Firmware (logging format + sampling) and enclosure design

## Why this project
This is a portfolio hardware design artifact demonstrating:
- PCB layout + schematic capture workflow in KiCad
- Practical embedded hardware system design (power, sensing, storage, interfaces)
- Manufacturing-ready outputs via Gerber generation (when finalized)

## License
If no license file is included, assume **all rights reserved** (portfolio viewing only).