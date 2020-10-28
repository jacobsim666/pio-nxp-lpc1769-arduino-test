# PlatformIO NXP LPC1769 Arduino Test

## Description 

 Simple project for testing Arduino support on the NXP LPC1769 chip using a custom platform. 

 ## Import and Compile

Clone this repository and use VSCode + PlatformIO extension with the "Open Project" in the PIO Home screen to open the project.

If you're using the CLI, simply clone the project and run `pio run` / `pio run -t upload` inside it. 

## Uploading

The compiled firmware can be found under `.pio\build\nxp_lpc1769\firmware.bin` in the project folder. That firmware can e.g. be flashed using the "Flash Magic" program and with the chip in ISP_BOOT mode. 

If you use PlatformIO for uploading, select the correct `upload_protocol = x` in the `platformio.ini`. By default, an mbed-os disk upload is attempted. Other values are `cmsis-dap` to e.g. use an STLink. All valid values are found in https://github.com/p3p/pio-nxplpc-arduino-lpc176x/blob/master/boards/nxp_lpc1769.json#L35-L41. 