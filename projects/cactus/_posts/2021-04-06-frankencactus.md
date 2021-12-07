---
title: "Frankencactus: crappy, cute and blinking without a microcontroller"
layout: post
---

I only had two plants in my room and they both died within a month or so. Maybe, if they involved LEDs, sensors and wires I would think about them more often. What started as a stupid joke, ended up as a cool one-day project: making a cactus with LEDs!

Because I always want to *know* everything, which often results in *doing* nothing, the plan was to hack something together in a single day. To deal with imperfection. To avoid theoretizing. To learn iterative approach to doing things. Thanks to Vita, I didn't fall into the over-enginerring rabbit holes this time :)


## How it's made

We gathered some random stuff from around the house:

- a plastic bowl with a lid
- LED diffuser caps
- piping isolation foam

I've got no idea why I had that isolation foam at home, but it was an okay (and cheap) material for the job. The diffuser caps were salvaged from some old xmas lights I believe.

![workbench](/assets/images/projects/cactus/workbench.jpg){:class="wider"}

First, we made a hole into the rice bowl's lid with a utility knife, shoved the isolation foam inside and somehow shape it into a cactus. We then drilled the holes into the foam, fitting the diffuser caps nicely without gluing them or anything, so they can be replaced.

An 5mm LED diode fits inside the diffuser cap and all of them are connected to an old 5V phone charger. When it came to electronics, I spotted myself dreaming about a custom PCB and connectors and whatnot... I took a deep breath, said "NO", and did the opposite: quickest and dirtiest wiring ever, using a ~~duct~~ tape and massive blobs of solder :D In retrospect, this was the best decision of the project.

![wiring](/assets/images/projects/cactus/crappy_wiring.jpg)

## Where's the magic

It's not rocket science, just a bunch of LEDs in a cactus-shaped foam, right? Well... yes, but it still took a whole afternoon to do it. But that is not why I am writing about it, really.

The best part was switching it on for the first time: half of the LEDs did not work at all, which was not surprising if I think about the wiring efforts. However, some LEDs blinked in random intervals, causing a strange, but kinda pleasant, candle-like flickering effect. It looks even cooler that way, actually.

So, what was the last time you made something blink without a microcontroller, huh? ;)

![finished frankencactus](/assets/images/projects/cactus/flickering.gif)