---
title: Building the interface v0.1
date: 2021-02-23 11:30:02 +0100
layout: post
---

It's finally time to build this interface and move to the software part! After messing around with PCF8574 I/O expanders a little bit, I build the arduino -> IDE interface.
I was mostly reffering to Carlos Durandall's ATAPIDUINO scheme, ommiting stuff I didn't understand or think was important.

I tried to redraw and simplify Carlo's schematic, but ended up with even messier one and gave up. I'll do it properly in the next phase, to print PCBs (because this trough-hole stuff was a pain in the ass to do).


IMAGE

I decided it's better to just write what goes where (included at the end of this log).

After hooours of planning, wire stripping and soldering it was done. AND IT WORKS! :D
I used an old ATX power supply to power the board and the CD-drive. I also used DIP IC socket adapters just in case I'd fry one of the I/O chips, and I used Arduino Nano.
Controller board from an old CD-drive

IMAGE

IMAGE

IMAGE

IMAGE

What goes where?

ARDUINO:

Arduino A5 (SCL)    --->    47kOhm resistor (pull-up)    --->    + 5V
Arduino A5 (SCL)    --->    PCF8574 pin 14 (SCL)     (TO EACH PCF!)

Arduino A4 (SDA)    --->    47kOhm resistor (pull-up)    --->    + 5V
Arduino A4 (SDA)    --->    PCF8754 pin 15 (SDA)    (TO EACH PCF!)

Arduino Vin    --->    + 12V
Arduino GND    ---->    GND

Each I/O expander has it's own address to distinguish between them, I'll call them PCF#1, PCF#2 and
PCF#3 (addresses 0x20, 0x21 and 0x21 respectively).

PCF#1:
Address is 0x20

pin 16 (VCC)    --->    +5 V
pin 8 (GND)    --->    GND

pin 1 (A0)    --->    GND
pin 2 (A1)    --->    GND
pin 3 (A2)    --->    GND

pin 13 (INT)    --->    N.C. (not connected anywhere)

pin 4 (P0)    --->    IDE pin 17 (D0 also DD0 or Data0)
pin 5 (P1)    --->    IDE pin 15 (DD1)
pin 6 (P2)    --->    IDE pin 13 (DD2)
pin 7 (P3)    --->    IDE pin 11 (DD3)
pin 9 (P4)    --->    IDE pin 9 (DD4)
pin 10 (P5)    --->    IDE pin 7 (DD5)
pin 11 (P6)    --->    IDE pin 5 (DD6)
pin 12 (P7)    --->    IDE pin 3 (DD7)

PCF#2:
Address is 0x21

pin 16 (VCC)    --->    +5 V
pin 8 (GND)    --->    GND

pin 1 (A0)    --->    GND
pin 2 (A1)    --->    GND
pin 3 (A2)    --->    GND

pin 13 (INT)    --->    N.C. (not connected anywhere)

pin 4 (P0)    --->    IDE pin 4 (DD8)
pin 5 (P1)    --->    IDE pin 6 (DD9)
pin 6 (P2)    --->    IDE pin 8 (DD10)
pin 7 (P3)    --->    IDE pin 10 (DD11)
pin 9 (P4)    --->    IDE pin 12 (DD12)
pin 10 (P5)    --->    IDE pin 14 (DD13)
pin 11 (P6)    --->    IDE pin 16 (DD14)
pin 12 (P7)    --->    IDE pin 18 (DD15)

PCF#3:
Address is 0x22

pin 16 (VCC)    --->    +5 V
pin 8 (GND)    --->    GND

pin 1 (A0)    --->    GND
pin 2 (A1)    --->    GND
pin 3 (A2)    --->    GND

pin 13 (INT)    --->    N.C. (not connected anywhere)

pin 4 (P0)    --->    IDE pin 35 (A0)
pin 5 (P1)    --->    IDE pin 33 (A1)
pin 6 (P2)    --->    IDE pin 36 (A2)
pin 7 (P3)    --->    IDE pin 37 (CS0)
pin 9 (P4)    --->    IDE pin 38 (CS1)
pin 10 (P5)    --->    IDE pin 1 (RST also nRST)
pin 11 (P6)    --->    IDE pin 23 (nDIOW)
pin 12 (P7)    --->    IDE pin 25 (nDIOR)

So now I can play around with CD-drives and give them various commands and see what happens, sweet! Oh and for the arduino code, I used ATAPIDUINO's sketch R1.0. I didn't have physical buttons in my design yet, so I changed the button controls to Serial.read() commands.

Next step I want to do is play around a little, see if the circuit works and if it does - make a proper schematic and print a PCB.