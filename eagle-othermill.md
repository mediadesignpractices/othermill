# Producing PCBs on the Othermill (from EAGLE)
Casey Anderson, Winter 2016

## CNC overview

A CNC Machine removes precise parts of a multi-layer material that are unnecessary, leaving (in the case of producing circuit boards) conductive traces for current to flow and / or holes to slide components / screws into.

<blah blah something about endmills and changing them>

Circuit boards are generally multi-layered. They consist are of a  Fiberglass substrate (to mount and hold traces and components in place) with a layer of Copper (to conduct current) glued to it. Our Othermill can make circuit boards from two types of "blanks":

* Single Sided: a layer of copper on one side of the fiberglass.

* Double Sided: consisting of a layer of copper on both sides of the fiberglass.

The material for a single sided board is referred to as FR-1. A double-sided board is typically referred to as FR-2. It is important to note that copper oxidizes (rusts) over time so all circuit board blanks must remain in an air-tight container when not in use.


## Powering the Othermill

Once you have logged into the computer, make sure that the othermill is connected to a computer via USB and that the power switch on the back panel is in the on position. When the mill first turns on it plays a short little melody. If the light inside the mill is off that means the mill is not on.


## Open Otherplan

Launch Otherplan, the software that talks to the mill. If the mill is connected and on, you should see a warning, as soon as the program is running, at the bottom of the window suggesting that you Home the Machine. Click Start Homing and wait until it finishes resetting each motor to its default position.


## Setup Fixturing

There are two fixtures typically used with the mill: the aluminum spoil board and the bracket. We never remove the spoil board, and prefer to keep the bracket attached to the spoil board at all times. The bracket is intended to makes alignment easier when cutting on both sides of the same object (example: double sided circuit board). Do not remove it unless you have a reason to.

1. Click on Setup Fixturing in the setup Menu. You will see a new menu appear at the bottom of the window wherein you can either configure the spoil board or the bracket. Make sure Bracket is selected and then click Locate.

2. The spoil board will move to the inside edge of the front panel of the machine. Before doing anything else, take a moment to make sure there isn't any leftover debris on the spoil board. If you see any fiberglass particles, or small bits of metal, use the vacuum cleaner under the mill to suck it up. When you are sure that the spoil board is clear click continue in the window at the bottom of the Otherplan UI.

3. The mill will prompt you to Reverse the endmill. You should ONLY USE THE 1/16th or 1/8th endmill for this part, as the 1/32" and 1/64" endmills are too delicate to be inserted backwards into the mill. Using both of the wrenches, carefully remove whatever endmill is already in the collet, store it in the clear plastic holder, and locate either the 1/16th or 1/8th endmills. Once you have located the correct endmill, reverse it so the untapered shaft is pointing down towards the spoil board, slide it some (but not all) of the way into the collet, and tighten with the wrenches until snug. Click Continue to move to the next step.

4. The mill will return to home.

5. The window at the bottom will instruct you to Align tool tip to bottom of carriage. Look at the graphic above the spoil board in the UI and adjust (by clicking either Z+ or -Z) the position of the bottom tip of the endmill such that it is anywhere between the edges of the "safe zone." The bottom-most point of the endmill doesn't need to be exactly in the middle, just somewhere within those two lines. When you are done adjusting the height of the endmill click continue.

6. Otherplan will prompt you to double check that there is nothing on the spoil board. If it is clear, simply click Locate. The mill will now automatically calculate its height relative to the spoil board and then check to make sure the bracket is properly attached. Every once in a while the mill throws an error in the midst of the location process because it thinks it has found something conductive that is not the spoil board. If this happens, check to make sure there are not any metal filings, or other debris, on the spoil board and try to restart the location process. If the error persists I have successfully resolved this by power cycling the machine. When the machine returns to home you are done with this part of the setup process.


## Setup Material (pt. 1)

1. Click Setup material in the setup window.

2. A new window should pop up at the bottom wherein you can set the material properties. Choose Double-Sided and then click Continue.

3. Next simply click Align to Bracket and then Done.


## Setup Material (pt. 2)

1. Cover one side of the Circuit board evenly with double sided tape. Be careful not to overlap any strips of tape, as we want the board to sit as evenly on the spoil board as possible otherwise our holes will be at an angle.

2. Trim any tape that hangs past the edge. Tape on the edges could also make the board uneven on the spoil board surface. I use a hardware store razor blade for this but an Xacto knife would work also.

3. Now align the bottom left corner of the board into the corner of the Bracket so that the side and bottom edge are flush against the Bracket. Press firmly with your hands across all parts of the board so that it lays flat and feels firmly attached. It should look like this:

<insert photo here>


## Importing your EAGLE file into Otherplan

 Otherplan, can import .brd files directly from EAGLE (hoorray, no Gerber file nonsense!). To import your .brd file click Import Files in the Otherplan setup window and select your file. If you have done this correctly you should see your PCB design on the material in the UI.

 (insert photo of the above here)


##
