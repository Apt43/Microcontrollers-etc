<!--
libcamera for Raspberry Pi.md

Copyright (c) 2022 Eric M. Chen

Change History:
2022-07-17/ec:  Initial release.
 -->

# libcamera for Raspberry Pi

Quote from [Raspberry Pi Documentation](https://www.raspberrypi.com/documentation/accessories/camera.html)

> Raspberry Pi is transitioning from a legacy camera software stack based on proprietary Broadcom GPU code to an open-source stack based on libcamera. Raspberry Pi OS images from Bullseye onwards will contain only the libcamera-based stack. Raspberry Pi OS images up to and including Buster will contain the legacy Raspicam stack, though the libcamera stack and applications can be installed using apt, or built by following the normal build instructions.

## IMX519 Autofocus Camera

[Arducam 16MP Autofocus camera](https://www.amazon.com/Arducam-Autofocus-Raspberry-Megapixel-Resolution/dp/B09STL7S88/ref=sr_1_2?m=A2IAB2RW3LLT8D&marketplaceID=ATVPDKIKX0DER&qid=1658079827&refinements=p_4%3AArducam&s=merchant-items&sr=1-2) needs *libcamera* to capture images and videos.

See [IMX519 Autofocus Camera and Raspberry Pi libcamera Guide](https://www.arducam.com/docs/cameras-for-raspberry-pi/raspberry-pi-libcamera-guide/) for more information.
