---
layout: page
title: Notes for 3D printing
---

## Structure Design

1) Design the 3D structure via the software [Solidworks](https://www.solidworks.com/sw/support/downloads.htm) (not free) or [Onshape](https://www.onshape.com/) (free, online)
2) Design the mold within the part skeleton, then set the output file format as ‘stl’, the size of stl mold is in mm size.

---
## Mold printing
### Equipments:

(i) Hardware: Wanhao Duplicator 4S, with the filament material of ABS or PLA
(ii) Software: 1) Java; 2) Python; 3) ReplicatorG/ SIMPLIFY 3D(Optional);
(iii) [Environment setting and software installation](http://www.wanhao3dprinter.com/Down/ShowArticle.asp?ArticleID=18) 
	
### Operations  
1. connect the computer with the printer via USB connector, then configure the port and driver for the 3D printer, then click “Connect” --> successful connection;  
2. slice the file ('stl' model) for gcode file (Parameter adjustment: fill with 100%; layer thickness: 0.2mm; speed: 35mm/s; temperature: 230 degrees or 220 degrees); then generate the gcode file for the current model (equal to the slice function), and generate .x3g file into the SD card --> file generation for printing;
    Alternatively, we can also print the mold directly from the PC control. 
3. printer operations
    * level the building plate: 1) select the option for leveling; 2) change the position of the nozzle by moving the nozzle base; 3) change the height of the nozzle in the four corners (where the 3d tape is covered.) with adjustment of the four knobs under the plate; ensure the distance between the nozzle and plate is around the height of A4 paper;
    * load the filament: 1) wait until the nozzle has reached the temperature about 220 degrees for printing; 2) gradually fill the filament into the nozzle through the top hole of the nozzle base. 3) stop filling until the filament has come out from the nozzle.
    * Select the file for printing: 1) preheat and wait;

**Tips or notices:**
1) After the first layer is printed, screw down the nut a little bit to bring it closer together; --(aim for the better printing mold);
2) In order to print better mold, PLA is better than ABS material during experiments.

**Common problems:**
1. *Edge warping?*  
  Solution:  
  * PLA can have better performance than ABS, although the quantity printed is lower.
  * Exterior support is necessary
  * Large base can help prevent the edge warping. In order to take it off easily, the base should not be very thick, 1mm is enough.
2. *Printing discontinuity*  
  Solution:  
  * Unload the filament and reload it, in order to make sure the wire is good for printing.
  * Set the printing width suitable.
