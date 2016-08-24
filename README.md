# WIFI-IOT-CORE for IoT production project

_Wifi IoT Core_ project is to combine STM32 + ESP8266.

- ESP8266 is an amazing but cheap wifi chip. However it has many limitions, such as: no USB, limited analog interface, few I/O etc, while applications which are developed on it often need USB-Serial communication. Therefore many ESP8266-based modules in the world are added USB-TTL chip. While this brings some value to developing work, the value is just little in practical use. The design in this _Wifi IoT Core_ project uses the cheap STM32, with USB interface, to ease development, and complements many other features which are missing in ESP8266.

- The _Wifi IoT Core_ project including:

    + [wifi-iot-core-hw](https://github.com/genuine-engineering/wifi-iot-core-hw). Hardware is designed with [KiCad](http://kicad-pcb.org/)
    + [wifi-iot-core-stm32-fw](https://github.com/genuine-engineering/wifi-iot-core-stm32-fw). Firmware for STM32, based on [libopencm3](https://github.com/libopencm3/libopencm3)
    + [wifi-iot-core-esp8266-fw](https://github.com/genuine-engineering/wifi-iot-core-esp8266-fw). Firmware for ESP8266, based on [Espressif SDK 2.0](https://espressif.com/en/support/download/sdks-demos)

# Wifi-iot-core-hw
## Overview
The hardware is designed with [KiCad](http://kicad-pcb.org/) software. It includes two main components: ESP8266 and STM32F103C8T6.

 - STM32 has USB interface and is connected with ESP8266 via UART.

 - The output pins of the STM32 and ESP8266 are exposed for external use.

## Schematic

[![Wifi IOT Core HW Schematic](assets/wifi-iot-core-hw-sch.png)](assets/wifi-iot-core-hw-sch.svg)

## PCB

[![Wifi IOT Core HW PCB](assets/wifi-iot-core-hw-pcb.png)](assets/wifi-iot-core-hw-pcb.svg)

## 3D

[![Wifi IOT Core HW 3D](assets/wifi-iot-core-hw-3d.png)](assets/wifi-iot-core-3d.wrl.stl)

## BOM

| Refs                      | Value           | Footprint                            |
|---------------------------|-----------------|--------------------------------------|
| C7                        | 15pf            | lib:C_0603                           |
| C1,C9-C12,C15,C17,C19,C20 | 0.1uF           | lib:C_0603                           |
| C4,C5                     | 10pF            | lib:C_0603                           |
| C6                        | 15pF            | lib:C_0603                           |
| C16,C18                   | 1uF             | lib:C_0603                           |
| C3                        | 100nF           | lib:C_0603                           |
| C21                       | 10nF            | lib:C_0603                           |
| C2,C13,C14                | 10uF-50v        | Capacitors_SMD:C_1210                |
| C8                        | 470pF           | lib:C_0603                           |
| R11,R12                   | 22              | lib:R_0603                           |
| R10                       | 1.5K            | lib:R_0603                           |
| R2-R5                     | 10K             | lib:R_0603                           |
| R9                        | 0R              | lib:R_0603                           |
| R1,R6-R8,R13              | 10k             | lib:R_0603                           |
| SW1                       | RST             | lib:SW_SPST_B3U-1000P-B              |
| SW2                       | SW_PUSH_SMALL_H | lib:SW_SPST_B3U-1000P-B              |
| U1                        | ESP-07v2        | lib:ESP-07v2-smd-16pin               |
| U2                        | STM32F103C8Tx   | lib:LQFP-48_Pin1.7x0.3mm_Pitch0.5mm  |
| U3                        | LP2985LV        | TO_SOT_Packages_SMD:SOT-23-5         |
| P1,P2                     | CONN_01X20      | Pin_Headers:Pin_Header_Straight_1x20 |
| P7                        | CONN_01X04      | Pin_Headers:Pin_Header_Straight_1x04 |
| P3-P6                     | CONN_01X01      | lib:MountingHole_2mm                 |
| P8                        | USB             | lib:Micro_usb_B_smd                  |
| Y2                        | 32.687          | lib:crystal_smd_32.768_2Pin          |
| Y1                        | 8MHz            | lib:Crystal_SMD_5032_4Pads           |
| D2                        | Led             | LEDs:LED_0805                        |
| D1                        | Led GPIO16      | LEDs:LED_0805                        |

## Gerber file

[Wifi IOT Core HW Gerber file](assets/gerber.zip)

## CC-BY license

[![CC-BY](http://mirrors.creativecommons.org/presskit/buttons/88x31/png/by.png)](https://github.com/idleberg/Creative-Commons-Markdown/blob/spaces/4.0/by.markdown)
