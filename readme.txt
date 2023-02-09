Improved Video Board for Yamaha MSXs version 1.2
Copyright (c) 2016-2023 RBSC


About
-----

This is the improved video board for Yamaha YIS503II, YIS503III and similar MSX/MSX2 computers to replace the original video
boards or the older versions of the video boards from RBSC. The changes to the v1.2 board comparing to the previous verions are:

- Allows to use either CXA1675 or CXA2075 video encoder chips
- Contains an improved YTRAP filter
- Allows to use through-hole electrolytic capacitors (see note below)
- Allows to switch between on-board and internal MSX's 3.58MHz clock generator for NTSC
- Allows to disable one or both on-board clock generators
- Requires less components if CXA2075 encoder is used
- If using only computer's 3.58Mhz and NTSC, there's no need to assemble both clock generators

It is possible to use some components from the old black-and-white video board from the YIS503IIIR computer to build the v1.2
board. The following components can be re-used:

- 330uF capacitors (4)
- 10uF capacitors (4)
- 2sc1684 transistors (4)
- 100uF capacitors (2)
- DIN8 female socket
- Male 13-pin connector for motherboard's cable

IMPORTANT! When installing 100uF capacitors from the original board, please make sure to install the 16v rated capacitor as C3
and the 10v rated capacitor as C2. Otherwise, the 10v rated capacitor installed as C3 may blow up!


WARNING!
--------

Do not install ONBOARD and EXT jumpers at the same time! When using the EXT jumper, disable both NTSC and PAL clock generators
with their respective jumpers (see below).

The pinout of the RGB connector on the new video board differs from the original pinout! On the new board pin 3 is connected to
+12v supply. When making RGB to SCART cables or when using such cables designed for the Japanese MSX mashines, please make sure
that you connect the +12v to the correct SCART pin - pin 8. Connecting +12v to this pin will switch the TV/monitor to 4:3 mode.

DO NOT connect the cable from Yamaha YIS805 to this video board! The pin order is different on the YIS805 and you will damage
the board if you connect it to YIS805!

It is advised to power down the computer before switching between PAL and NTSC in order to avoid damage to the encoder chip.


Settings
--------

Compared to v1.1 of the videoboard, there are more jumpers. The jumpers labeled as PAL or NTSC DISABLE are used to disable the
on-board PAL or NTSC clock generators and use the internal computer's 3.58MHz clock for NTSC encoding. The installed jumper
disables the clock generator.

The ONBOARD and EXT jumpers are used to select which clock to use for NTSC encoding. When using the EXT jumper, the computer's
internal 3.58MHz clock will be fed to the encoder chip. This will effectively eliminate all color atrefacts in the composite
video output. But this will work only with NTSC mode. The installed jumper enables either on-board or external clock signal.
Never install both jumpers at the same time! Please note that the jumper settings do not affect the RGB output.

There are three 3-pin mode selection jumpers on the video board. These jumpers are used to set the color encoding for the S-Video
and composite video outputs. All 3 jumpers must be set the same way. When the pins 1-2 of the jumpers are shorted, the NTSC
encoding is enabled. Otherwise, when pins 2-3 of the jumpers are shorted, the PAL encoding is enabled. Please note that the
jumper settings do not affect the RGB output.

When setting up the board, it's recommended to measure the voltages on the outputs of 4 potentiometers (variable resistors). The
measurement should be done on the central pin. The correct voltage setting is required to form the stable picture on the
composite video and S-Video outputs.

When using the CXA1675 encoder chip, the recommended voltage for the CSYNC variable resistor is 1.3v, the recommended voltages
for Red, Green and Blue variable resistors are from 1.5v to 2.0v, depending on the desired brightness. The voltages on R, G and
B channels must be the same to avoid color distortion. Each color should be tuned after setting it as background color - for
example when setting the blue color's voltage, use the "color15,4,4" command in Basic to set blue as background color. For
green color use the "color15,2,2" command and for red color use the "color15,6,6" command.

When using the CXA2075 encoder chip, the voltage for CSYNC variable resistor should be set to 1.5v and the voltages for Red,
Green and Blue variable resistors should be set up to 3.0v to reach the desired brightness.


Notes
-----

When using the CXA2075 video encoder, it's not neccessary to install the following elements: C22, C23, C26, C27, R25, R29, R30.
Also, if L1 is not installed, please bridge its solder pads with a wire. However, it's highly recommended to use L1 for better
results.

When planning to use only NTSC encoding with the internal MSX's clock, it may not be necessary to install both oscillators,
both trim capacitors, 74HCT04 chip, C31, C13, C19, R17, R20, R23, as well as optional capacitors on the back side of the board.

Please use the following oscillators: 3.579MHz for NTSC and 4.433MHz for PAL. Using other oscillators may cause undesired side
effects.

It is recommended to use the 74HCT04 chip for the frequency generator circuit. The HC series chips may also work, but the HCT
series is highly recommended.

There may be artefacts on the color transitions in the composite video's output when using the on-board clock generators. These
artefacts can be removed by carefully adjusting the corresponding trim capacitors (C14 or C20) with a small flat screwdriver. 

The sharpness of the composite video output can be adjusted by the C23 trim capacitor that is marked as "YTRAP". Please use a
small flat screwdriver with an isolated handle to trim the capacitors, otherwise interference will occur.

If you are using a jumper pin header instead of the original cable connector, be careful to connect the cable from the MSX's
main board correctly. Incorrect cable connection may damage the video board and your MSX computer!


IMPORTANT!
----------

The RBSC provides all the files and information for free, without any liability (see the disclaimer.txt file). The provided information,
software or hardware must not be used for commercial purposes unless permitted by the RBSC. Producing a small amount of bare boards for
personal projects and selling the rest of the batch is allowed without the permission of RBSC.

When the sources of the tools are used to create alternative projects, please always mention the original source and the copyright!


Contact information
-------------------

The members of RBSC group Tnt23, Wierzbowsky, Pyhesty, Ptero, GreyWolf, SuperMax, VWarlock and DJS3000 can be contacted via the group's
e-mail address:

info@rbsc.su

The group's coordinator could be reached via this e-mail address:

admin@rbsc.su

The group's website can be found here:

https://rbsc.su/
https://rbsc.su/ru

The RBSC's hardware repository can be found here:

https://github.com/rbsc

The RBSC's 3D model repository can be found here:

https://www.thingiverse.com/groups/rbsc/things

-= ! MSX FOREVER ! =-
