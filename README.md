# GRBLcd
LCD support for GRBL

GRBL is a great program for an ATmega328 to control your CNC, 3D Printer, Lasercutter or similar. But as it's very complex, it's memory hungry too. So there is each byte calculated to fit to the tiny device, almost nothing left. And if there would be place left, there would be no pin to use. But what if you want to not to have your pc with you at the machine? Or simply want a fast overview, what's currently going on?
GRBLcd, inspired by Xlcd, is here to help you. Perfectly for headless systems, no need for an external computer, featuring G-Code read from SD-Cards.
The code runs much smoother than Xlcd. I already forked Xlcd to add some code improvements, but most development would be incompatible with the Xlcd Board, so here is a complete new program. Ideally driven by an 32u4 or MEGA2560, as they feature hardware serial and an independent serial port via USB or even multiple hardware serial ports. A Leonardo board is sufficient for all tasks at the moment, could be shrinked, if using a Arduino Micro (Pro Micro has lack of pins, but can take it too).

How it works:
--
The board works as a bridge between your computer and the GRBL controller. Simply connect your computer to `Serial` via the USB-Port and your GRBL board to `Serial1` (the only hardware serial pins on ATmega32u4). The board parses all information from the machine, to display infos at a LCD (16x2 is ok, 20x4 is great). If you don't want to use the pc, you can simply add a SD-Slot and switches to browse through the files and run one of these.

Under active development – to be released soon.
