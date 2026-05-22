# Wiring Plan

## ESP32-C3 → MPU6050

| ESP32-C3 | MPU6050 |
|-----------|-----------|
| 3V3 | VCC |
| GND | GND |
| SDA | SDA |
| SCL | SCL |

## ESP32-C3 → DRV8833

| ESP32-C3 | DRV8833 |
|-----------|-----------|
| PWM Pin 1 | AIN1 |
| PWM Pin 2 | AIN2 |
| PWM Pin 3 | BIN1 |
| PWM Pin 4 | BIN2 |

## Power System

Battery → TP4056

Battery → DRV8833

Battery → ESP32-C3
