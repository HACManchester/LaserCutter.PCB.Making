# KiCAD - PCB Part 2

## Locking parts

For the next step we're going to move and lock the parts which need to be at the edges of the board in place

  * Click / Turn on the Mode footprint button
  * Move each of the parts which need to be in a fixed place into position
  * Right Click on those parts and select Lock **Footprint**

<a href="../../images/Design/KiCad-PCB/Pcb4.png"><img src="../../images/Design/KiCad-PCB/Pcb4.png" height="50%" width="50%" ></a> <br>

## Place parts

Next we're going to use the Auto Place feature of KiCad just to do an initial placement <br>
(make sure Alex doesn't catch you using this)

Make sure to set the grid size to something fairly small before using this.
Also you may want to manually move things around afterwards for better placement
I just find it's a good initial step before anything else

<a href="../../images/Design/KiCad-PCB/Pcb5.png"><img src="../../images/Design/KiCad-PCB/Pcb5.png" height="50%" width="50%" ></a> <br>

## Design Rules

Next we're going to set the design rules for the board.

### Hackaday Suggestions

Looking at this hackaday link for boards made using a Laser Cutter.
Its suggests the following

  * <https://hackaday.com/2013/05/11/laser-cutter-helps-make-dual-sided-pcbs/>

| Rule               | Min              | Typical          | Max             |
| -------------------|------------------|------------------|-----------------|
| Track Clearance    |                  | 15mil (0.381mm)  |                 |
| Track Width        | 22mil (0.5588mm) |                  |                 |
| Drill size         | 20mil (0.508mm)  |                  |                 |
| Vias / Outer       | 18mil (0.4572mm) |                  | 20mil (0.508mm) |
| Pads Top / Bottom  | 15mil (0.381mm)  |                  |                 |
| Autorouting Grid   |                  | 2mil (0.0508mm)  |                 |

They also suggest

  * 24 gauge wire or thinner is used for Vias
  * Drill bit is 0.02" (0.508mm) in diameter for via holes
  * Drill bit is 0.04" (1.016mm) in diameter for header pin holes

### Kicad Design Rules

By Selecting Desgin Rules -> Design Rules from the menu we can create a new NetClass to add in values
You may want to play around with different smaller values to see what is possible.

| Header      | Value     |
|-------------|-----------|
| Name        | Laser PCB |
| Clearance   | 0.381     |
| Track Width | 0.5588    |
| Via Dia     | 0.7       |
| Via Drill   | 0.508     |
| uVia Dia    | 0.7       |
| uVia Drill  | 0.508     |

Also you need to apply this netclass to all the components on the list

<a href="../../images/Design/KiCad-PCB/Pcb6.png"><img src="../../images/Design/KiCad-PCB/Pcb6.png" height="50%" width="50%" ></a> <br>

## Auto Routing

For the Next step we're going to route the board

### Export .dsn file

  * First Select the Free Route Button
  * Next Press the button labled "Export a Specctra Design (*.dsn) File"
  * Save the .dsn file ideally to a seperate directory (the auto router will likley create other files where the dsn file is located)

<a href="../../images/Design/KiCad-PCB/Pcb7.png"><img src="../../images/Design/KiCad-PCB/Pcb7.png" height="50%" width="50%" ></a> <br>

Next grab a copy of the Freerouting jar from

  * <https://github.com/freerouting/freerouting/tree/master/binaries>

### Freerouting

Open the dsn file saved within Freerouting

<a href="../../images/Design/KiCad-PCB/Freerouting1.png"><img src="../../images/Design/KiCad-PCB/Freerouting1.png" height="50%" width="50%" ></a> <br>

Select AutoRoute

<a href="../../images/Design/KiCad-PCB/Freerouting2.png"><img src="../../images/Design/KiCad-PCB/Freerouting2.png" height="50%" width="50%" ></a> <br>

Select File -> Export Specctra Session File

<a href="../../images/Design/KiCad-PCB/Freerouting3.png"><img src="../../images/Design/KiCad-PCB/Freerouting3.png" height="50%" width="50%" ></a> <br>

This should result in a .rules and .ses file being exported into the same directory

### Import back to KiCad

Next import the .ses file back into KiCad.

<a href="../../images/Design/KiCad-PCB/Pcb8.png"><img src="../../images/Design/KiCad-PCB/Pcb8.png" height="50%" width="50%" ></a> <br>

This should then place the routes and via's

## Manual Routing

When manual routing, I find it easier to enable the two buttons highlighted

<a href="../../images/Design/KiCad-PCB/Pcb9.png"><img src="../../images/Design/KiCad-PCB/Pcb9.png" height="50%" width="50%" ></a> <br>

This way all the options for right click  / Drag / Delete tracks are available

## TODO

  * <https://www.wayneandlayne.com/blog/2013/02/26/kicad-tutorial-pcb-edges/>
  * <https://www.wayneandlayne.com/blog/2013/02/26/kicad-tutorial-copper-pours-fills/>
  * <https://www.wayneandlayne.com/blog/tag/kicad-tutorial/>
