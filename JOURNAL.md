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
