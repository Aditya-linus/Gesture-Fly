# MPU6050 Testing

## Overview


# Wiring Connections

## ESP32-C3 → MPU6050

| ESP32-C3 Pin | MPU6050 Pin |
|---|---|
| 3V3 | VCC |
| GND | GND |
| GPIO4 | SDA |
| GPIO5 | SCL |


# Testing Procedure

2. Connected the MPU6050 to the ESP32-C3 using jumper wires.
3. Verify voltage across VCC and GND.
4. Upload an I2C scanner sketch to detect the MPU6050.
5. Confirm MPU6050 address at `0x68`.
6. Uploaded raw MPU6050 reading test code.
7. Verifyd live accelerometer values through the Serial Monitor.
8. Tilt the sensor physically to confirm changing sensor values.


<img width="1600" height="720" alt="image" src="https://github.com/user-attachments/assets/ce88113d-54fa-43b1-bfe5-800c416d2692" />


# I2C Scanner Code

```cpp
#include <Wire.h>

void setup() {

  Wire.begin(4, 5);

  Serial.begin(115200);

  while (!Serial);

  Serial.println("\nI2C Scanner");
}

void loop() {

  byte error, address;
  int devices = 0;

  Serial.println("Scanning...");

  for(address = 1; address < 127; address++) {

    Wire.beginTransmission(address);

    error = Wire.endTransmission();

    if(error == 0) {

      Serial.print("Found device at 0x");

      if(address < 16)
        Serial.print("0");

      Serial.println(address, HEX);

      devices++;
    }
  }

  if(devices == 0)
    Serial.println("No I2C devices found");

  delay(3000);
}
```



Serial monitor output 

Scanning...
Found device at 0x68




# MPU6050 Test Code

```cpp
#include <Wire.h>

const int MPU = 0x68;

void setup() {

  Serial.begin(115200);

  Wire.begin(4, 5);

  delay(1000);

  Serial.println("Starting MPU6050...");

  Wire.beginTransmission(MPU);
  Wire.write(0x6B);
  Wire.write(0x00);

  Wire.endTransmission(true);

  delay(100);

  Serial.println("MPU6050 READY");
}

void loop() {

  Wire.beginTransmission(MPU);
  Wire.write(0x3B);

  Wire.endTransmission(false);

  Wire.requestFrom(MPU, 6, true);

  if(Wire.available() == 6) {

    int16_t AcX =
      Wire.read() << 8 | Wire.read();

    int16_t AcY =
      Wire.read() << 8 | Wire.read();

    int16_t AcZ =
      Wire.read() << 8 | Wire.read();

    Serial.print("X: ");
    Serial.print(AcX);

    Serial.print(" | Y: ");
    Serial.print(AcY);

    Serial.print(" | Z: ");
    Serial.println(AcZ);
  }

  delay(500);
}
```

This will plot the axis readings in the serial monitor and confirr the working of the gyroscope.

