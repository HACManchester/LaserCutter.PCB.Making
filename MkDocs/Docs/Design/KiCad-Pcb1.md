# KiCAD - PCB Part 1

## Assigning Footprints

First design your schematic within KiCad

<a href="../../images/Design/KiCad-PCB/Schematic1.png"><img src="../../images/Design/KiCad-PCB/Schematic1.png" height="50%" width="50%" ></a> <br>

Next we need to assign PCB footprints for each item on the schematic

<a href="../../images/Design/KiCad-PCB/Schematic2.png"><img src="../../images/Design/KiCad-PCB/Schematic2.png" height="50%" width="50%" ></a> <br>

Within the assign footprints window, we can

  * Filter by pin count
  * Filter by keywords associated with the PCB Footprint and Schematic part
  * Filter by Library
  * Get a preview of the footprint being assigned to the part

<a href="../../images/Design/KiCad-PCB/Schematic3.png"><img src="../../images/Design/KiCad-PCB/Schematic3.png" height="50%" width="50%" ></a> <br>

Typically with KiCad it stores multiple schematic parts within a single .lib file <br>
But the PCB Footprints are usually stored one file per footprint within a directory ending in .pretty

## Generating the NetList

Next we need to generate a netlist file as an input to the PCB Editor pcbnew <br>
Click on the Netlist button within the schematic editor

<a href="../../images/Design/KiCad-PCB/Schematic4.png"><img src="../../images/Design/KiCad-PCB/Schematic4.png" height="50%" width="50%" ></a> <br>

This will cause a file called ProjectName.net to be outputed within the Project Directory

## Opening the PCB

Next we're going to read in the netlist into the PCB Editor pcbnew <br>
Open up pcbnew and Click the **Read NetList** button

<a href="../../images/Design/KiCad-PCB/Pcb1.png"><img src="../../images/Design/KiCad-PCB/Pcb1.png" height="50%" width="50%" ></a> <br>

Click Current Netlist and check the bottom for any errors when the file is read in

<a href="../../images/Design/KiCad-PCB/Pcb2.png"><img src="../../images/Design/KiCad-PCB/Pcb2.png" height="50%" width="50%" ></a> <br>

## Creating a Edge cut out Border

You should now have a bunch of components all grouped together in one place <br>
For the next step we're going to draw a Edge Cut out / Border around the components <br>

  * Select Change Cursor Shape to make the cursor a horizontal / vertical line on the PCB, this will help when drawing the box
  * Select the Edge Cuts layer for drawing the box
  * Pressing the Space key will zero the relative cordinates at the bottom for measuring distance
  * The Blue line icon can be used to draw the box around the footprints

<a href="../../images/Design/KiCad-PCB/Pcb3.png"><img src="../../images/Design/KiCad-PCB/Pcb3.png" height="50%" width="50%" ></a> <br>

Right Click -> End Drawing once you've reached the last corner <br>
It's also best to do this with a grid of 1mm
