# KiCAD Routing - TODO

## Auto Routing

For the Next step we're going to route the board

### Export .dsn file

  * First Select the Free Route Button
  * Next Press the button labled "Export a Specctra Design (*.dsn) File"
  * Save the .dsn file ideally to a seperate directory (the auto router will likley create other files where the dsn file is located)

<a href="../../images/KiCad/Routing/Pcb1.png"><img src="../../images/KiCad/Routing/Pcb1.png" height="50%" width="50%" ></a> <br>

Next grab a copy of the Freerouting jar from

  * <https://github.com/freerouting/freerouting/tree/master/binaries>

### Freerouting

Open the dsn file saved within Freerouting

<a href="../../images/KiCad/Routing/Freerouting1.png"><img src="../../images/KiCad/Routing/Freerouting1.png" height="50%" width="50%" ></a> <br>

Select AutoRoute

<a href="../../images/KiCad/Routing/Freerouting2.png"><img src="../../images/KiCad/Routing/Freerouting2.png" height="50%" width="50%" ></a> <br>

Select File -> Export Specctra Session File

<a href="../../images/KiCad/Routing/Freerouting3.png"><img src="../../images/KiCad/Routing/Freerouting3.png" height="50%" width="50%" ></a> <br>

This should result in a .rules and .ses file being exported into the same directory

### Import back to KiCad

Next import the .ses file back into KiCad.

<a href="../../images/KiCad/Routing/Pcb2.png"><img src="../../images/KiCad/Routing/Pcb2.png" height="50%" width="50%" ></a> <br>

This should then place the routes and via's

## Manual Routing

When manual routing, I find it easier to enable the two buttons highlighted

<a href="../../images/KiCad/Routing/Pcb3.png"><img src="../../images/KiCad/Routing/Pcb3.png" height="50%" width="50%" ></a> <br>

This way all the options for right click  / Drag / Delete tracks are available

## TODO

  * <https://www.wayneandlayne.com/blog/2013/02/26/kicad-tutorial-pcb-edges/>
  * <https://www.wayneandlayne.com/blog/2013/02/26/kicad-tutorial-copper-pours-fills/>
  * <https://www.wayneandlayne.com/blog/tag/kicad-tutorial/>

  * Unsolderable top pads, for battery and pin headers, tRestrict (Place -> Keep Out Area)
  * avoid vias under smd components, vRestrict (Place -> Keep Out Area)
  * TQFP will probably need thinner tracks