# OpenLTTO
The OpenLTTO Project is an attempt to recreate the Lazer Tag Team Ops protocol, and game system, in a completely open-source solution. Eventually our intent, is to expand on the LTTO system, adding new functionality, and features, while maintaining backwards compatibility with this classic Lazer Tag gear.

> This Project wouldn't be possible without all the hard work of Richie Mickan https://github.com/rmick
> His work on recreating the LTTO Protocol, and the development of the Combobulator app are core to the firmware and capabilities of this project.

> Additionally this is built on top of the excellent product developed and released by Hasbro/Tiger Electronics. And the work done by Tag Ferret to release the technical specs, and unlock much of the magic of the protocol, and the inner workings.

We intend to do this via a collection of open-source hardware components that can act as building blocks, to build anything you might require for a Lazer Tag game (Taggers, Hosting Pods, Zone controllers, utilities, etc). And an opensource firmware to operate it all. 

Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

# OpenLTTO Motherboard
The OpenLTTO Motherboard is a simple circuit, which mainly breaks out connectors from an M5Stack CoreS3, which is a packaged microcontroller containing an ESP32-S3 chip. This microcontroller offers a suite of great features making it an ideal centerpiece for the OpenLTTO ecosystem. It is inexpensive, and provides a nice commercial product, with a display, touchscreen, motion sensors, sound output, an SD Card slot, and plenty of internal flash and RAM, along with a powerful dual core 240Mhz processor.

## Hardware Interfaces
The OpenLTTO Motherboard has multiple hardware interfaces that can be used in many ways to construct Lazer Tag gear

### IR Ports
The OpenLTTO Motherboard has 4x IR Ports, which allow interfacing any of our IR Modules. Each port can be individually addressed with independent IR Transmit and Receive functions in order to sense where incoming tags come from, and control where IR packets are sent. Modules can also be daisy chained together on a single port, which makes them function in unison at a single address (all modules include an "IN" and an "OUT" port to allow chaining)

### Switch Ports
The Switch ports allow interfacing buttons or switches to the motherboard, such as user interaction buttons, or trigger/reload switches, etc. These can then be mapped in the configuration screen to various functions.

### RGB Port
The RGB Port is a common pinout for interfacing WS2812 or similar RGB LED chains (often called NeoPixels). These can be chained together, and controlled from the firmware for a number of functions and lighting effects.

### I2C Expansion Port
The I2C Port is reserved for future expansion, it uses the common "Grove" pinout and connector (JST PH 2.0). This will allow adding any other I2C based peripherals in the future.

### Battery Connection
The Battery Connection supports any single parallel cell 3.7V Lithium Polymer, or Lithium Ion batteries (for example you can have a single cell, or you can hook up multiple cells in parallel, but never in series). The M5Stack CoreS3 has a USBC port and can manage battery levels, and charge the battery via USBC.

## OpenLTTO Motherboard Top Side (interface to M5Stack CoreS3)
![Image of OpenLTTO Motherboard Top](![image](https://github.com/OpenLTTO/OpenLTTO-Motherboard/blob/main/OpenLTTO%20Motherboard%20Top.png?raw=true)

## OpenLTTO Motherboard Bottom Side
![Image of OpenLTTO Motherboard Bottom](https://github.com/OpenLTTO/OpenLTTO-Motherboard/blob/main/OpenLTTO%20Motherboard%20Bottom.png?raw=true)
