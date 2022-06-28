<!--
ESP32 Development Board Pin Layout.md
Copyright (c) 2022 Eric M. Chen

Change History:
2022-06-28/ec:  Initial release.
 -->

# ESP32-DEVKIT-V1 Board

Microprocessor: ESP-WROOM-32

## Row 1

|Name|Pin    |I2C|SPI      |Touch|ADC<sup>[4]</sup>/DAC|UART|Note|
|----|-------|---|---------|-----|---------------------|----|----|
|EN  |Enable
|VP  |GPIO 36|   |         |     |ADC1 CH0             |    |Input only. Sensor VP
|VN  |GPIO 39|   |         |     |ADC1 CH3             |    |Input only. Sensor VN
|D34 |GPIO 34|   |         |     |ADC1 CH6             |    |Input only
|D35 |GPIO 35|   |         |     |ADC1 CH7             |    |Input only
|D32 |GPIO 32|   |         |9    |ADC1 CH4|
|D33 |GPIO 33|   |         |8    |ADC1 CH5|
|D25 |GPIO 25|   |         |     |ADC2 CH8/DAC1|
|D26 |GPIO 26|   |         |     |ADC2 CH9/DAC2|
|D27 |GPIO 27|   |         |7    |ACD2 CH7|
|D14 |GPIO 14|   |HSPI CLK |6    |ADC2 CH6|
|D12 |GPIO 12|   |HSPI MISO|5    |ADC2 CH5|
|D13 |GPIO 13|   |HSPI MOSI|4    |ADC2 CH4|
|GND |GND
|VIN |VIN    |   |         |     |                     |    |5V to 14V<sup>[5]</sup>

## Row 2

|Name|Pin    |I2C|SPI      |Touch|ADC/DAC |UART                  |Note|
|----|-------|---|---------|-----|--------|----------------------|----|
|D23 |GPIO 23|   |VSPI MOSI|
|D22 |GPIO 22|SCL|
|TX0 |GPIO 1 |   |         |     |        |~~0 TX~~<sup>[3]</sup>
|RX0 |GPIO 3 |   |         |     |        |~~0 RX~~<sup>[3]</sup>
|D21 |GPIO 21|SDA|
|D19 |GPIO 19|   |VSPI MISO|
|D18 |GPIO 18|   |VSPI CLK |
|D5  |GPIO 5 |   |VSPI CS  |
|TX2 |GPIO 17|   |         |     |        |2 TX
|RX2 |GPIO 16|   |         |     |        |2 RX
|D4  |GPIO 4 |   |         |0    |ADC2 CH0|
|D2  |GPIO 2 |   |         |2    |ACD2 CH2|
|D15 |GPIO 15|   |HSPI CS  |3    |ADC2 CH3|
|GND |GND
|3V3 |3V3

3. UART0 is used by the logger component. Projects should use UART2.
4. ADC2 is used by the Wi-Fi driver. Use ADC2 only when Wi-Fi is not needed.
5. Can't find datasheet to confirm the voltage range. Using 5V has no problem.

## Note

- Except for using the designated pins, software implementation is also available for
    various functions. See related documentation for detail.
- PWM on all I/O pins.
- On board LED is on GPIO 2.

### Reference

- [lastminuteengineers.com](https://lastminuteengineers.com/esp32-pinout-reference/)
