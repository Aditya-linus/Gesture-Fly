# Additional Component Testing

This section caontains the testing procedures and results for the remaining hardware components used in the GestureFly project.

---

# 720 Coreless Motor Testing

## Overview

720 coreless brushed motors are used as the propulsion system of the drone.

These motors were selected because they are:
- lightweight
- inexpensive
- commonly used in micro drones

# Testing Procedure

1. Connected a single motor directly to a AA battery.
2. Verified motor spin direction.
3. Tested all four motors individually.
4. Measured resistance values using a multimeter.


# Results

✅ All motors spun successfully

✅ No overheating observed

✅ No vibration issues detected

✅ No burning smell observed

✅ Motors operated smoothly


<img width="720" height="1600" alt="WhatsApp Image 2026-05-27 at 21 01 15" src="https://github.com/user-attachments/assets/5b67a09a-2f61-4009-ba32-efc2e84fa3d1" />

---

# Observations

| Motor | Resistance |
|---|---|
| Motor 1 | ~1.2Ω |
| Motor 2 | ~1.2Ω |
| Motor 3 | ~1.2Ω |
| Motor 4 | ~0.9–1.0Ω |

One motor had slightly lower resistance and appeared to spin slightly faster than the others.


# LiPo Battery Testing

## Overview

A 1S LiPo battery is used because :
- lightweight design
- compatibility with brushed motors
- compact size

---

# Testing Procedure

1. Measured battery voltage using multimeter.
2. Connected battery to DRV8833 motor driver.
3. Verified motor operation under LiPo power.

---
<img width="720" height="1600" alt="WhatsApp Image 2026-05-27 at 21 04 05" src="https://github.com/user-attachments/assets/3279de5b-5f14-40b4-88fe-959af39b9c9d" />

# Results

✅ Battery voltage measured approximately 4.19V fully charged

✅ Successfully powered motors

✅ Stable power delivery verified

# Frame Prototype Testing

## Overview

A 75mm TinyWhoop-style frame is selected as the base platform for the project.

The frame is :
- lightweight
- has propeller protection
- is suitable for indoor testing

---

# Planned Material

| Property | Value |
|---|---|
| Material | PETG |
| Layer Height | 0.15mm |
| Infill | 30% |
| Printing Method | FDM |

---

# Overall Hardware Status

| Component | Status |
|---|---|
| ESP32-C3 | ✅ Tested |
| MPU6050 | ✅ Tested |
| DRV8833 | ✅ Tested |
| 720 Motors | ✅ Tested |
| Propellers | ✅ Tested |
| TP4056 | ✅ Tested |
| LiPo Battery | ✅ Tested |
| JST Connectors | ✅ Tested |
| Frame Design | ✅ Selected |
| Physical Assembly | ⏳ In Progress |
