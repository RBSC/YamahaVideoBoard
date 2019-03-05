Improved Video Board for Yamaha MSXs version 1.1
Copyright (c) 2016 RBSC


Notes
-----

Please use the following oscillators: 3.579 MHz for NTSC and 4.433 MHz for PAL.

It is recommended to use 74HCT04 chip for the frequency generator circuit. The possible interference on the composite video output
can be reduced to a minimum by the trim capacitors.

When setting up the board, it's recommended to measure the voltages on the outputs of 4 potentiometers (variable resistors). The
correct voltage setting is required to form the picture on the composite video and S-Video outputs. The recommended voltage for
the CSYNC variable resistor is 1.3v, the recommended voltages for Red, Green and Blue variable resistors is from 1.5v to 2.0v
depending on the desired saturation. The voltages on R, G and B must be the same to avoid color distortion. Each color should be
tuned after setting it as background - for example when setting the blue color's voltage, use the "color15,4,4" command in Basic
to set blue as background color.

If you are using a jumper pin row instead of the original connector, be careful to connect the cable from the MSX's main board
correctly. Incorrect cable connection can damage the video board and MSX!


IMPORTANT!
----------

The RBSC provides all the files and information for free, without any liability (see the disclaimer.txt file). The provided information,
software or hardware must not be used for commercial purposes unless permitted by the RBSC. Producing a small amount of bare boards for
personal projects and selling the rest of the batch is allowed without the permission of RBSC.

When the sources of the tools are used to create alternative projects, please always mention the original source and the copyright!


Contact information
-------------------

The members of RBSC group Wierzbowsky, Ptero and DJS3000 can be contacted via the MSX.ORG or ZX-PK.RU forums. Just send a personal
message and state your business.

The RBSC repository can be found here:

https://github.com/rbsc


-= ! MSX FOREVER ! =-
