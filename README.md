# STM32 Weather Station (BME280 + OLED)

A compact weather station based on the **STM32L476RG** microcontroller. The device reads temperature, humidity, and pressure from the BME280 environmental sensor and displays the formatted data in real-time on an OLED screen.

## Features
* Reading environmental data from the Bosch BME280 sensor.
* Displaying results on an OLED display (SSD1306 driver).
* Communication with both modules via the I2C bus.
* **Shared I2C bus:** Both the screen and the sensor are connected to the same microcontroller pins (I2C1), using different hardware addresses.

## Hardware Setup (Pinout)

| Module | STM32 Pin | Function | Notes |
| :--- | :--- | :--- | :--- |
| **I2C (Shared)** | **PB8** | SCL | Clock signal (connected to BME280 and OLED) |
| | **PB9** | SDA | Data line (connected to BME280 and OLED) |
| **Power** | 3.3V | VCC / VIN | Power supply for both modules |
| | GND | GND | Common ground |

## Credits
This project uses excellent open-source libraries. Full copyright belongs to their respective creators:
* **BME280 library for STM32:** [Controllerstech BME280 Library](https://github.com/controllerstech/STM32-HAL/tree/master/BME280/I2C)
* **SSD1306 OLED library for STM32:** [Afiskon SSD1306 Library](https://github.com/afiskon/stm32-ssd1306)

*Huge thanks to the authors for sharing their code!*
