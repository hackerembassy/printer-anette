The Anette printer is based on Anet A6

## Non-printable changes from Anet A6

1. PSU: Temporarily Meanwell 24V 600W. Will be changed to two different PSU's in the near future. 
2. Motherboard: SKR 1.4 Turbo  
   *Quirk: pins for second extruder heater are used instead for a heatsink fan on the on the first (and only) extruder, so the heatsink fan can have PWM and turn on only when needed.*  
3. Installed drivers: All TMC 2209 
4. Firmware: **Klipper** ✨ (Marlin compatible)
5. Build volume: 220x220x170 *(170mm height can be safely upped to 190mm in the firmware, I think)*
6. Extruder:  
    1. Trianglelab BMG dual geared extruder clone  
    2. Extruder motor: 1.8deg NEMA17 23MM (pancake)  
    3. Auto bed leveling sensor: original **BLTouch 3.1** ✨
    4. Hotend: Trianglelab E3D V6 hotend clone  
       1. Heat break: Trianglelab GRADE5 V6 titanium alloy heat break (**Fullmetal** ✨)  
       2. Heater cartridge: Trianglelab 6*20MM 12V / 24V 50W  
       3. Silicone sock *(please take it off when heating nozzle >250C)*
       4. Trianglelab T-D500 Temperature Sensor 500℃ *(provides unprecise measurements with temps below 100C, but it's okay)* 
       5. Various [assortment of V6 nozzles](./tools/nozzles.jpg) 
7. Heat Bed: 
   1. 200x200mmm silicone heater pad 200W *(not sure)*, works in parallel with the original 220x220x3 aluminium 120W heatbed
   2. **Wham Bam Flexible Build System** ✨ [info](https://whambamsystems.com/flexible-build-system) and [short overview](https://www.youtube.com/watch?v=NMJ_P_5z53c) *(spare parts in the printer supplies box)*
      1. Wham Bam Flexi Magnetic Base (high temp-resistant up to 150 degrees with high temp 3M adhesive)
      2. Wham Bam Flexi Build Plate (spring steel)
      3. PEX Build Surface film on build plate

## Printable changes from Anet A6
Lots of them. If some 3D printed part breaks, you can ask @ubershy, and she will provide models (or links to models) or even source files.

## See also

[Anette important info and tips](./anette_important_info_and_tips.md)
