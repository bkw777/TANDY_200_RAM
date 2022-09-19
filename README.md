# Option RAM module for TANDY 200

Replacements for TANDY 26-3866 24K SRAM module for TANDY 200 portable computer.

There are a few different options here. You pick whichever you need.  
* Single-bank with an SOP-28 chip - Drop-in replacement for the original 24K module, with a large-ish chip that's relatively easy to solder by hand. Use this if you already have one original ceramic module, and want to keep using it, and just want one more 24K module to fill the machine, and you prefer to use, or happen to already have an SOIC-28/SOP-28 version of the SRAM chip.
* ~Single-bank with a TSOP chip - Still TODO~
* Dual-bank with an SOP-32 chip - This provides the full 48 as 2 normal 24K modules all on one board. You plug a single one of these into OPTION RAM#2 slot. Uses an SOIC-32/SOP-32 chip for easier hand soldering.
* Dual-bank with a TSOP chip - Same as above but takes a TSOP-32 version of the SRAM chip. These are more common and more available, but also more of a challenge to solder by hand.

<!--
There are a few different designs available that all do the same thing but using different parts.

Some variants are single-bank like the original TANDY 26-3866 ceramic 24k module. These are drop-in replacements for the original modules, where one board = one bank = one Option RAM socket. You can have up to two boards installed in the machine.

Some variants are dual-bank, where one board supplies both Option RAM bank #1 and #2. You plug the one board into the Option RAM #2 socket, and this takes the place of two single-bank modules.

Some variants use different chip packages, so that you have options to use whatever types of chip you have, or can get, or can solder by hand.

There is also a [schematic of the original RAM bank](TANDY_26-3866.svg), re-drawn in KiCAD just for reference. There is no PCB for this, it's just for reference while designing new replacement modules to help ensure the replacement really still outwardly works the same as the original.
-->

See the [releases](../../releases) tab for gerber zips for manufacturing.  
There are no direct "order from OSHPark" or PCBWAY links for these yet because they are not yet verified.

## Single-Bank

![](../../raw/main/TANDY_200_RAM.jpg)  
![](../../raw/main/TANDY_200_RAM_top.jpg)  
![](../../raw/main/TANDY_200_RAM_bottom.jpg)  
![](../../raw/main/TANDY_200_RAM.svg)  

<!-- PCB from [OSHPark](),  or  [PCBWAY](),  or  [gerbers](../../releases/latest/)  -->
BOM from [DigiKey](https://www.digikey.com/short/f5hhwt4j),  or  [TANDY_200_RAM.BOM.csv](TANDY_200_RAM.BOM.csv)  

## Single-Bank, tsop

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

## Dual-Bank

![](../../raw/main/TANDY_200_Dual_RAM.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM_top.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM_bottom.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM.svg)  

<!-- PCB from [OSHPark](),  or  [PCBWAY](),  or  [gerbers](../../releases/latest/)  -->  
BOM from [DigiKey](https://www.digikey.com/short/25v45c90),  or  [TANDY_200_Dual_RAM.BOM.csv](TANDY_200_Dual_RAM.BOM.csv)  

## Dual-Bank - TSOP

![](../../raw/main/TANDY_200_Dual_RAM_tsop_14mm.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM_tsop_20mm.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM_tsop_top.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM_tsop_bottom.jpg)  
![](../../raw/main/TANDY_200_Dual_RAM_tsop.svg)  

<!-- PCB from [OSHPark](),  or  [PCBWAY](),  or  [gerbers](../../releases/latest) -->  
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

<!--
## Notes  

There are a couple of other ways to make [PCB DIP legs](https://gist.github.com/bkw777/52d85d89eeff8445cc667685d05ea94d) properly thin enough so that they don't harm sockets, instead of the relatively expensive machines brass Mill-Max 3121 pins in the BOM.

The DIP row spacing is actually 725 mils not 700. This makes it a little bit annoying to solder the legs because the rows don't line up exactly with a breadboard, but it's not an error.  
Use a set of single row socket headers in the breadboard, or even two sets, stacked to make a taller set. This allows the socket headers to spread apart a little and make it easier to hold the pins and pcb in place for soldering, without having the pins wind up angled inwards as badly.

-->
