# Leptosis - Ultra Flat PG1316 Split Keyboard

"Leptos" stands for "flat" in greek, added with the suffix is, it forms the word "Leptosis", signifying the most flat. This represents my long lasting desire for an real flat keyboard that is portable and light. The name is also quite similar to the latin word "levitatio", signifying levitation and thus light.

| Left | Right |
| ---- | ----- |
| ![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/93c19a7e2f73b48492104c29d259a4b94f9fd808_image.png) | ![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/02141a62144210c4f89702bedfaa414e6e2c939f_image.png) |

## What is this?

Leptosis is an ultra flat split bluetooth keyboard. It's thickness will be ~0.5mm, and employs the compact miryoku layout. Using an onboard nrf module, it acheives an ultra long battery life.

## Features
- Ultra long battery life (~4 months for central and 1 year for peripheral)
- Ultra thin (0.5cm)
- Ultra compact (13.2x9.2cm)
- Custom battery management and optimization
- ZMK bluetooth

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/23edbb57a7ef36e5c4a47974ee4243b9c40d1baa_image.png)

## Usage

PCB files are in the `hardware` directory, you need to buy one pcb for the right and the left.

The PCB uses JLCPCB's 1.2mm JLC04121H-7628 stackup. Other stackups would require re-tuning of the USB and antenna feed trace.

The case is in the `CAD` directory. You need to print two of them - one mirrored.

The software is in the `firmware`. Leptosis uses ZMK, allowing ultra long battery life.

