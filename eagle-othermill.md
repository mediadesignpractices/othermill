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

3. The mill will prompt you to Reverse the endmill. You should ONLY USE THE 1/16th or 1/8th endmill for this part, as the 1/32" and 1/64" endmills are too delicate to be inserted backwards into the mill. Using both of the wrenches, carefully remove whatever endmill is already in the collet, put it in its holder, and locate either the 1/16th or 1/8th endmills. If you are not sure which endmill is which you can check the size by measuring with the calipers in the Making Lab. Once you have located the correct endmill, reverse it so the untapered shaft is pointing down towards the spoilboard, slide it some (but not all) of the way into the collet, and tighten the collet with the wrenches until snug. Click Continue to move to the next step.

4. The return to home once you click continue.

5. The menu at the bottom should be instructing you to Align tool tip to bottom of carriage. Look at the graphic above the spoilboard in the UI and adjust (by clicking either Z+ or -Z) the position of the bottom tip of the endmill such that it is anywhere between the edges of the "safe zone." The bottom-most point of the endmill doesnt need to be exactly in the middle, just somewhere within those two lines. When you are done adjusting the height of the endmill, click continue.

6. Otherplan will prompt you to double check that there is nothing on the spoilboard. If it is clear, simply click Locate. The mill will now automatically calculate its height relative to the spoilboard and then check to make sure the bracket is properly attached. Every once in a while the mill throws an error in the midst of the location process because it thinks it has found something conductive that is not the spoilboard. If this happens, check to make sure there are not any metal filings, or other debris, on the spoilboard and try to restart the location process. If the error persists I have successfully resolved this by power cycling the machine. When the machine returns to home you are done with this part of the setup process.


## Setup Material (pt. 1)

1. Next click Setup material in the setup window.

2. A new window should pop up at the bottom wherein you can set the material properties. Choose either Double-Sided and then click Continue.

3. Next simply click Align to Bracket and then Done.


## Setup Material (pt. 2)

1. Cover one side of the Circuit board evenly with double sided tape. Be careful not to overlap any strips of tape, as we want the board to sit as evenly on the spoilboard as possible otherwise our holes will be at an angle.

2. Trim any tape that hangs past the edge. Tape on the edges could also make the board uneven on the spoilboard surface.

3. Now align the bottom left corner of the board into the corner of the Bracket so that the side and bottom edge are flush against the Bracket. Press firmly with your hands across all parts of the board so that it lays flat and feels firmly attached. It should look like this:

<insert photo here>


## Importing your EAGLE file into Otherplan

 Otherplan, can import .brd files directly from EAGLE. To import your .brd file click Import Files in the Otherplan setup menu and select your file. If you have done this correctly you should see your PCB design on the material in the UI.

 (insert photo of the above here)


## 
