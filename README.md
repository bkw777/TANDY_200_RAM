# Option RAM module for TANDY 200

Replacements for TANDY 26-3866 24K SRAM module for TANDY 200 portable computer.

There are a few different options here. You pick whichever you need.  
* Single-bank, SOP-28 chip - Drop-in replacement for the original 24K module, with a large-ish chip that's relatively easy to solder by hand. Use this if you already have one original ceramic module, and want to keep using it, and just want one more 24K module to fill the machine, and you prefer to use, or happen to already have an SOIC-28/SOP-28 version of the SRAM chip.
* Single-bank, TSOP-28 chip - Same as above but uses a TSOP version of the SRAM chip.
* Dual-bank, SOP-32 chip - This provides the full 48 as 2 normal 24K modules all on one board. You plug a single one of these into OPTION RAM#2 slot. Uses an SOIC-32/SOP-32 chip for easier hand soldering.
* Dual-bank, TSOP-32 chip - Same as above but uses a TSOP version of the SRAM chip. These are more common and more available, but also more of a challenge to solder by hand.

<!--
There are a few different designs available that all do the same thing but using different parts.

Some variants are single-bank like the original TANDY 26-3866 ceramic 24k module. These are drop-in replacements for the original modules, where one board = one bank = one Option RAM socket. You can have up to two boards installed in the machine.

Some variants are dual-bank, where one board supplies both Option RAM bank #1 and #2. You plug the one board into the Option RAM #2 socket, and this takes the place of two single-bank modules.

Some variants use different chip packages, so that you have options to use whatever types of chip you have, or can get, or can solder by hand.

There is also a [schematic of the original RAM bank](TANDY_26-3866.svg), re-drawn in KiCAD just for reference. There is no PCB for this, it's just for reference while designing new replacement modules to help ensure the replacement really still outwardly works the same as the original.
-->

See the [releases](../../releases) tab for gerber zips for manufacturing.  
If there is no link to order a pcb for one of the versions below, it means that design isn't tested and proven yet.

## Single-Bank - SOP

![](../../raw/main/TANDY_200_RAM.jpg)  
![](../../raw/main/TANDY_200_RAM_top.jpg)  
![](../../raw/main/TANDY_200_RAM_bottom.jpg)  
![](../../raw/main/TANDY_200_RAM.svg)  

<!-- PCB from [OSHPark](),  or  [PCBWAY](),  or  [gerbers](../../releases/latest/)  -->
BOM from [DigiKey](https://www.digikey.com/short/f5hhwt4j),  or  [TANDY_200_RAM.BOM.csv](TANDY_200_RAM.BOM.csv)  

## Single-Bank - TSOP

![](../../raw/main/TANDY_200_RAM_tsop.jpg)  
![](../../raw/main/TANDY_200_RAM_tsop_top.jpg)  
![](../../raw/main/TANDY_200_RAM_tsop_bottom.jpg)  

<!-- ![](../../raw/main/TANDY_200_RAM_tsop.svg)   -->

<!--
PCB from [OSHPark](),  or  [PCBWAY](),  or  [gerbers](../../releases/latest)  
BOM from [DigiKey](),  or  [BOM.csv]()  
-->

<!--
## Single-Bank THT DIP

![](../../raw/main/TANDY_200_RAM_tht.jpg)  
![](../../raw/main/TANDY_200_RAM_tht_top.jpg)  
![](../../raw/main/TANDY_200_RAM_tht_bottom.jpg)  
![](../../raw/main/TANDY_200_RAM_tht.svg)  

PCB from [OSHPark](),  or  [PCBWAY](),  or  [gerbers](../../releases/latest)  
BOM from [DigiKey](),  or  [BOM.csv]()  
-->

## Dual-Bank - SOP

![](../../raw/main/TANDY_200_Dual_RAM.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM_top.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM_bottom.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM.svg)  

<!-- PCB from [OSHPark](),  or  [PCBWAY](),  or  [gerbers](../../releases/latest/)  -->  
BOM from [DigiKey](https://www.digikey.com/short/25v45c90),  or  [TANDY_200_Dual_RAM.BOM.csv](TANDY_200_Dual_RAM.BOM.csv)  

## Dual-Bank - TSOP

![](../../raw/main/TANDY_200_Dual_RAM_tsop.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM_tsop_top.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM_tsop_bottom.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM_tsop.svg)  

Supports both 14mm and 20mm tsop-32.
PCB from <!-- [OSHPark](),  or  -->[PCBWAY](https://www.pcbway.com/project/shareproject/TANDY_200_RAM_48K_TSOP_57aa6fd6.html),  or  [gerbers](../../releases/latest) -->  
BOM from [DigiKey](https://www.digikey.com/short/bvrwht5d),  or  [TANDY_200_Dual_RAM_tsop.BOM.csv](TANDY_200_Dual_RAM_tsop.BOM.csv)  

<!--
## Dual-Bank THT DIP

![](../../raw/main/TANDY_200_Dual_RAM_tht.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM_tht_top.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM_tht_bottom.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM_tht.svg)  

PCB from [OSHPark](),  or  [PCBWAY](),  or  [gerbers](../../releases/latest)  
BOM from [DigiKey](),  or  [BOM.csv]()  
-->

## Original TANDY 26-3866 24K Option RAM for reference  
Re-drawn in KiCAD from the info in the service manual.  
This is what any alternative must replicate or emulate.  
The internal 24K bank is also the same (without the ceramic DIP carrier module).

![](../../raw/main/TANDY_26-3866.svg)
![](../../raw/main/TANDY_26-3866_top.jpg)
![](../../raw/main/TANDY_26-3866_bottom.jpg)

## Misc Notes  

The BOM includes Mill-Max 3121 machined brass micro pins, but there are a couple of other ways to make properly thin [PCB DIP legs](https://gist.github.com/bkw777/52d85d89eeff8445cc667685d05ea94d) .

The DIP row spacing is actually 725 mils not 700. This makes it a little bit annoying to solder the legs because the rows don't line up exactly with the 100-mil rows in a breadboard, but the odd spacing is deliberate not an arror.  

Suggestion for soldering the pins:  
Use some generic single-row female pin headers in a breadboard to hold the pins in alignment for soldering.  
Take 2 rows of 28 pins of single-row female pin headers and insert them into a breadboard 600 mils apart like for a normal 600 mil dip.  
One row is for holding pins, the other will not line up with the other row of holes, it is just for the pcb to rest on to hold up the other side of the pcb so it's level.  
Dip the post end of a pin in tacky solder paste, and insert into a hole in the pcb. Let the flux hold the pin in the pcb, don't worry about how loose the fit is and how the pin isn't held perpendicular. Repeat for all 14 pins of ONE row of the pcb.
Insert the row of pins into one of the female sockets on the breadboard, laying the pcb across the top of the other socket. Solder the pins from the top.  
Extract the pcb from the socket and repeat for the other row of 14 pins. Finally do the single pin.  
The pins are very fragile. Be careful not to let them get bent, because they don't bend much before they break, and they bend easily, so just be real careful not to let anything catch on them and be careful when extracting from sockets not to allow the pcb to tip and angle.

