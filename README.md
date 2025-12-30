# ZeroBug Hexapod (Fork)

**Important** I haven't built this yet so don't follow this guide until I post full instructions.

A fork of the original ZeroBug hexapod by Max.K, redesigned for robust power delivery, modular expansion, and stable servo performance using widely available components. Ideal for hobbyists.
---

## **Features**

* 20 MG90S micro servos: 18 for legs, 2 for a front-mounted claw
* Dual PCA9685 16-channel PWM drivers for precise, synchronized servo control
* High-current UBECs with shared ground bus for stable power under heavy loads
* Spare servo ports for future expansion (manipulators, sensors, accessories)
* 3-DOF-per-leg inverse kinematice for omnidirectional locomotion, strafing, rotation, and dynamic gaits (tripod, ripple, wave)
* Raspberry Pi Zero W controller with Bluetooth PS4 controller input
* Reinforced, 3D-printable frame for improved alignment and structural integrity
* Modular software architecture separating high-level motion planning from low-level servo actuation

---

## **Hardware Overview**

* Servos: MG90S micro servos, widely available, easy to replace
* Drivers: 2 × PCA9685 PWM controllers, I²C interface
* Power: High-current UBECs providing clean 5–6 V, isolated logic supply
* Grounding: Shared ground bus for signal integrity and stable voltage
* Frame: Original ZeroBug CAD design with reinforced geometry, 3D-printed

---

## **Power & Wiring**

* Each PCA9685 driver powered by its own 15 A UBEC to handle servo load spikes
* Shared ground bus ensures stable PWM signal and reduces glitches
* Raspberry Pi can be powered separately or from a UBEC with voltage isolation
* Wiring supports easy expansion and addition of extra servo devices

---

## **Software & Control**

* High-level motion planning and gait generation run on the Raspberry Pi Zero W
* Real-time 3D inverse kinematics per leg for precise foot positioning
* Omnidirectional walking, rotation, and compound maneuvers supported
* Remote control via Bluetooth gamepad
* Software separates high-level logic from low-level PWM actuation, ensuring stable multi-servo updates

---

## **Expansion**

* Extra servo ports allow adding additional manipulators, sensors, or custom devices
* Modular architecture supports future software upgrades and custom gaits
* Easily upgradable to new hardware thanks to standardized, widely available components

---

## **Getting Started**

1. Print the frame using provided CAD files
2. Assemble electronics following wiring diagram
3. Connect UBECs with shared ground bus and isolated logic supply
4. Install Raspberry Pi software and dependencies
5. Pair BT gamepad for remote control
6. Boot it up and hope there's no smoke!

---

## **License**
This project is licensed under the GNU General Public License v3.0 (GPL-3.0).

You are free to use, modify, and redistribute this software and its associated hardware designs, provided that any derivative works are also distributed under the same license. There is no warranty for the software or hardware; use it at your own risk.

