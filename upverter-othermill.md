#Notes on Importing in to othermill


#upverter to othermill

##1. Download and prep files
  - Download the "Gerber Files" and "NC Drill (Excellon) files"
  - unzip the files
  - Change the extension of the Drill File(s) from .drill to .txt
  - move the drill file into the directory of the gerber files you just downloaded.
  - move to the desktop of the othermill computer prior to use.
  
##2. Prep othermill
	- Open Otherplan
	- Home the machine it will prompt this after the machine has been turned on.
	- Setup Fixturing
		-Toggle bracket and run through the steps to install the bracket. (You will need the 1/8" flat end bit)
	- Setup Material
	 	-Select board type and align to bracket

##3. Setup and Load Machine
	-Tape the board trying to cover the entire surface of board - on the edge where the bracket will go you want no tape exposed on the edges.
	-Select "Loading" to load machine
	-Fix board to machine and then home machine.

##4. Import files
  - select import
	- follow import instructions
	- if you want only nets without copper around them open "advanced..."
		- set clearance with to .5" or greater untill part is cleared.
  - in the "Advanced section" set trace cut depth to .02"
  - starting with the largest (1/8) bit add bits to the "Tools to use" section untill all holes can be drilled (1/8, 1/32, 1/64 works well)
  - Changing some of the settings to minify the use of the 1/64 may be neccessary - this is especially important on larger boards 1/64 bit takes much longer than the larger bits.
  - Once you have your board and everything looks correct select "Start Cutting..." if you are cutting multiple boards select "Cut Visible".
  - Follow instructions given by Other Mill


##Mecahnical details at the moment does not work.