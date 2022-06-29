<!--
Raspberry Pi Board Pin Layout.md
Copyright (c) 2022 Eric M. Chen

Change History:
2022-06-28/ec:  Initial release.
 -->

# Raspberry Pi Board

Pin #2 is located at the corner of the board. Even number pins are close to the edge of
the board.

***Based on Raspberry Pi 4 Model B.***

## Row 1

|Pin|Desc.  |I2C|SPI<sup>2</sup>|PWM  |
|--:|-------|---|---------------|-----|
|2  |5V
|4  |5V
|6  |GND
|8  |GPIO 14
|10 |GPIO 15
|12 |GPIO 18|   |1 CE0          |PWM0|
|14 |GND
|16 |GPIO 23
|18 |GPIO 24
|20 |GND
|22 |GPIO 25
|24 |GPIO 8 |   |0 CE0          |
|26 |GPIO 7 |   |0 CE1          |
|28 |ID_SC<sup>1</sup>
|30 |GND
|32 |GPIO 12|   |               |PWM 0|
|34 |GND
|36 |GPIO 16|   |1 CE2
|38 |GPIO 20|   |1 MOSI
|40 |GPIO 21|   |1 SCLK

## Row 2

|Pin|Desc.  |I2C|SPI<sup>2</sup>|PWM  |
|--:|-------|---|---------------|-----|
|1  |3V3
|3  |GPIO 2 |SDA
|5  |GPIO 3 |SCL
|7  |GPIO 4
|9  |GND
|11 |GPIO 17|   |1 CE1
|13 |GPIO 27
|15 |GPIO 22
|17 |3V3
|19 |GPIO 10|   |0 MOSI
|21 |GPIO 9 |   |0 MISO
|23 |GPIO 11|   |0 SCLK
|25 |GND
|27 |ID_SD<sup>1</sup>
|29 |GPIO 5
|31 |GPIO 6
|33 |GPIO 13|   |               |PWM 1|
|35 |GPIO 19|   |1 MISO         |PWM 1|
|37 |GPIO 26
|39 |GND

## Note

1. Do not use these pins for anything other than attaching an I2C ID EEPROM.
2. To Enable SPI1, update <code>/boot/config.txt</code>, add
    ```
    dtoverlay=spi1-3cs
    ```

### Reference

Raspberry Pi 4 Model B [datasheets.raspberrypi.com](https://datasheets.raspberrypi.com/rpi4/raspberry-pi-4-datasheet.pdf)
