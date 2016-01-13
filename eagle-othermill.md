# Producing PTH PCBs on the Othermill (from EAGLE)
Casey Anderson, Winter 2016


## Introduction

This article provides instructions for producing a double-sided `PCB`, designed in EAGLE, on MDP's Othermill. The acronym `PCB` stands for `Printed Circuit Board`. Since this is double-sided, we will stick with `Pin Through Hole` (often shortened to `PTH`) components.

## CNC overview

A CNC Machine removes precise parts of a multi-layer material that are unnecessary, leaving (in the case of producing circuit boards) conductive traces for current to flow and / or holes to slide components into.

Material removal is accomplished via a collection of `endmills` (which are similar to drill bits). Larger `endmills` are "faster" or better at easily removing lots of material quickly, whereas smaller `endmills` are "slower" or better at removing material from increasingly tiny areas. Generally one tries to minimize cut time by using the largest `endmills` for as much of the job as possible.

Two wrenches are magnetically attached to the Othermill in order to facilitate switching out `endmills` from the `collet` (the metal cone that holds the endmills in place), a normal part of completing diferent parts of a job.

You can complete most circuit board jobs with the following `endmills`: `1/64"`, `1/32"`, and `1/8"`.

Circuit boards are generally multi-layered. They consist of a Fiberglass substrate (to mount and hold `traces` and components in place) with a layer of Copper (to conduct current) glued to it. The Othermill can make circuit boards from two types of `blanks`:

* Single Sided: a layer of copper on one side of the fiberglass.

* Double Sided: consisting of a layer of copper on both sides of the fiberglass.

The material for a single sided board is referred to as `FR-1`. A double-sided board is typically referred to as `FR-2`. It is important to note that copper oxidizes (rusts) over time so all circuit board blanks must remain in an air-tight container when not in use.


## Powering the Othermill

Once you have logged into the computer make sure that the mill is connected to via USB and that it's power switch (on the back panel) is in the on position. If the light inside the mill is off the mill is not on.


## Open Otherplan

Launch Otherplan, the software that talks to the mill. If the mill is connected and on, you should see a warning at the bottom of the window suggesting that you `Home the Machine`. Click `Start Homing` and wait until it finishes resetting each motor to its default position.


## Setup Fixturing

There are two fixtures typically used with the mill: the aluminum `spoil board` and the `bracket`. We never remove the `spoil board`, and prefer to keep the `bracket` attached at all times. The `bracket` is intended to make alignment easier when cutting on both sides of the same object (example: double sided circuit board). Do not remove it unless you have a reason to.

1. Click on `Setup Fixturing` in the setup menu. You will see a new window appear at the bottom of the UI wherein you can either configure the `spoil board` or the `bracket`. Make sure `Bracket` is selected and then click `Locate`.

2. The spoil board will move to the inside edge of the front panel of the machine. Before doing anything else, make sure there isn't any leftover debris on the `spoil board`. If you see any fiberglass particles, or small bits of metal, use the vacuum cleaner under the mill to suck it up. When you are sure that the spoil board is clear click `continue` in the window at the bottom of the Otherplan UI.

3. The mill will prompt you to `Reverse the endmill`. You should only use the `1/16" or 1/8" endmill` for this part, as the others are too delicate to be inserted backwards into the mill. Using both of the wrenches, carefully remove whatever `endmill` is already in the `collet`, return it to its clear plastic holder, and locate either the `1/16th or 1/8th endmills`. Once you have located the correct `endmill`, reverse it so the `untapered shaft` is pointing down towards the `spoil board`, slide it some (but not all) of the way into the `collet`, and tighten with the wrenches until snug. Click `Continue` to move to the next step.

4. The mill will return to home.

5. The window at the bottom will instruct you to `Align tool tip to bottom of carriage`. Look at the graphic above the spoil board in the UI and adjust (by clicking either` Z+` or `-Z`) the position of the bottom tip of the `endmill` such that it is anywhere between the edges of the `safe zone`. The bottom-most point of the `endmill` doesn't need to be exactly in the middle, just somewhere within those two lines. When you are done adjusting the height of the `endmill` click continue.

6. Otherplan will prompt you to double check that there is nothing on the `spoil board`. If it is clear, simply click `Locate`. The mill will automatically calculate its height relative to the `spoil board` and then check to make sure the `bracket` is properly attached. Every once in a while the mill throws an error in the midst of the location process because it thinks it has found something conductive that is not the `spoil board`. If this happens, check to make sure there are not any metal filings, or other debris, on the `spoil board` and try to restart the location process. If the error persists I have successfully resolved this by power cycling the machine. When the machine returns to home you are done with this part of the setup process.


## Setup Material (pt. 1)

1. Click `Setup material` in the setup window.

2. A new window should pop up at the bottom wherein you can set the material properties. Choose `Double-Sided` and then click `Continue`.

3. Next simply click `Align to Bracket` and then `Done`.


## Setup Material (pt. 2)

1. Cover one side of the Circuit board evenly with double sided tape. Be careful not to overlap any strips of tape, the board needs to sit as evenly on the `spoil board` as possible.

2. Trim any tape that hangs past the edge. Tape on the edges could also make the board uneven on the `spoil board` surface. I use a hardware store razor blade for this but an Xacto knife would also work.

3. Align the bottom left corner of the board into the corner of the `bracket` so that the side and bottom edge are flush. Press firmly with your hands across all parts of the board so that it lays flat and feels firmly attached. It should look like this:

<insert photo here>


## Importing your EAGLE file into Otherplan

 Otherplan, can import `.brd` files directly from EAGLE (hooray, no Gerber file nonsense!).

 1. To import your `.brd` file click `Import Files in the Otherplan` setup window and select your file. If you have done this correctly you should see your PCB design on the material in the UI.

 (insert photo of the above here)



## Selecting Mills / Configuring Feeds and Speeds

blah blah


## Flight Check


## Changing Endmills

## Flipping the Board
