# Wiring Notes — Line Maze Solver Bot PCB

This document explains the wiring and connector usage for the **Line Maze Solver Bot PCB**.

The PCB is designed around:
- **Arduino Nano**
- **TB6612FNG motor driver**
- **IR sensor array**
- **Battery input + switch**
- **Motor output headers**

---

## ✅ 1) Power / Battery Connections

### Battery Input
- Connect the battery to the PCB battery pads/connector.

⚠️ Recommended battery:
- **2S Li-ion / LiPo (7.4V nominal)** OR
- **9V–12V supply** depending on your motor and regulator setup.

> Always verify your TB6612FNG voltage ratings and power path before using 12V.

### ON/OFF Switch
If your PCB has a switch footprint:
- Battery + goes through the switch to power the board.

✅ This allows easy ON/OFF control of the bot.

---

## ✅ 2) Arduino Nano Mounting

- Insert the **Arduino Nano** on the PCB header footprint.
- Make sure the Nano orientation is correct:
  - USB port direction should match the silkscreen/PCB markings.
  - Wrong orientation can damage the board.

---

## ✅ 3) Motor Driver (TB6612FNG) Connections

TB6612FNG handles 2 DC motors:
- **Motor A** = Left motor
- **Motor B** = Right motor

### Motor Output Headers
Connect motors to the screw terminal / header connectors:

| Output Header | Motor |
|-------------|-------|
| MOTOR A     | Left Motor |
| MOTOR B     | Right Motor |

✅ If the bot moves in opposite direction, swap the motor wires or invert direction in code.

---

## ✅ 4) IR Sensor Array Connector

### Purpose
The IR sensor array is used for:
- Line following
- Maze solving
- Detecting left/right/center line position

### Connector Pins (Typical)
Most IR arrays use:
- **VCC (5V)**
- **GND**
- Multiple analog/digital outputs (A0, A1, A2...)

✅ The PCB provides an IR connector with:
- 5V
- GND
- Sensor output pins to Arduino inputs

⚠️ Note:
Confirm the exact pin order from your IR module before connecting.

---

## ✅ 5) Switches / Buttons (SW1, SW2)

### Usage Idea
You can use SW1 and SW2 for:
- Start/Stop bot run
- Mode select (Line follow / Maze mode)
- Calibration trigger (sensor calibration)

Example:
- SW1 = Start
- SW2 = Calibration / Reset

These can be connected to Arduino digital pins with pull-up or pull-down configuration.

---

## ✅ 6) Enable / Control Headers (if present)

Some PCBs include an "EN MOTOR" header:
- Used to enable/disable motor driver output
- Can be connected to Arduino pin or tied to HIGH

If motor driver does not run:
✅ Check:
- STBY/EN pin is HIGH (enabled)
- Arduino is sending PWM correctly

---

## ✅ 7) Recommended Wiring Checklist ✅

Before powering ON:
✅ Battery polarity correct (+/-)  
✅ Arduino Nano properly oriented  
✅ Motor connected to correct output headers  
✅ Sensor array connected with correct pin order  
✅ No short circuits / loose wires  

---

## ✅ 8) Common Issues & Fixes

### Problem: Motors not spinning
✅ Check:
- Battery voltage available
- Motor driver enabled (STBY/EN)
- PWM pins correct
- Motor terminals properly connected

### Problem: Bot moves backward instead of forward
✅ Fix:
- Swap motor wires OR invert direction logic in code

### Problem: Sensor readings unstable
✅ Fix:
- Ensure sensor has proper 5V and GND
- Avoid loose sensor wiring
- Keep sensor wires away from motor wires (noise)

---

✅ Wiring complete — Bot ready for testing 🚀
