# PlatformIO NXP LPC1769 Arduino Test

## Description 

 Simple project for testing Arduino support on the NXP LPC1769 chip using a custom platform. 

 ## Import and Compile

Clone this repository and use VSCode + PlatformIO extension with the "Open Project" in the PIO Home screen to open the project.

If you're using the CLI, simply clone the project and run `pio run` / `pio run -t upload` inside it. 

## Uploading

The compiled firmware can be found under `.pio\build\nxp_lpc1769\firmware.bin` in the project folder. That firmware can e.g. be flashed using the "Flash Magic" program and with the chip in ISP_BOOT mode. 

If you use PlatformIO for uploading, select the correct `upload_protocol = x` in the `platformio.ini`. By default, an mbed-os disk upload is attempted. Other values are `cmsis-dap` to e.g. use an STLink. All valid values are found in https://github.com/p3p/pio-nxplpc-arduino-lpc176x/blob/master/boards/nxp_lpc1769.json#L35-L41. 

## Expected outcome

Code will attempt to blink an LED that you must connect to pin P0.01 on of the processor. On the SKR 1.4 Turbo board, this pin can be found on the I2C port marked as "0.1" on the backside of the PCB. See https://github.com/bigtreetech/BIGTREETECH-SKR-V1.3/blob/master/BTT%20SKR%20V1.4/Hardware/BTT%20SKR%20V1.4PIN.pdf and https://github.com/bigtreetech/BIGTREETECH-SKR-V1.3/blob/master/BTT%20SKR%20V1.4/Hardware/bot.jpg.

Of course, the code can be arbitrarily changed to a different pin, as listed in https://github.com/p3p/pio-framework-arduino-lpc176x/blob/master/system/lpc176x/pinmapping.h.