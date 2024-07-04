Hi! Thanks for download My Custom Firmware for Wanhao Duplicator i3!
Before you start, i need to explain some topics.

TOPIC 1:
This firmware is based on Creality Ender 3 printer. So, you need to create a custom profile on your preference slicer software (Ultimaker Cura, Slic3r, Prusa Slicer or Orca Slicer).

On Ultimaker Cura, you'll need to add a Creality Ender 3 printer and make some changes.
![image](https://github.com/Noobli95/ProjectNugget/assets/123615009/f14cc196-b98b-4482-8c64-0d91292b7489)

Start G-Code:

G21 ;metric values
 G90 ;absolute positioning
 M82 ;set extruder to absolute mode
 M107 ;start with the fan off
 G28 X0 Y0 ;move X/Y to min endstops
 G28 Z0 ;move Z to min endstops
 G1 Z15.0 F{speed_travel} ;move the platform down 15mm
 G92 E0 ;zero the extruded length
 G1 F200 E6 ;extrude 6 mm of feed stock
 G92 E0 ;zero the extruded length again
 G1 F{speed_travel} 
 ;Put printing message on LCD screen
 M117 Printing...

 End G-Code:

 M104 S0 ;extruder heater off 
 G91 ;relative positioning
 G1 E-1 F300  ;retract the filament a bit before lifting the nozzle, to release some of the pressure
 G1 Z+0.5 E-5 X-20 Y-20 F{speed_travel} ;move Z up a bit and retract filament even more
 G28 X0 Y0 ;move X/Y to min endstops, so the head is out of the way
 M84 ;steppers off
 G90 ;absolute positioning

Travel Configuration:

![image](https://github.com/Noobli95/ProjectNugget/assets/123615009/bcd6ee08-66d4-4c1b-bab0-7610ac6322b1)

Unluckily, in the lats versions of Cura (5.6.0 and 5.7.2) we have a little problem. The problem is that the print had layer failures. So, I'm trying to find a new profile to test this. I believe a custom profile in your favorite software will do the trick.

When I find the solution I'll post it.

TOPIC 2:

We have 2 files here.

Firmware.bin

Marlin for Wanhao Duplicator i3.zip folder

If you just want update the new firmware on your board, put the Firmware.bin on your sd card, connect in the 3d printer and turn it on. After a few seconds, the firmware has updated on your board.

BUT, if you want make some changes, the Zip folder has all the configuration files.

DO IT BY OWN YOUR RISK. I DON'T HAVE ANY RESPONSABILITY IF YOU COMMIT A CRUCIAL MISTAKE.

Why am I saying this? It's because we have a new library updates on vs code, platformIO, auto biuld marlin and Marlin firmware. For this reason, it's normal have a crashes and errors.
You can use this code as a example to make your own  firmware too.

Finally, I need to express all my gratefull for all my friends who helped me with a good words or money. Razgriz, Otávio, Fábio Pinheiro, Ana Clara Aravecchia (she's the best!), Pablo, Gabriel, LVírus, my Instagram/Youtube Followers, etc.
Without you guys, that's not could be possible.

Thank you to come here and see my repository. Have fun and awsome prints!
Ah, I remember something. If my English isn't good to understand, sorry. I'm Brazillian, trying to learn the language.

Kisses,
Noobli_
