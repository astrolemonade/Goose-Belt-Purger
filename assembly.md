# Goose Belt Purger assembly

## Preparation steps
a) Identify, if your board has protective flyback diodes. You can check the comprehensive list [here](board_list.md),. If not or you are in doubt, you will have to add it yourself to motor terminals. At this moment there are no known boards with RC snubber integrated, so expect to add snubber either way.
  
![](/Assets/Schottky-Octopus.jpg)  
_Example of BTT Octopus with Schottky diode on board_  
  
b) Install heatset inserts into **GBP_Idler** (1x) and **GBP_Deflector** (2x). If you want to use HSI variant arm, install insert also to **GBP_Arm_HSI** (1x). If you plan to use an AT style or Klicky style mount, you can also install inserts in those parts.  
c) Remove integrated support of **GBP_Deflector_(long/short)**. Grab the small bridging element in the middle with small pliers and remove it with twisting motion. It should easily and cleanly detach.   

## Assembly steps
1. _(Skip this step if you are using MicroFlip board. Instead just solder MicroFlip to your motor)_  
   Solder wires to the motor. If your board does not have sufficient protection, solder a schottky flyback diode and/or RC snubber to the motor terminals together with wires  
  **_1a._** Correct polarity of the motor is needed. Output shaft of the motor should be turning CCW (or CW if you printed mirrored version). If you can, test the polarity beforehand. In case the motor spins other way, switch the wires. If you are not adding flyback diode, you can reverse them later on in connector. If you are adding flyback, you will need to revert them directly on the motor.  
  **_1b._** Schottky flyback diode has a set polarity and you need to solder its cathode to the motor terminal where positive voltage (+) wire is connected. Cathode is usually marked with a colour stripe. Other end of diode shall go directly to the other motor terminal. Double check the polarity, because doing this wrong may overload and damage your control board.  
  **_1c._** RC snubber is formed of a capacitor and a resistor. One leg of each component shall be soldered together (in series) and other legs to the motor terminals (one resistor leg to one motor terminal, one capacitor leg to other motor terminal). RC snubber does not have set polarity and it does not matter which way around do you solder it.  
   
![](/Assets/snubber.jpg) ![](/Assets/schematic.jpg)   
_Example of snubber; schematic of snubber with diode_
   
2. Insert the motor to a slot in **GBP_Frame**. It should fit tightly, but not deform the part. Depending on your gearbox configuration you may have some play in axial direction. Try to place your motor in such a way, that the face with output shaft  is as flush with frame as possible.  
3. Clamp the motor from top with **GBP_Motor_cover**, push through 2x M3x20 FHCS screws, add **GBP_Deflector** to bottom and screw it together.  
4. Insert two of the bearings and one magnet into **GBP_Arm**. Bearings should be inserted from flat side (one with logo on it). Polarity of the magnet does not matter. If it is too loose, you may fix it with a drop of glue, but this should generally not be needed. Magnets act as a spring pulling arm away from mount and as such are being pushed into a pocket.  
5. Put M3x30 screw through remaining bearing, add **GBP_Bearing_spacer** on screw, then push the screw through arm opening and second bearing. Set the third bearing flush into hole and screw on **GBP_Idler**. Idler has to be fully tightened against bearing, but has to move freely. Do not overtighten, as it can damage your bearings.    
6. Put other magnet into Frame. Make sure to orient it in such a way, that it will repulse the magnet in Arm, when they are faced aginst each other.  
7. Slide the arm on the motor shaft, through remaining bearing. Make sure the arm can freely move up and down and that it gets pushed away from frame by magnets. Place nyloc nut to slot on top of arm _(does not apply to HSI variant)_ Secure the arm to mount with M3x20 SHCS _(M3x16 SHCS for HSI variant)_ screw (do not fully tighten). 
8. Push the M3 nut into a slot in **GBP_Motor_pulley** and screw in a set screw. You may need to push a nut deep inside with a screwdriver.  _Some users skip this step. This is ok, but can lead to pulley wobbling_
9. Push the pulley into the motor shaft. Push it as far as you can, but leave a tiny gap so that the arm is free to move. Tighten the set screw against motor shaft.  
10. Take the wristband, turn it inside out, slightly stretch it by hand and slide it on the pulley and idler. You don't need to put it into any specific position, it will self align when switched on.  
11. Test the assembly. Verify, that the motor turns when powered, that the arm can move and that the belt keeps turning without slipping off the pulleys. 

## Mount assembly and integration into printer
Purger is designed to be compatible with ArmoredTurtle brush mount and regarding its assembly, you should refer to AT's wonderful manual located [**here**](https://www.armoredturtle.xyz/manual.html?manual=at_brush&step=1)  
Alternatively you can use Klicky style mount, which lacks ease of operation of the AT brush mount, but can be easier to adapt for certain printers.  
  
Purger itself is connected to its mount via a dovetail connection. If your printer is properly tuned, GBP should mate with the mount firmly, without any residual movement, but also without the need for excessive force to mate them. If they are too hard to assemble, you can gently sand the sides of the dovetail wedges on the frame. If they are too loose, you can shim the purger with a piece of paper or thin plastic placed between the purger's frame and the AT mount.    
  
Once everything is in place, you can adjust the purger to the right position using screws in the AT mount. If you use the basic (not offset) mount, the horizontal adjustment screw gets exposed when you remove the vertical adjustment screw and lift the arm up. Don't forget to put this screw back once you are done.  
You should adjust the Z position so that that there is a tiny gap between the nozzle and the wristband. You can use the M3x20 SHCS screw for fine adjustment.  
In case you choose the HSI arm variant, you should secure your screw with threadlocker or any other means. If you don't, your screw will eventually fall out due to vibrations.

For instructions on how to use the mounts for the most popular printers, see below
  
### Voron Trident
For the Voron Trident you can use either a basic mount (without brush), or an offset version with a brush. The offset version is recommended, because it shifts most of the purger away from the bed, preventing collisions with any other mods you might have. If you decide to use a basic mount, keep in mind you have to use customized parts designed for GBP, which are 10 mm shorter than the stock AT brush mount parts.  
You can place your mount and purger anywhere you want as long as you don't have a collision with your bed. The intended position is as far to the left (or to the right for the mirrored version) as possible.

![](/Assets/Trident/IMG20250901094611.jpg)
  
### Voron 2
For the Voron 2 you have to use a specifically designed offset mount, which clears the purger from colliding with the bed profiles. You are supposed to place the mount directly above the bed profile, so that the purger is on the left side of the printer (or right for the mirrored version) and the brush is in the center. In the case of the 250 mm frame size this will put the purger's end very close to the printer side panel, so you can consider using the "lite" version of the deflector, since the pellet guiding cover is effectively not needed.  
If you plan to use a waste bucket, make sure to mount it in your printer at this phase, to ensure you have enough clearance. 

![](/Assets/V2.4/image%20(5).jpg)

## Troubleshooting and FAQ
- My wristband shifts partially/fully off the pulleys towards bed - this is most likely due to bad tolerance of a bearings holding the idler and/or missing M3x16 SHCS screw. Some cheaper bearings allow the idler or arm to be pulled to the side by a band tension, which causes this shifting off. If you can, use a better bearing. Otherwise try using **GBP_Idler(+3,0)**  
- My wristband shifts too far in, towards motor - less common, could be due to arm being warped. Try using **GBP_Idler(+0)**



