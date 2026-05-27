# Final Drone Wiring Connections

This document contains the final wiring layout for the fully assembled GestureFly drone.

The drone uses:
- ESP32-C3 as the flight controller
- MPU6050 for stabilization
- 2× DRV8833 motor drivers
- 4× 720 coreless motors
- 4× 55mm propellers
- 1S LiPo battery power system

# System Architecture

MPU6050
    ↓
ESP32-C3
    ↓
DRV8833 Drivers
    ↓
720 Motors


# ESP32 C3 Connections 

| ESP32-C3 Pin | Connected Component | Purpose |
|---|---|---|
| GPIO2 | DRV8833 #1 IN1 | Motor Control |
| GPIO3 | DRV8833 #1 IN2 | Motor Control |
| GPIO6 | DRV8833 #1 IN3 | Motor Control |
| GPIO7 | DRV8833 #1 IN4 | Motor Control |
| GPIO8 | DRV8833 #2 IN1 | Motor Control |
| GPIO9 | DRV8833 #2 IN2 | Motor Control |
| GPIO10 | DRV8833 #2 IN3 | Motor Control |
| GPIO20 | DRV8833 #2 IN4 | Motor Control |
| GPIO4 | MPU6050 SDA | I2C Data |
| GPIO5 | MPU6050 SCL | I2C Clock |
| 3V3 | MPU6050 VCC | Sensor Power |
| GND | Common Ground | Shared Ground |

---

# MPU6050 Connections

| MPU6050 Pin | ESP32-C3 Connection |
|---|---|
| VCC | 3V3 |
| GND | GND |
| SDA | GPIO4 |
| SCL | GPIO5 |
| XDA | Not Connected |
| XCL | Not Connected |
| AD0 | Not Connected |
| INT | Optional Future Use |

---

# DRV8833 #1 Connections

## Logic Connections

| DRV8833 Pin | Connection |
|---|---|
| VCC | ESP32 3V3 |
| GND | Common Ground |
| EEP | 3V3 |
| IN1 | GPIO2 |
| IN2 | GPIO3 |
| IN3 | GPIO6 |
| IN4 | GPIO7 |

---

## Motor Connections

| DRV8833 Output | Motor |
|---|---|
| OUT1 + OUT2 | Front Left Motor |
| OUT3 + OUT4 | Front Right Motor |

---

## Power Connections

| DRV8833 Pin | Connection |
|---|---|
| VLT | LiPo Positive |
| GND | LiPo Negative |

---

# DRV8833 #2 Connections

## Logic Connections

| DRV8833 Pin | Connection |
|---|---|
| VCC | ESP32 3V3 |
| GND | Common Ground |
| EEP | 3V3 |
| IN1 | GPIO8 |
| IN2 | GPIO9 |
| IN3 | GPIO10 |
| IN4 | GPIO20 |

---

## Motor Connections

| DRV8833 Output | Motor |
|---|---|
| OUT1 + OUT2 | Rear Left Motor |
| OUT3 + OUT4 | Rear Right Motor |

---

## Power Connections

| DRV8833 Pin | Connection |
|---|---|
| VLT | LiPo Positive |
| GND | LiPo Negative |

---

# LiPo Battery Connections

| Battery Wire | Connection |
|---|---|
| Positive (+) | DRV8833 VLT |
| Negative (-) | Common Ground |

---


# TP4056 Charging Connections

| TP4056 Pin | Connection |
|---|---|
| B+ | LiPo Positive |
| B- | LiPo Negative |

The following components MUST share a common ground:

- ESP32-C3
- MPU6050
- DRV8833 #1
- DRV8833 #2
- LiPo Battery
- TP4056

 Power Distribution

## 3.3V Rail Powers

- ESP32-C3 logic
- MPU6050
- DRV8833 logic side
- DRV8833 enable pins

---

## LiPo Battery Powers

- DRV8833 motor power stage
- brushed motors

---


The MPU6050 should:
- remain flat
- remain centered
- be mounted securely

This is critical for stabilization.


The following connections should be able to perform the hover tests without any errors.

Note- The connections for future gesture-based flight control are still under development.
