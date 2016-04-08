# KiCad - Creating an edge border

One of the first steps when creating a new PCB is to set the edge of the board. <br>
There's a number of reasons for doing this.

  * This will define the outer edge for cutting the board
  * This will define the limits for the auto placement feature if used.
  * This will define the limits for the auto routing feature if used.

Looking at the below screen grab

<a href="../../images/KiCad/EdgeBorder/Pcb1.png"><img src="../../images/KiCad/EdgeBorder/Pcb1.png" height="50%" width="50%" ></a> <br>

One of the first things your probably going to want to do is to change the cursor from a simple cross to a set of lines that span the entire board.
This makes creating box outlines a fair bit easier when drawing them.
The button is the one highlighted on the far left.

Next select the yellow **Edge Cuts** layer at the top right

When measuring distance on the board it's possible to use the **Space** key to set a zero point.
This will set dx and dy at the bottom on the toolbar to a zero point, you can then use this to measure distance across the board

To start the edge cuts line, click the **blue dotted line** highlighted on the right to start drawing the box. <br>
Use **Right Click -> End Drawing** once you've reached the last corner

It's also best to do this with a grid of 1mm, the cursor will auto snap to the grid but you can change the grid size along the top toolbar.

