# Leptosis - Ultra Flat PG1316 Split Keyboard

![](assets/front.jpg)

"Leptos" stands for "flat" in greek, added with the suffix is, it forms the word "Leptosis", signifying the most flat. This represents my long lasting desire for an real flat keyboard that is portable and light. The name is also quite similar to the latin word "levitatio", signifying levitation and thus light. (I'm bad at naming things lol)

## What is this?

Leptosis is an ultra flat split bluetooth keyboard. It's thickness will be ~7.5mm, and employs the compact miryoku layout. Using an onboard nrf module, it achieves an ultra long battery life.

| Left | Right |
| ---- | ----- |
| ![](assets/left.png) | ![](assets/right.png) |

## Features
- Ultra long battery life (~4 months for central and 1 year for peripheral)
- Ultra thin (7.5mm)
- Compact (13.2x9.2cm)
- Custom battery management and optimization
- Embedded nrf52 mcu
- ZMK bluetooth

![](assets/hand-scale.jpg)

## Fabrication

You can either use PCBA to fabricate the PCB, or reflow it yourself. I highly discurrage you to reflow the yourself if you haven't reflowed a aQFN package before - it's a nightmare to get right.

The PCB files are in the `hardware` directory, you need to buy one pcb for the right and the left. There is also a V-Cut panneled version in `hardware/panel`. It uses JLCPCB's 1.2mm JLC04121H-7628 stackup. Other stackups would require re-tuning of the USB data lines and antenna feed trace.

The case is in the `CAD` directory. Print out all `.step` files.

The software is in the `firmware`. Leptosis uses ZMK, allowing ultra long battery life.

After fabrication, solder on some jumpers onto the 4 test pads, and connect it to a JTAG connector (I'm using the ST-LINK). Download the bootloader from the newest action [here](https://github.com/cheyao/Adafruit_nRF52_Bootloader/actions) and unzip it.

For stlink, install openocd and run the following commands:

```zsh
openocd -f /usr/share/openocd/scripts/interface/stlink.cfg -f /usr/share/openocd/scripts/target/nrf52.cfg -c 'program <path_to_bootloader>.hex verify reset; shutdown;'
```

For other JTAG connectors, please refer to your own documentation.

Now plug in a USB-C cable, and you should see a mass storage device called `LEPTOSIS`.

Download the ZMK config from this repo: https://github.com/cheyao/zmk-config/actions, drag the utf file to the mass storage device and you are done!

## Misc

Liked this project? Drop a star and check out my [other Icepi Zero project](https://www.crowdsupply.com/icy-electronics/icepi-zero/)!

