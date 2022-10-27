---
title: "It started with a fail..."
layout: post
---

Sometime ago I found this old DVD player and a set of speakers, which I used for listening to music, for years. If I turned off my laptop, which was connected to the AUX input of the DVD player, it would make this annoying sound. Can't remember if it was high-pitched squeeching or a low-pitched hum, but anyways I ended up turning off the DVD player everytime as well. But for this, I would have to...STAND UP AND PRESS AN EXTRA BUTTON, so something had to be done about it.

![phillips "micro theater" dvd player, MCD 122](/assets/images/projects/potofmusic/original_player.png)

My knowledge and motivation in audio electronics are not too great, so I decided to do a simple but good-enough hack: wireless control of the power button on the player. So, the first step was clear: open up the case, figure out what is going on, locate the power button, add a wirelessly-controlled-switch somewhere around there.


## Aaand it's gone
I managed to open the case of the DVD player (Phillips MCD 122) and guessed what the three PCBs are for: power-supply, CD/DVD stuff and the "frontend".

![dvd player internals](/assets/images/projects/potofmusic/internals.jpg){:class="wider"}

Since the power button was located on the front panel, I focused on the "frontend" PCB only. It's called the **display board** in the Phillips' [service manual](https://www.manualslib.com/manual/1378595/Philips-Mcd113.html) which contains lots of schematics and was useful in figuring stuff out. Kind of.

There was an IC[^1] connected to all the buttons and the LCD display, with some wires going to other parts of the system (eg. power supply board). I soldered a wire to the input pin where the button was connected and tried applying different voltages to it: GND, 2.7V, 3V and 5V. Nothing seemed to do the job. In fact, after some more desperate poking around, the original buttons stopped working and the whole display didn't turn on anymore. I fried the chip, I guess, whoopsie. 

Well, it was fun anyway. In retrospect, I see that buttons are connected in somekind of a matrix which I've seen before somewhere, it's probably a popular trick for saving GPIO pins and might explain why the button did not behave the way I expected. Anyways, better luck next time.

[^1]: ZX935P; Can't find much about it on the internet. Is it a microcontroller? An LCD driver?