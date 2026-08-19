# USB-2.0-Hub-PCB
PCB Design of 2 Layer USB 2.0 Hub in KiCad, comprising Schematic design, PCB Layout &amp; Routing, DRC Checking, 3D Visualization and Gerber Files




USB 2.0 Hub PCB Design

📌 Project Overview

This project presents the complete schematic and PCB design of a USB 2.0 Hub developed using KiCad.

The design includes the USB upstream interface, USB hub controller, downstream USB ports, ESD protection, power distribution, clock circuitry, reset circuitry, decoupling capacitors, and supporting passive components.



The project was developed following a complete PCB design workflow:

Schematic Design → Footprint Assignment → PCB Layout → Routing → 3D Verification → Gerber Generation → Bill of Materials (BOM).

The purpose of this project is to demonstrate practical skills in USB interface design, PCB schematic capture, component placement, PCB routing, design-rule verification, manufacturing preparation, and hardware documentation.



🎯 Project Objectives

The main objectives of this project are:
Design a functional USB 2.0 Hub PCB.
Create the complete electrical schematic.
Select appropriate electronic components and footprints.
Design the PCB layout using KiCad.
Route USB differential signal pairs appropriately.
Implement USB power distribution.
Include ESD protection for USB interfaces.
Implement reset and clock circuitry.
Add appropriate decoupling and bypass capacitors.
Perform Electrical Rules Check (ERC).
Perform Design Rules Check (DRC).
Verify the PCB using KiCad 3D Viewer.
Generate manufacturing-ready Gerber files.
Prepare a Bill of Materials (BOM).
Document the complete hardware design process.


🧩 System Architecture

The general architecture of the USB 2.0 Hub is:

                         USB HOST / COMPUTER
                                │
                                │
                         USB 2.0 UPSTREAM
                                │
                                ▼
                    ┌─────────────────────┐
                    │ Upstream Connector  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ ESD / USB Protection│
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   USB Hub Controller│
                    │         IC          │
                    └──────┬───┬───┬──────┘
                           │   │   │
                 ┌─────────┘   │   └─────────┐
                 ▼             ▼             ▼
          ┌───────────┐ ┌───────────┐ ┌───────────┐
          │ USB Port 1│ │ USB Port 2│ │ USB Port 3│
          └───────────┘ └───────────┘ └───────────┘
                                             │
                                      ┌───────────┐
                                      │ USB Port 4│
                                      └───────────┘

The exact architecture and number of ports depend on the implemented USB hub controller and final schematic.

🔌 USB Interfaces

The PCB contains:

Upstream USB Interface

The upstream interface connects the USB hub to a host computer or USB-enabled device.

It carries:

USB VBUS
USB D+
USB D−
GND
Downstream USB Interfaces

The downstream interfaces provide USB connectivity to external devices such as:

USB flash drives
USB keyboards
USB mice
USB development boards
Other USB 2.0-compatible peripherals

🛡️ Protection Circuitry

USB connectors are exposed to external devices and therefore require protection against electrostatic discharge and other transient events.

The design includes USB protection circuitry to improve interface robustness.

The protection section is intended to protect the USB signal and power lines while maintaining the required USB signal path.

⚡ Power Section

The power section distributes the required supply voltage to the USB hub controller and downstream USB interfaces.

The design includes appropriate:

Power input
VBUS connections
Ground connections
Decoupling capacitors
Power filtering/protection components

Care was taken to provide appropriate power paths and local bypass capacitors near the hub controller and other active components.

⏱️ Clock and Reset Circuitry

The USB hub controller requires appropriate clock and reset circuitry for reliable operation.

The design includes:

Clock/crystal circuitry
Load capacitors where required
Reset circuitry
Supporting passive components

These components are placed close to the relevant controller pins to reduce unnecessary routing and improve PCB implementation.

🖥️ Schematic Design

The complete schematic was developed using KiCad Schematic Editor.

The schematic includes:

USB upstream interface
USB downstream interfaces
USB hub controller
ESD protection
Power distribution
Clock circuit
Reset circuit
Decoupling capacitors
Pull-up/pull-down resistors
Supporting passive components
Schematic


A PDF version of the schematic is also provided in:

Schematic/Schematic_PDF.pdf
🟩 PCB Design

The PCB was designed using KiCad PCB Editor.

The PCB design process included:
Importing the schematic netlist into PCB Editor.
Assigning and verifying footprints.
Defining the board outline.
Placing components.
Routing signal traces.
Routing USB differential pairs.
Designing power connections.
Adding the ground plane.
Checking clearances.
Running DRC.
Performing 3D verification.
PCB Layout




📐 PCB Design Considerations

The following PCB design considerations were taken into account:
Component placement
Short and direct USB signal routing
USB differential pair routing
Ground return paths
Power distribution
Decoupling capacitor placement
Connector accessibility
PCB edge clearance
Track-to-track clearance
Thermal considerations
Silkscreen readability
Manufacturing constraints


🧪 Design Verification
The PCB design was verified using KiCad's electrical and physical design-checking tools.

ERC — Electrical Rules Check

ERC was used to identify electrical connectivity issues in the schematic.

Checks included:

Unconnected pins
Power connection issues
Incorrect electrical connections
Missing power drivers
Signal connectivity
DRC — Design Rules Check

DRC was performed on the PCB layout.

Checks included:

Track clearance
Pad clearance
Via clearance
Copper-to-edge clearance
Unconnected nets
Silkscreen violations
Hole and board-edge checks
Manufacturing-rule violations
DRC Result




Genuine design violations were reviewed and corrected before finalizing the PCB.

🧊 3D PCB Verification
KiCad 3D Viewer was used to inspect the completed PCB.

The 3D inspection helped verify:

Component placement
Connector orientation
Component height
PCB outline
Mechanical arrangement
Overall board appearance
3D Top View
3D Bottom / Angled View


🧾 Bill of Materials
A Bill of Materials is included in:

Manufacturing/BOM.csv

The BOM contains information such as:

Parameter	Description
Reference	Component reference designator
Component	Component type
Value	Component value
Footprint	Assigned PCB footprint
Quantity	Required quantity


🏭 Manufacturing Files
Manufacturing files are provided in the Gerber directory.

Gerber/
└── USB_2.0_Hub_Gerbers.zip
The Gerber package contains the fabrication data required for PCB manufacturing, including the relevant copper, solder mask, silkscreen, board outline, and drill information.
The Gerber package should be reviewed using a Gerber viewer before sending the design for fabrication.

🔄 PCB Design Workflow
Project Requirements
        ↓
Block Diagram
        ↓
Schematic Design
        ↓
Component Selection
        ↓
Footprint Assignment
        ↓
PCB Import
        ↓
Board Outline
        ↓
Component Placement
        ↓
USB Differential Pair Routing
        ↓
Power Routing
        ↓
Ground Plane
        ↓
ERC Verification
        ↓
DRC Verification
        ↓
3D PCB Inspection
        ↓
Gerber Generation
        ↓
Manufacturing Package


🛠️ Software and Tools

Design Software
KiCad
KiCad Schematic Editor
KiCad PCB Editor
KiCad 3D Viewer
KiCad Gerber Viewer
Version Control
Git
GitHub



💡 Technical Skills Demonstrated
This project demonstrates practical experience in:

PCB schematic design
PCB layout
Component selection
Footprint assignment
USB 2.0 interface design
USB differential pair routing
ESD protection
Power distribution
Decoupling
Ground-plane design
Component placement
PCB routing
ERC verification
DRC verification
3D PCB visualization
Gerber generation
BOM preparation
Hardware documentation
Git/GitHub version control



📂 Repository Structure
USB-2.0-Hub-PCB/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── Schematic/
│   ├── USB_2.0_Hub.kicad_sch
│   └── Schematic_PDF.pdf
│
├── PCB/
│   ├── USB_2.0_Hub.kicad_pcb
│   └── PCB_3D_View.png
│
├── Gerber/
│   └── USB_2.0_Hub_Gerbers.zip
│
├── Manufacturing/
│   └── BOM.csv
│
├── Documentation/
│   └── Project_Report.pdf
│
└── Images/
    ├── 01_Block_Diagram.png
    ├── 02_Schematic.png
    ├── 03_PCB_Layout.png
    ├── 04_3D_Top_View.png
    ├── 05_3D_Bottom_View.png
    ├── 06_DRC_Result.png
    └── 07_Gerber_Viewer.png



🚀 Future Improvements
Possible future improvements include:

Fabrication of the PCB
PCB assembly and soldering
Hardware bring-up and testing
USB enumeration testing
USB data-transfer testing
Power-consumption measurements
Signal-integrity verification
ESD testing
Thermal testing
Validation of all downstream USB ports
Hardware debugging and performance optimization
📊 Project Status
Stage	Status
Requirements	✅ Completed
Schematic Design	✅ Completed
Component Selection	✅ Completed
Footprint Assignment	✅ Completed
PCB Layout	✅ Completed
PCB Routing	✅ Completed
ERC	✅ Completed
DRC	✅ Completed
3D Verification	✅ Completed
Gerber Generation	✅ Completed
PCB Fabrication	⏳ Future Work
Hardware Testing	⏳ Future Work



📜 License
This project is released under the CERN Open Hardware Licence – Permissive (CERN-OHL-P) v2.0.
See the LICENSE file for the complete license terms.

👨‍💻 Author

Mitte Devaranganath

B.Tech — Electronics and Communication Engineering

Areas of Interest
PCB Design
Digital Electronics
FPGA Design
Verilog/SystemVerilog
Hardware Design


⭐ Project Summary
This project demonstrates the complete development workflow of a USB 2.0 Hub PCB, from schematic capture and component selection through PCB layout, routing, verification, 3D inspection, and manufacturing-file generation.

The repository contains the design source files and supporting documentation required to understand, review, modify, and potentially manufacture the PCB.
