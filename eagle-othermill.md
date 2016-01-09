# Producing PCBs on the Othermill (from EAGLE)
Casey Anderson, Winter 2016

## CNC overview

The CNC Machine is like the opposite of a 3D Printer: it removes precise parts of material that are unnecessary, leaving (in the case of producing circuit boards) only conductive traces for current to flow or holes to slide components into (in the case of Pin Through Hole parts).

<blah blah something about endmills and changing them>

Circuit boards consist of a multi-layer material made of a  Fiberglass substrate (to mount and hold traces and components in place) with a layer of Copper (to conduct current) glued to it. Our Othermill can make circuit boards from two types of "blanks":

* Single Sided: a layer of copper on one side of the fiberglass only.

* Double Sided: consisting of a layer of copper on both sides of the fiberglass.

The material for a single sided board is referred to as FR-1 whereas the material for a double sided board is referred to as FR-2. It is important to note that copper oxidizes (rusts) over time so all circuit board blanks must remain in an air-tight container when not in use.


## Powering the Othermill

Once you have logged into the computer, make sure that the othermill is connected to a computer via USB and that the power switch on the back panel is switched on. When the mill is on you should hear a short little melody and see a light turn on inside of the cutting area.


## Open Otherplan

After verifying that the mill is plugged into the CPU and on, launch Otherplan, the software that talks to the mill. If the mill is connected and on, you should see a warning, as soon as the program is running, at the bottom of the window suggesting that you Home the Machine. Click Start Homing and wait until it finishes resetting each motor to its default position.


## Setup Fixturing

There are two fixtures typically used with the mill: the spoilboard and the bracket. We never remove the spoilboard, and prefer to keep the bracket attached to the spoilboard at all times. The bracket is intended to assist with alignment when cutting parts on multiple sides of the same object (example: double sided circuit board), but its easiest to just leave it attached unless you have a specific reason to remove it.

1. Click on Setup Fixturing in the setup Menu. You will see a new menu appear at teh bottom of the window wherein you can either configure the spoilboard or the bracket. Make sure Bracket is selected and then click Locate.

2. This will move the spoilboard to the inside edge of the front panel of the machine where you could attach the bracket to the spoilboard. You shouldn't need to attach the bracket, though, as it should already be attached. Before doing anything else, take a moment to make sure there isn't any leftover debris on the spoilboard. If you see any fiberglass particles, or small bits of metal, use the vacuum cleaner under the mill to suck it up. When you are sure that the bracket is attached and the spoilboard is cleared, click continue in the menu at the bottom of the Otherplan UI.

3. The mill will prompt you to Reverse the endmill. You should ONLY USE THE 1/16th or 1/8th endmill for this part, as the 1/32" and 1/64" endmills are too delicate to be inserted backwards into the mill.




## Importing your EAGLE file into Otherplan

 Otherplan, can import .brd files directly from EAGLE. To import your .brd file click Import Files in the Otherplan setup menu and select your file. If you have done this correctly you should see your PCB design on the material in the UI.

 (insert photo of the above here)

##
