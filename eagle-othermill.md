# Producing PCBs on the Othermill (from EAGLE)
Casey Anderson, Winter 2016

 The software that controls the Othermill, known as Otherplan, can import .brd files directly from EAGLE. To import your .brd file click Import Files in the Otherplan setup menu and select your file. If you have done this correctly you should see your PCB design on the material in the UI.

 (insert photo of the above here)

The CNC Machine is like the opposite of the 3D Printer: it removes parts of the multi-layer material that are unnecessary, leaving only conductive traces for current to flow or holes to slide components into (in the case of Pin Through Hole parts).

Circuit boards consist of a multi-layer material made of a  Fiberglass substrate (to mount and hold traces and components in place) with a layer of Copper (to conduct current) glued to it. Our Othermill can make circuit boards from two types of "blanks": Single Sided (there is only a copper layer on one side of the fiberglass) or Double Sided (conductive on both sides of the fiberglass). The material for a single sided board is referred to as FR-1 whereas the material for a double sided board is referred to as FR-2. It is important to note that copper oxidizes over time so all circuit board blanks must remain in an air tight container when not in use.

The Othermill has a 5x4in spoilboard, so the material  blank board
