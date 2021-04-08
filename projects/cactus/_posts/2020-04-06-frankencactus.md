---
title: "Frankenkaktus: crappy, cute and blinking without a microcontroller"
layout: post
excerpt_separator: <!--more-->
---

I only had two plants in my room and they both died within a month or so. Maybe, if they involved LEDs, sensors and wires I would think about them more often. What started as a stupid joke, ended up as a cool one-day project: making a cactus with LEDs!

Because I always want to *know* everything, which often results in *doing* nothing, the plan was to hack something together in a single day. To deal with imperfection and avoiding theory. Thanks to Vita, I didn't fall into the over-enginerring rabbit holes this time :)


## How it's made

We gathered some random stuff from around the house:

- a plastic bowl with a lid
- LED diffuser caps
- piping isolation foam

I've got no idea why I had that isolation foam at home, but it was an okay (and cheap) material for the job. The diffuser caps were salvaged from some old xmas lights I believe.

<!-- <div class="wider side-by-side">
<img src={{ "/assets/images/profile_photo.jpg" | relative_url }} alt="profile_photo"/>
<img src={{ "/assets/images/projects/cactus/diffuser_caps.jpg" | relative_url }} alt="LED diffuser caps" title="LED diffuser caps"/>
<img src={{ "/assets/images/projects/cactus/foam_in_a_bowl.png"  | relative_url }} alt="Piping isolation foam stuck in a plastic bowl" title="Piping isolation foam stuck in a plastic bowl"/>
</div> -->
{% capture img1 %}
{{ "/assets/images/projects/cactus/diffuser_caps.jpg" | relative_url }}
{% endcapture %}
{% capture img2 %}
{{ "/assets/images/projects/cactus/foam_in_a_bowl.png" | relative_url }}
{% endcapture %}
{% include sidebyside.html src1=img1 src2=img2 %}

IMAGE OF WORKING PROCESS

First, we made a hole into the rice bowl's lid with a utility knife, shoved the isolation foam inside and somehow shape it into a cactus. We then drilled the holes into the foam, fitting the diffuser caps nicely without gluing them or anything, so they can be replaced.

An 5mm LED diode fits inside the diffuser cap and all of them (<20) are connected to an old 5V phone charger (in parallel, with XXX resistors). However, when it came to electronics I spotted myself dreaming about custom PCB and connectors and whatnot. I took a deep breath, said "NO", and did the opposite: quickest and dirtiest wiring ever, using a duct tape and massive blobs of solder :D In retrospect, this decision was the best part the project.



## Where's the magic

It's not rocket science, just a bunch of LEDs in a cactus-shaped foam, right? Well... yes, but it still took a whole afternoon to do it. But that is not why I am writing about it, really.

The best part was switching it on for the first time: half of the LEDs did not work at all, which was not surprising if I think about the wiring efforts. However, some LEDs blinked in more-or-less regular intervals, causing a very pleasant, candle-like flickering effect. It looks even cooler that way, actually.

So, what was the last time you made something blink without a microcontroller, huh? ;)

<!--more-->