# TMS9929A / TMS9928A RGB
## A RGB demodulator for TMS9929A / TMS9928A chip, mostly used on MSX computers and Colecovision. 

This board outputs RGB+CSYNC from the original YPbPr chip channels of the TMS99 chip. 
Output from each color channel can be adjusted using a trimmer. 
Based on the [Universele interface RGB op MSX1 en SV.328](http://www.msxarchive.nl/pub/msx/mirrors/hanso/hwdoityourself/rgbmsx1.pdf). Mine fixes the emitter follower transistors of this version.
This repository contains the KiCad project and the gerber files.

## Features
- Each channel can be tuned
- Provides audio output pin
- Provides 5V output pin (if you want to use it with an RGB Scart cable for TV)
- Fits into the MSX composite modulator slot
- Extremely cheap!

## Video
[![TMS99 RGB BOARD](https://img.youtube.com/vi/eCPy9jgGLzQ/0.jpg)](https://www.youtube.com/watch?v=eCPy9jgGLzQ)

## Sample output (photo taken on BVM 20DU)
![VIDEO OUT](https://raw.githubusercontent.com/elder0010/msx_rgb/main/images/msx.jpg)

## Assembled PCB
![PCB](https://github.com/elder0010/msx_rgb/blob/main/images/1.jpg)

## The PCB in a Phonola VG-8020
![PCB](https://github.com/elder0010/msx_rgb/blob/main/images/2.jpg)

## External view of the mini din connector (RF modulator has been replaced)
![PCB](https://github.com/elder0010/msx_rgb/blob/main/images/3.jpg)

## Perks
This board provides an RGB output for the TMS9929A / TMS9928A chip.
Even if it's impossible to have 100% correct colours, it's possible to obtain a palette very close to the correct one in this way:
- Set each RGB trimmer to 0
- Turn up a little the RED and GREEN potentiometer until something visible appears on screen
- Turn up the BLUE potentiometer until the background becomes blueish - keep in mind that the blue channel is the most problematic one because of the TMS99x non-standard design
- Execute the command color 1,1 to set the screen and the text to black
- Notice how the black is blueish, and turn down the BLUE potentiometer until the background becomes less blueish ;)
- Execute the command color 15,4 to restore the screen to the default colours
- Repeat until you get a satisfactory result
- adjust the GREEN and the RED potentiometer accordingly 

In this way the palette should be close to the original.

## Compatibility
This board has been tested with TMS9929A (PAL) chip and TMS9928A (NTSC).

- PCB shape is the same of [TMS9929A RGB and Component adapter](https://hackaday.io/project/13056-tms9929a-rgb-and-component-adapter)
- Special thanks to [iz8dwf](https://www.youtube.com/iz8dwf)
