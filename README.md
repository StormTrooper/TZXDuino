# TZXDuino


Arduino based TZX and TAP (currently only ZX spectrum and Amstrad CPC flavour) file player.
Modified original souce to use LCD 16x2 without I2C

Parts Used
==========
Arduino Pro Mini
SD card module
16x2 LCD (This build is specifically for the non I2C Version)

Small audio amp, I used an LM386 module, but any headphone type amp should work
5 x Buttons (micro switches are best, but any should work)


Wiring
======
All buttons pull the pin to GND.

Arduino Pins
============

- A0 -> BUTTON (ROOT)
- 03 -> Output (To Amp)
- 10 -> SDCS (SD Card chip select)
- 11 -> MOSI (SD Card MOSI PIN)
- 12 -> MISO (SD Card MI PIN)
- 13 -> SCK (SD Card SCK PIN)
- 2  -> BUTTON (DOWN)
- A1 -> BUTTON (UP)
- A2 -> BUTTON (STOP)
- A3 -> BUTTON (PLAY)
- 4  -> LCD RS
- 5  -> LCD EN
- 6  -> LCD D4
- 7  -> LCD D5
- 8  -> LCD D6
- 9  -> LCD D7

LCD PINS
========

- LCD RS -> 4 ARDUINO
- LCD EN -> 5 ARDUINO
- LCD D4 -> 6 ARDUINO
- LCD D5 -> 7 ARDUINO
- LCD D6 -> 8 ARDUINO
- LCD D7 -> 9 ARDUINO
- VCC -> 5v
- GND -> GND

SD CARD PINS
============

- GND -> GND
- 5V -> 5V
- SDCS -> 10 ARDUINO
- MOSI -> 11 ARDUINO
- SCK -> 13 ARDUINO
- MISO -> 12 ARDUINO
- GND -> GND


Usage
=====

Wire up as above, and program the Arduino using the IDE.

Drop some TZX/TAP/CDT files onto a FAT32 formatted SD card, plug it into the TZXDuino, and power on.

Up/Down buttons move through the files, Play starts playback.

To get files to load first time you'll need to adjust the volume until you get a strong signal on the Spectrum / CPC. Once you've got a strong signal you should able to load most files as if you were using a normal tape.

History
=======

Starting with the Arduitape WAV playing project, i've moved to playing TZX and TAP files directly without needing to convert them to a WAV file first.

Credits
=======

Code: Andrew Beer
[Github](https://github.com/sadken)

LM386 circuit from 
[StackExchange](https://electronics.stackexchange.com/questions/65478/lm386-audio-amplifier-not-amplifying)

