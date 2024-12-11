# CoBra XP

CoBra XP is a Z80 computer design derived from the [Cobra](https://github.com/ceteras/CoBra) project.

It is built for eXPerimenting with digital circuits and creating new Z80 projects.  
This is made to honor the community of modders who have worked hard on their Cobra computers, adding features and extensions.  
Their work meant cutting tracks, adding wires, building extension boards, and most important, knowing the pcb and schematic to perfection, bringing amazing innovative solutions.  
Examples of this kind of contributions can be seen on [cobrasov.com](https://cobrasov.com/CoBra%20Project/index.html).

It comes without saying that one must know what they're doing when building with Cobra XP.  
Also if you don't have experience building electronics, this project can be a serious learning platform for you.

## Disclaimer:
I offer no guarantees of any kind. This is an experiment, join at your own risk!  
The original project, as many others similar to them have a reputation of a certain difficulty to make it work.  
For some of us, this is the best part, after building it, the debugging sessions can be spectacular and lead to a better understanding.

## Experiment status
An order for a batch of boards has been placed to one of the very popular pcb manufacturers.

![CoBra mainboard](https://github.com/ceteras/Cobra-Xp/blob/main/img/mainboard.png?raw=true)

The 10 boards have arrived to those who joined the group order, and one of them is up & running, in the 64K configuration.

![CoBra mainboard](https://github.com/ceteras/Cobra-Xp/blob/main/img/CobraXP_NM.jpg?raw=true)

## Specs:

- 3.5MHz Z80A CPU
- two banks of 16pin DRAM chips, can fit 4164 or 5V only 16Kbit DRAM like MCM4517
- three memory maps, one for each: boot, CP/M mode, ZX Spectrum mode
- boot rom can be 27C128, 27C256, 27C512, 28C256 (28 pin)
- BASIC interpreter rom is in 32pin socket, up to 4MBit 39SF040 (8x 16KB pages selectable in software, two more jumpers for MSB addresses)
- 256 x 192 resolution ZX Spectrum video interface, relocatable base address (boot and CP/M modes place video area at a different address)
- 58 keys keyboard, featuring 50 keys for ZX Spectrum mode plus 8 for CP/M
- AY39810 sound chip
- i8272 floppy interface - on a daughter board (not included in the repo for now)
- RS232 port (bit-banged)
- joystick port
- prototyping area, can fit a PLCC 84 THT socket
- 5 non-populated 28pin 7.62mm DIN footprints, can 26CV12 GAL chips for example.  
each of them has a row of pads connected to each pins for easier wiring
- 6x 10 pin headers plus one 4 pin for power, connected to address and data bus plus some important signals on the board  
this is intended to allow creating daughter boards.   
they fit a perfboard, they are aligned to a 0.1 inch pitch  
a template for an extension daughter board can be seen in extensions/template
- 8x GND test points spread throughout the board, intended for beaded test points useful to hook a scope probe ground clip
- address and data busses are also present as test points
- smd jumpers split some connections, most of them on the bottom side, they help with modding, [documentation here](https://github.com/ceteras/Cobra-Xp/blob/main/documentation/Jumpers.ods)
- extension port using a 3x32 pin DIN41612 connector
