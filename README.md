# mcu-board

Some design notes for an MCU board...
Deeply WIP.

## Features

1. STM32 Cortex M4 with FSMC (possibility: STM32F413ZGT6 for 144-LQFP,
   STM32F413VGT3 for 100-LQFP, and STM32F413RGT6 for 64-LQFP)
2. Extra flash and PSRAM
2. WIFI module e.g. [ESP32 C3](https://www.espressif.com/sites/default/files/documentation/esp32-c3-mini-1_datasheet_en.pdf) or [ESP32 S3](https://www.espressif.com/sites/default/files/documentation/esp32-s3-mini-1_mini-1u_datasheet_en.pdf)
3. 4 motor control ports (EV3 compatible)
4. 4 sensor control ports (EV3 compatible)
5. Raspberry Pi pin-out connector (enough to communicate with
   Raspberry pi Zero, does not need full support)
5. SD card (SPI interface enough/SDIO nice to have but requires supported MCU)
6. Accelerometer (could be external)
7. STEMMA QT connector (nice to have)
8. Some informative display (nice to have)
9. A couple of buttons for interface (nice to have also)
10. Lego "compatible" physical shape.

### Notes

- The [WIFI
  module](https://www.digikey.co.uk/en/products/detail/espressif-systems/ESP32-C3-MINI-1-H4/14548892)
  with the SD card on one side and the Raspberry Pi connector may not
  need to be active at the same time.
- The display could be controlled by the WIFI module via [AT
  commands](https://docs.espressif.com/projects/esp-at/en/latest/esp32/Compile_and_Develop/How_to_add_user-defined_AT_commands.html).
  Other things could be moved to the WIFI module too (the interface
  buttons, maybe).
- The board would be a [Raspberry Pi
  hat](https://github.com/raspberrypi/hats) that can work alone. This
  can be a rev 2 objective, but planning for the space would not hurt.
