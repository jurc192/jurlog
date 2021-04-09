---
title: "Das-mas cactus"
layout: post
excerpt_separator: <!--more-->
---

How to make a better version of the cactus? Honestly, I'm afraid to even touch the first one: it flips over easily, diffuser caps fall out sometimes and half of the lights don't work anyways. Improving on this shouldn't be too hard.

## Sculpting

This time we used a **modeling clay** and went for a fancier shape of the cactus. We tried planning things, but the "just do it and pray" method took over: we've connected two plastic bottles together using random stuff (cardboard, piping foam leftovers, lots of tape) and covered them with the modeling clay.

{% capture img1 %}
{{ "/assets/images/projects/cactus/plastic_base.jpg" | relative_url }}
{% endcapture %}
{% capture img2 %}
{{ "/assets/images/projects/cactus/clay_base.jpg" | relative_url }}
{% endcapture %}
{% include sidebyside.html src1=img1 src2=img2 class="taller" %}


It looked pretty well and robust enough, but there was an issue: how to get the bottles out? Oh, by the way, the bottle was previously used for a home-made schnaps, so the whole thing smelled like booze. A lot.

We detached the "arm" of the cactus by somehow cutting it off and pulled the main bottle out. Same thing for the smaller bottle and the joint between the two. Somehow. Not without damage though, but nothing that couldn't be fixed with more clay :)

![pulling out the bottle](/assets/images/projects/cactus/bottle_pull_out.jpg){: class="wider"}

In order to make it more robust, we used an actual **flower pot** and hacked together a cardboard mount for the cactus.  

Drilling a hole into the pot was a real pain in the ass, but we wanted to mount a switch properly. It took a loong time and a drill-bit was getting really hot, but in the end it worked out and it looks pretty cool. 

{% capture img1 %}
{{ "/assets/images/projects/cactus/pot_cardboard1.jpg" | relative_url }}
{% endcapture %}
{% capture img2 %}
{{ "/assets/images/projects/cactus/pot_cardboard2.jpg" | relative_url }}
{% endcapture %}
{% include sidebyside.html src1=img1 src2=img2 %}
{% capture img1 %}
{{ "/assets/images/projects/cactus/switch_hole.jpg" | relative_url }}
{% endcapture %}
{% capture img2 %}
{{ "/assets/images/projects/cactus/switch_mounted.jpg" | relative_url }}
{% endcapture %}
{% include sidebyside.html src1=img1 src2=img2 %}

## Electronics

NO DUCT TAPE THIS TIME!!! The previous cactus was powered by an USB charger which "worked" but didn't look nice and the cable was too short. All of its wires were "protected" by a regular tape, some of the LEDs were connected in series and half of them didn't work. 

This time I've put some more love into the wiring:

- using a perfboard (all connections + resistors)
- using a proper power supply [^1]
- using a on/off switch
- using heat-shrink tubes [^2]

<br>

{% capture img1 %}
{{ "/assets/images/projects/cactus/board_1.jpg" | relative_url }}
{% endcapture %}
{% capture img2 %}
{{ "/assets/images/projects/cactus/board_2.jpg" | relative_url }}
{% endcapture %}
{% include sidebyside.html src1=img1 src2=img2 %}
{% capture img1 %}
{{ "/assets/images/projects/cactus/power_supply1.jpg" | relative_url }}
{% endcapture %}
{% capture img2 %}
{{ "/assets/images/projects/cactus/power_supply2.jpg" | relative_url }}
{% endcapture %}
{% include sidebyside.html src1=img1 src2=img2 %}

Wiring and soldering everything together took about 6 hours. The most annoying and time-consuming task was getting the wires through the cactus (small hole IN, bottom opening OUT). Is there a smart way to do this? Anyways, **all of the LEDs work**! No accidental blinking!

[^1]: 220V, X A. Opened it just enough to reach the power rails, otherwise left untouched and inside enclosure.
[^2]: 22 awg, stranded silicone wire



## Das-mas cactus

That was it, it turned out pretty well I think. Look at the photos :)

