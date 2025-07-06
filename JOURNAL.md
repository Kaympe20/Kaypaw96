---
title: "Kaypaw96"
author: "Kayla Blosser aka @Kayla"
description: "A southpaw 96% keyboard"
created_at: "2024-07-03"
---
I setup the layout using [keyboard-layout-editor](https://keyboard-layout-editor.com/)

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/ee1725c6bd7e4fd20f30cdcb9966434611b743f4_image.png)

Time Spent: 1hr

---

I created the basic layout of the keyswitches in the schematic after learning how matrixes work

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/18f0e79148acda34cb0deea40d169ac21999fda4_image.png)

... only to realize I need diodes.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/7b2b6222051b8629493235d64f7ba329b0ca0616_image.png)

Time Spent: 2hr

---

I wired up the matrix with labels

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/a3a0ca186cb5de0d7edd43af8fb941454b406b0a_image.png)

Time Spent: 1.5hr

---

The pico didn't have enough pins so I've begun work directly using the RP2040 using the [RP2040 hardware design datasheet](https://datasheets.raspberrypi.com/rp2040/hardware-design-with-rp2040.pdf).

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/5e6719d96c81a1639f9b2c05f53cf33184b02999_image.png)

Time Spent 3hr

---

I finished up the setup for the RP2040 including power delivery, USB communications, and 

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/628352ad440f64f340b11410bc5efb963d06fffd_image.png)


Time Spent: 3.5 hr

---

I research JLC PCBA Extended and added all of the neopixels on a single pin that will draw 1.3A.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/af1464ef197b6ba9b5433839f6e94bf1095fa65c_image.png)

Time Spent: 1.5hr

---

I got a dark theme to stop searing my eyes and got capacitors for the NeoPixels, as well as having to figure out that 0.1uF is the same as 100nF.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/bc9e8e9d4b430f0bbe956d89ae7ef471cf1f8c21_image.png)

Time Spent: 2hr

---

I found 0805 capacitors of varying capcity on [LCSC](https://lcsc.com/), imported them using [`easyeda2kicad`](https://github.com/uPesy/easyeda2kicad.py). I then assigned each type to its respective item, before realizing that the ESR of 0805 capacitors is too much for the RP2040 and that I would need 0402 alternatives. After going back to get the diodes, I couldn't find footprints so I had to slightly modify the template 0402 footprint.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/962c379ded31283c0a6f65fe54aaf0208e1df729_image.png)

Time Spent: 3.5hr

---

I started designing the PCB and started the grueling wiring of each individual key and light. I want to cry <img src="https://emoji.slack-edge.com/T0266FRGM/hdheavysob/3c96038a66442dc6.png" width=20>. My fingers and my soul are in pain.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/199011b9da2bc830c324a42149f0a03e34c708a7_image.png)

Time Spent: 2.5hr

---

I finished adding all of the neopixels, all 105 of them <img src="https://emoji.slack-edge.com/T0266FRGM/hdheavysob/3c96038a66442dc6.png" width=20>.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/0f102d579128bc67d136db932ba23f202447350d_image.png)

Time Spent: 1.5hr

---

I added more capacitors as per the spec of the SK6812-MINI's... 52 of them. I love KiCAD.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/6c4dc1273d6f9d76a6ed650c2f125c67bf88eb20_image.png)

Time Spent: 1.5hr

---