# ESP32-C3 Testing

## Overview


- low cost
- compact size
- built-in WiFi + Bluetooth
- ESP-NOW support
- lightweight form factor

## Arduino IDE Configuration

| Setting | Value |
|---|---|
| Board | ESP32C3 Dev Module |
| Upload Speed | 921600 |
| Flash Frequency | 80MHz |
| Flash Mode | QIO |
| Partition Scheme | Default 4MB with SPIFFS |
| Port | COM6 (varies by system) |


# Testing Procedure

1. Install ESP32 board package in Arduino IDE.
2. Connect ESP32-C3 using USB-C cable.
3. Verify COM port detection.
4. Upload basic serial communication test code.
5. Verify successful firmware upload.
6. Open Serial Monitor at `115200 baud`.
7. Confirm stable serial output.
8. Verify GPIO outputs using DRV8833 motor driver tests.
9. Verify I2C communication with MPU6050.




# Basic Test Code

```cpp
void setup() {

  Serial.begin(115200);

  delay(1000);

  Serial.println("ESP32-C3 Running");
}

void loop() {

  Serial.println("Running");

  delay(1000);
}
```

---

#  Serial Monitor Output

ESP32-C3 Running
Running
Running
Running


# Issues Encountered

| Problem | Solution |
|---|---|
| Serial monitor blank | Correct baud rate |
| Upload failures | Verified correct COM port |
| MPU6050 not detected | Fix GPIO wiring |
| Incorrect GPIO connection | GPIO5 was accidentally connected to GPIO6 |


# Future Plans

The ESP32-C3 will later be responsible for:

- drone stabilization
- wireless ESP-NOW communication
- gesture control processing
- motor control logic
- telemetry logging
- future black-box flight logging system

here is an Image of the esp32 C3 super mini:

<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/bf0f24ca-78ea-4c10-be64-7e91dd3e9aa5" />

