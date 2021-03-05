---
layout: post
title: A dive into the CD-drive!
date: 2021-02-23 14:30:02 +0100
excerpt_separator: <!--more-->
---

I started with exploring my CD - drive. How does it work, how do I control it and what does it output? The "how does it work" part you can find easily, if you know how to open google and search for it. I won't go into this here.

Next step for me was reading all there is to read on the housing of my CD-drive. I was happy to see that the model I have, is so well labeled- all the connectors on the back are labeled with words. I don't see such effort in newer devices so often.

## POWER SUPPLY

Powering the drive is quite straight-forward (thanks to all the labels and stickers). In my case it says: "POWER SUPPLY DC 5V 1.5A / 12V 1.5A" .

Now, for the connector (labelled "DC INPUT") couldn't find a better answer than: MOLEX. As you might see "Molex" isn't one specific model of connector, but tons of them- crap! According to their webpage, the keyword that takes you one step closer to your CD- (and hard-, and floppy-) drive is "8981-series". That's good enough for me, for now. You can scavenge some of them from your old computer's (ATX) power supply!

Thing about the power supply that bothered me was: do I need both 12V and 5V supplies? Shouldn't only one be enough? After some reading on forums, I found out that you DO need both. One for the motors and "heavy weight stuff", other for the control circuit, chips and stuff. Having two separate power supplies looks a bit gipsy-ish solution, so I will try to find more elegant solution later. Any Electrical Engineers with an advice here? :)


## AUDIO CONNECTOR

I noticed that there already is an audio output connector (link). And some of my CD - drives even have two of them, digital and analog one. This means I could hook an amplifier directly to the drive, without having to deal with digital to analog conversion (the part which I'm "afraid" the most - have the least knowledge) -yay! :D


<!--more-->

## SLAVES AND MASTERS CONNECTOR

There is a connector that enables you to switch the CD drive between submissive-mode and master-dominating-your-life-mode...or something?
It's actually a connector for setting "Master" or "Slave" mode of the device (computers IDE controller needs to know this). Afaik it's there for historical reasons and since I only have one device, "Master" mode should work fine.


## IDE INTERFACE

Now the big connector...and the big knowledge gap for me. The IDE interface connector. You know you're entering the messy world of standards and protocols when googling "IDE interface" first takes you to "Parallel ATA" wiki. What? And it is a loooong page, full of history.

Before diving into it: IDE interface connector is used for connecting the drive with the computer's motherboard. It's an interface, for sure. And at the moment I only know that sending the right signals to the right pins (from Arduino, for example), will control my CD-drive. Yay! Also, IDE controller is an interesting keyword.

But what "language" does it speak? What bits do I need to send to which pins to open the cd-tray for example, or to skip a song? I guess I'll have to find info about some protocols...
