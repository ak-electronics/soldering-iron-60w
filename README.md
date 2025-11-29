🔥 60W Soldering Iron Temperature Controller PCB and Gerber

A compact, triac-based AC temperature controller designed for 60W soldering irons.
This project includes the KiCad schematic, PCB design, BOM, and working circuit based on a phase-angle control method (similar to a dimmer).
It allows smooth temperature adjustment using a variable resistor while maintaining simplicity and low cost.

✨ Features

✔️ Triac-based AC power control using BT136-600

✔️ Smooth temperature adjustment using a 500K potentiometer

✔️ Compact PCB layout designed for pen-style soldering irons

✔️ Component values matched to a widely-used reference design

✔️ LED indicator for power/activity

✔️ Optional snubber network for improved stability

✔️ Fully designed in KiCad

📘 How It Works

This controller uses phase-angle control to regulate the power delivered to the soldering iron.
The RC timing network charges each AC cycle and triggers the triac gate through a DIAC (or zener-trigger), controlling how much of each waveform reaches the heating element.

Key functional blocks:

RC timing network → R1 + RV1 + C1

Trigger stage → R2 + DIAC (or zener clamp) + gate resistor

Power switching → BT136-600 triac

Load output → Direct connection to the soldering iron heater

Indicator → LED + resistor

📝 Schematic Preview
🛠 Bill of Materials (BOM)
Ref	Component	Value / Type	Notes
R1	Resistor	560K	RC timing resistor
RV1	Potentiometer	500K	Temperature adjust
R2	Resistor	10K	Trigger series resistor
R3	Resistor	82K–100K	Gate pull-down
C1	Capacitor	104 (0.1µF)	Timing capacitor
D1	LED	—	Power/trigger indicator
DIAC / D2	DB3 (recommended)	—	Triac trigger device
Q1	BT136-600	Triac	Main switching element
J1	AC Input	2-pin	Mains input
J2	Output	2-pin	Soldering iron connection
📂 Repository Structure
📦 Soldering-Iron-60W-Controller
 ├── KiCad/
 │    ├── schematic.kicad_sch
 │    ├── pcb.kicad_pcb
 │    ├── symbols/
 │    └── footprints/
 ├── assets/
 │    ├── schematic.png
 │    ├── pcb_render.png
 ├── README.md
 └── LICENSE

⚠️ Safety Notice

This project operates directly from mains AC voltage, which is dangerous.
Before building or testing:

Use an isolation transformer for experiments

Add a fuse on the AC input

Maintain proper creepage and clearance on the PCB

Use X2-rated capacitors where required

Ensure your soldering iron has proper earth grounding

I am not responsible for injury, damage, or misuse. Work carefully.

🚀 Getting Started

Clone the repo

git clone https://github.com/yourusername/60W-Soldering-Iron-Controller.git


Open the project in KiCad 6/7/8

Review or modify the schematic

Generate and order PCB from your preferred manufacturer

Assemble the board using the BOM

Test with an isolation transformer and proper multimeter tools

🤝 Contributions

Pull requests are welcome!
If you have improvements (snubber, enclosure, thermal feedback, PID control), feel free to share them.

⭐ Support
email me si.akash001@gmail.com
If you like this project, consider giving the repo a star ⭐ on GitHub — it really helps!
