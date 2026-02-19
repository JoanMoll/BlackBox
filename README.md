# BlackBox

Custom KiCad PCB for an ESP32-class, battery-powered environmental/room monitoring device.

## What it does
- Reads sensors: LDR (ambient light), ultrasonic (distance/proximity), + analog sensor input via op-amp stage (LMV321)
- Logs data to micro-SD
- Battery powered: VBAT → 3.3V regulation + power management

## Hardware overview
- MCU: ESP32 (planned)
- Sensors: LDR, ultrasonic, analog front-end (LMV321)
- Storage: micro-SD
- Power: battery (VBAT) + 3.3V rail

## Repo structure
- `hardware/` (or root): KiCad project files (`.kicad_pro/.kicad_sch/.kicad_pcb`)
- `docs/`: exports (schematic PDF, PCB renders)
- `fab/`: manufacturing outputs (gerbers) (optional)

## How to open
Install KiCad and open the `.kicad_pro` file.

## Status
- ✅ Schematic + PCB layout
- 🔜 DRC/ERC clean + manufacture gerbers
- 🔜 Order PCB + bring-up tests (power rails, SD, sensor IO)
- 🔜 Firmware + logging format
- 🔜 Enclosure

## Notes
This repo is intended as a portfolio hardware design artifact.
