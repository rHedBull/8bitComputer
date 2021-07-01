# 8bitCPU
self build 8bit CPU on a breadboard using only logic gates, some active circuit parts, resistors, capacitors and transistors

## used resources
### [Ben Eater](https://github.com/beneater)
special thanks to this guy who put a lot of work into his repository and youtube video series where he explains anything you need to know to rebuild this CPU build  
check out his works:  
https://eater.net/  
https://www.youtube.com/playlist?list=PLowKtXNTBypGqImE405J2565dvjafglHU  
if possible please support him on [Patreon](https://www.patreon.com/beneater)  

### [ThomasBuchinger](https://gist.github.com/ThomasBuchinger)
he adapted Ben's partlist for the European vendor [Reichelt](https://www.reichelt.de/) since some parts are hard to find in Europe
you can find it [here](https://gist.github.com/ThomasBuchinger/92f848d017fa94d7c7886f224a20c198)

## Software
the schematics you can find in this repo are all created using KiCad. Ben Eater did create those already, but since my parts are slightly different than his,   
I redesigned the circuits myself following his example. I can only recommend to try it yourself since one can learn a lot and maybe eventually even solder the CPU on a PCB board using the in KiCad generated gerber files.   
And the 3D animated models are beautiful!!!   


## Clock Module
### parts
- chip_1 = TLC556CN , timer
- chip_2 = SN74LS08N, and gates   
- chip_3 = SN74LS04N, inverter   
- chip_4 = SN74LS32N, or gates   
   
![clockModule_annotated](https://user-images.githubusercontent.com/65466619/124142808-d93e1a80-da8a-11eb-98af-4ac568ef1955.jpg)

### function
this combination of a mono- and astable timer results in a bistable timer. While the monostable timer is mainly used to let the computer run step by step which helps debugging, the astable timer [ClockModule_schematic.pdf](https://github.com/rHedBull/8bitComputer/files/6749040/ClockModule_schematic.pdf)
generates a continuous stream of equally logic high voltage, in equal time intervalls, to ensure the different computer parts run in concurency and the instructions are timed correctly.
