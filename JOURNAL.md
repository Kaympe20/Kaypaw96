---
title: "Kaypaw96"
author: "Kayla Blosser aka @Kayla"
description: "A southpaw 96% keyboard"
created_at: "2024-07-03"
---

### **Total Time Spent: 43hr**

---

## July 4, 2025

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

## July 5, 2025

I got a dark theme to stop searing my eyes and got capacitors for the NeoPixels, as well as having to figure out that 0.1uF is the same as 100nF.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/bc9e8e9d4b430f0bbe956d89ae7ef471cf1f8c21_image.png)

Time Spent: 2hr

---

I found 0805 capacitors of varying capcity on [LCSC](https://lcsc.com/), imported them using [`easyeda2kicad`](https://github.com/uPesy/easyeda2kicad.py). I then assigned each type to its respective item, before realizing that the ESR of 0805 capacitors is too much for the RP2040 and that I would need 0402 alternatives. After going back to get the diodes, I couldn't find footprints so I had to slightly modify the template 0402 footprint.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/962c379ded31283c0a6f65fe54aaf0208e1df729_image.png)

Time Spent: 3.5hr

---

I started designing the PCB and started the grueling wiring of each individual key and light. I want to cry 😢. My fingers and my soul are in pain.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/199011b9da2bc830c324a42149f0a03e34c708a7_image.png)

Time Spent: 2.5hr

---

I finished adding all of the neopixels, all 105 of them 😢.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/0f102d579128bc67d136db932ba23f202447350d_image.png)

Time Spent: 1.5hr

---

## July 6, 2025

I added more capacitors as per the spec of the SK6812-MINI's... 52 of them. I love KiCAD 👍.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/6c4dc1273d6f9d76a6ed650c2f125c67bf88eb20_image.png)

Time Spent: 1.5hr

---

## July 25, 2025

I started wiring everything to do with the microcontrollers and all of its additional parts. It got hectic and chaotic very quickly.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/1e0f04a5d4fcb4cd1c6c4c167b1d69f078d8bccd_image.png)

[@marios](https://github.com/GalaxyGamingBoy) recomended I do a ground pour so I used [my hackpad v2 docs backup](https://hackpad-v2-backup.pages.dev/advancedguide#ground%20pour) to learn how to do one and it started looking much better.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/09153d51440f6414125a32762c351b49b26227b6_image.png)

I then started on the rows and collumns, but was again having difficulty in figuring out how to route them without vias because they ruin signal integrity. Then I realized that the keys are binary and signal integrity/noise shouldn't be nearly enough to get to on from off. With that newfound knowledge, I routed all of them using at least 2 vias each.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/d4223af62206f5d99a0af37c053a55044a9c55f1_image.png)

Here's what the microcontroller section looks like:

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/8789ec09fb7e36c1c7a2b376b1e868c50966dc41_image.png)

Time Spent: 4.5 hr

---

## July 26, 2025

I finished the PCB!!!! 🎊🥳💃🎉📢📣 (almost, tomorrow I'll figure out the hole size I need for gasket mounting)

I did all of the requisite wiring and looked thorugh all of my DRC checkers to see if there was any major issues.

As per [@mra](https://github.com/MichaByte)'s suggestion, I set the ground fill to both sides and put in a bunch of vias to connect all of the unconnected areas (that I had to constantly change to no layers to check where the unconnected areas were).

I now have 0 unconnected areas, except for the sides of my heart, which is now broken after spending so much time on a keyboard that might not work.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/715b3190ecb2dc63c2680e1454ab7009639b5550_image.png)

I also had to add a few more decoupling capacitors as per the spec, which, as always, required a lot of rerouting.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/fbb6ea6decf185ebf913c7b77f0a7d98101782df_image.png)

Time Spent: 3.5hr

---

## July 27, 2025

I finished the mounting holes and added holes for stabalizers. Originally I wanted to forego using screws and wanted to do a gasket mounting setup, but with cost quickly becoming something I have to look out for, I'll leave the mounting holes, and get poron foam to laser cut at my local library should there be room in the budget.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/22c9884f2c6bb00e12e90d567b5b5a02abd7370e_image.png)

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/c07e9161458d1a15d8bfe113bbab5cb01e940622_image.png)

Time Spent: 1hr

---

## July 29, 2025

I added some more mounting holes and altered the size to be much better matched to the actual size of m3 screws.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/1a15580df9dcf5cc04aca85b4971ac32b9d3a9f2_image.png)

I also began CAD and started trying to figure out how to add a plate for my switches.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/33a10dfc5320d5261699ccb3653b07a8fb749d55_image.png)

Time Spent: 1.5hr

---

The holes were intersecting the stabalizers so I changed the position which required redoing half of the work I did.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/739f4c91b62ef06cd610a85bc7ff1dbd35691d43_image.png)

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/d369163766ed07542c1b771d145b08ea510d554c_image.png)

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/f465c7b7e9a7cbbe0b9b26e1a5a38b08aa6d3fdb_image.png)

While I was working on that, I decided to go and switch the measurements to variables to allow me to change them *en mas* later if tolerances don't allow.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/5a10b27e9b45d811591f30ed3a52f0ab01b5b524_image.png)

The grey "𝑓𝑥" indicates they are calculated instead of a set variable.

Time Spent: 2hr

---

## July 30, 2025

I looked at Joe Scotto's How to Design Mechanical Keyboard Plates and Cases [as reccomended by the hackpad guide](https://hackpad.hackclub.com/resources), and got a DXF of my keyboard layout.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/a0f09f938b1bc08be35bbe01c380dfd9efd3ebcb_image.png)

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/3b10ea10024651e0685144ded0c1257a5446c387_image.png)

Here's what extruding that plate gave me:

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/60860960621cc92958883212a19fe0e59e82ba57_image.png)

After that, I went and looked at this Keychron V1 product image and realized that there was the elevated sections where the weren't any surrounding keys.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/a634fd5a1913ac03455aa6761e70d594d9bf5c4e_keychron.webp.png)

So I sketched out all of the areas where the weren't any keys and dimensioned them using dimensions I found on this datasheet on Google Drive.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/928b2a243a3f5e465ddb240a74f1a50319ca09eb_image.png)

Here's what it looks like as a unit.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/bca3440b6990f9fae275319474013471fcafe843_image.png)

Then I added some mounting screw holes with a counterbore so the screw head wouldn't stick out.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/53160d2128d986d0d1edbd549c60317b64868fdf_image.png)


Time Spent: 2.5hr

---

I added each switch (*one by one*) into Onshape so I could have a full render.

First with the function row

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/c8aee10a99065d392f97ba9b3b6aabed2d8b2f49_image.png)

Then with the numpad:

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/0646b4b8e30400f7af2ebad74f839537f4a946cb_image.png)

and then just idk general area

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/09222dcb7967e56d02236c06ad780a6907e041ed_image.png)

Here's the fully setup:

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/aa4b33d606c7016567fc0c7a4ec51e288977665e_image.png)

(The different colors are from pulling the keycap models from different places.)

Time Spent: 2hr

---

I saw this video that told me to use [kbfirmware.com](https://kbfirmware.com/), so I imported my layout into it.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/a1009d172615e52786f6a38a5cb775ce2d84a7a0_image.png)

It did not import correctly at all, wrong number of cols and rows and some stuff isn't routed to the right place. Since you can't do bulk operations, I'll have to do something that's becoming something of a trend on this keyboard and do it one by one.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/070ec6d248b197265694d31ced1f74cf1a2df97e_image.png)

I then moved on to the keymap phase. The [QMK Keycode Docs](https://docs.qmk.fm/keycodes) were super easy to use and quite helpful.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/ef3fa6f341ecf75811b1d7ec73334cffc2f75e5c_image.png)

The task took so time but this work layout made it so much more efficient to work on.

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/f6fcd36f9f5020043613be19c81005587d47d449_image.png)

Time Spent: 1.5hr

---

## July 31, 2025

I went and did some light customization to really make this keyboard my own, including a logo made in MS paint:

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/c4d9b009921697d6353def71946d825573ff2b20_image.png)

![](https://hc-cdn.hel1.your-objectstorage.com/s/v3/048713e762cbde78e4d0c6b09361a31dc0fbfe0c_image.png)

Time Spent: 1hr

---