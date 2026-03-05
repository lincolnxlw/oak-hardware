# DM0260_OAK-FFC-CBA

## Overview
Camera Board Assembly (CBA) carrier board for ArduCam compact camera modules (CCMs). Designed by Luxonis as part of the OAK modular camera ecosystem. Interfaces via 26-pin FFC to OAK-FFC baseboards (OAK-FFC-3P, OAK-FFC-4P, OAK-FFC-6P).

- **Board ID:** DM0260
- **Revision:** R2M1E1
- **Design tool:** Altium Designer 23

## Key Specs
- 26-pin 0.5mm FFC interconnect to baseboard (bottom-contact connector)
- 33-pin interface to ArduCam camera modules
- 4-lane MIPI CSI-2
- 3V3 power input via FFC
- On-board power generation with two assembly variants:
  - **FAB_1V0:** Core voltage set to 1.0V (R4 populated) — for IMX-series sensors
  - **FAB_1V2:** Core voltage set to 1.2V (R5 populated) — for OV9x82 sensors
- M12 lens mount support

## Directory Structure
```
PCB/                  # Altium project files
  DM0260.PrjPcb       # Project file
  DM0260.PcbDoc        # PCB layout
  DM0260_CCM.SchDoc    # Camera module schematic
  DM0260_Power.SchDoc  # Power supply schematic
  Project_Information.SchDoc  # Revision history
Docs/                 # Fabrication outputs
  FAB_1V0/            # 1.0V variant fab files (Gerber, BOM, pick-place, drill)
  FAB_1V2/            # 1.2V variant fab files
Images/               # Reference photos and renders
3D_Models/            # Mechanical models
```

## Notes
- PCB source files are Altium (.PcbDoc, .SchDoc, .PrjPcb) — not KiCad
- Board outline matches older FFC CBA revisions (drop-in compatible)
- Two assembly variants differ only in which 0R resistor is populated (R4 vs R5) to set sensor core voltage
