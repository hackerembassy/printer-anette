# Playing music with Anette
## How
- Open the site https://www.ultimatesolver.com/en/midi2gcode
- Upload a midi file and press Analyze. 
- Select 2 axes (z axis is problematic to use)
- We have tried Steps per mm as 32 on both 1st and 2nd axis
- Work area max 200
- Set Agree checkbox and Create G-code
- Replace G01 with G1 
- Delete all commands before the first g1 and after the last g1
- Insert commands below to the beginning
G28 XY
G90
- Save as .gcode and send to printer or copy gcode and paste into console in fluidd