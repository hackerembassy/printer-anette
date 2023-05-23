# General Tips
1. Do not leave working printer unattended
2. Ask other people in chat which types of filament you are allowed to use
3. ~~Avoid as much as you can applying vertical force on the extruder carriage as it may misalign Z threaded rods making any saved bed meshes in the firmware invalid~~ 
   ~~* That's why "cold pull" is not recommended and it's also not needed with this machine. Just heat up the nozzle, retract the filament and cut the deformed end.~~
   ~~* Cyan **Align markers** that look like arrows are installed on each Z rod - they can help to detect misaligment~~  

   ~~I know it sucks that this printer doesn't have automatic Z alignment~~

   Everything above is deprecated. Thanks to someone overly enthuziastic, Anette now has automatic Z-tilt adjust at the start of every print.
   You can forget about it, just use @keimoger's SuperSlicer configs!
4. Don't let the hot nozzle stay still for more than few seconds near the heatbed to avoid damaging the print surface film
5. Regularly clean the nozzle cleaning brush installed on the side of the bed. You can use [tweezers](./tools/tweezers_scraper_cutter.jpg)
6. Bed warps greatly depending on temperature and it is compensated by ABL. The firmware of the printer holds in memory the bed mesh measurements for common temperatures like 60C or 70C. And bed mesh should be automatically loaded during start g-code in your slicer. Example in cura:  
    ```
    BED_MESH_PROFILE LOAD={material_bed_temperature_layer_0}
    ```  
    For any new heatbed temperature you need to preheat bed to the desired temperature, make sure Z rods are not misaligned and do the bed mesh measurement like this example for 69C:
    ```
    M190 S69  
    G28  
    BED_MESH_CALIBRATE PROFILE=69  
    BED_MESH_PROFILE SAVE=69  
    SAVE_CONFIG
    ```
7. To swap [nozzles](./tools/nozzles.jpg):
    1. ~~You can temporary remove fan duct for convenience. Simply pull it down while holding the extruder carriage~~ No you can not. Just work around it.
    2. Remove silicone sock from the heat block via [tweezers](./tools/tweezers_scraper_cutter.jpg)
    3. Follow the official [E3D instruction](https://wiki.e3d-online.com/E3D_Nozzles#Changing_Nozzles) for swapping nozzles (preheating to 285C, etc)   
       Note: the step "Re-tighten the heat-break into the HeatSink." is not possible with this printer, just skip
    4. Use [convenient tools](./tools/nozzle_tools.jpg) for unscrewing and screwing the nozzles

# Heat Bed
[Wham Bam flexible build system with PEX surface film](https://whambamsystems.com/flexible-build-system) is installed on the printer.  
You can see the [short overview and usage video](https://www.youtube.com/watch?v=NMJ_P_5z53c).

## Heat bed tips:
1. Try not to touch the top print surface with your hands, because you are a human and human's hands are usually oily, and oils generally prevent parts from sticking to the print surface. 
   If you do though, you will need to wipe the print surface with clean alcohol
2. Always cool down the flexible build plate and then bend it on two axes before taking off printed parts from it. Very thin parts still might not come off - they can be gently scraped with the [scraper](./tools/tweezers_scraper_cutter.jpg). If you are unsure, this [video](https://youtu.be/JZpZunV6Zx0?list=PLSlhFLYCaWuLzogLnofDmP1dMnFNhA0hr) shows how, though try to avoid excessive touching of the top print surface like the instructor on the video
3. It's recommended not to use glue. The PEX print surface film and ABL were installed partly to avoid using the glue altogether and it worked sufficiently for the common types of filament. Using glue can also lead to potential problems such as:
    1. Parts not releasing easily from the cold build plate due to glue and damaging the PEX print surface
    2. Parts actually sticking less to the print surface while printing. Properly maintained PEX surface is sufficient and probably has more adhesion than when combined with glue 
    3. Glue can mess with the established workflow of other people which do not use glue to print

   Instead use proper print parameters/conditions, keep the bed oil-free and [do regular refurbishing](https://www.youtube.com/watch?v=JZs8gvKTf88&list=PLSlhFLYCaWuLzogLnofDmP1dMnFNhA0hr&index=4) of the print bed surface ([steel wool](./tools/steel_wool.jpg) is available in the space). Ask other people for the proper print parameters for specific filaments - mainly for initial and subsequent heatbed temperatures, first layer height, fan part cooling amount and when it starts, nozzle temperatures and if the chamber should be open or closed.
