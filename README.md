# miniMP3
![image](./Assets/apart_top.png)
![image](./Assets/cad.png)

## About
A compact music player. 59.3 x 32 x 27 (mm). Bluetooth and 3.5mm jack compatible. mp3, wav, and flac compatible. 5-band EQ, and more functions when the firmware updates. 

## Idea
I wanted a little mp3 player that was small enough that I could just toss into my shirt pocket or keep it on a necklace. I don't want to be tied so much to my phone, and this seems like a reasonable first step to move a function off. There are also a couple old cds and etc. that I'd like to download.

## Assembly
Solder on:
- the display module
    - Make sure the alignment is correct! Orient the screen upwards and covering the "blank" side of the PCB. Check the pins to make sure they match. Solder in the pins. Clip off the excess length.
    ![image](./Assets/3d_front.png)
- the SD card module
    - Orient the slot facing outwards. Make sure the pins match on the module and the PCB. Make sure the length of the header pin is appropriate (5mm). Solder in the pins. Clip off the excess length. 
    ![image](./Assets/3d_back.png)
    (throughhole slots below where the module is pictured)
- the boot switch (4x4 push switch)
    - Surface mount on the back. Make sure the orientation is correct (longer side matches the longer side, the shorter side matches the shorter side), then use solder paste and carefully place.
    ![image](./Assets/3d_back.png)
    (exposed solder pads next to the ESP32-WROOM-32)
- the power switch (toggle switch)
    - Orient so that the pins align (no specific direction), then solder in the throughhole pins.
    ![image](./Assets/3d_front.png)
    (bottom right corner)
- the rotary switches
    - Next to the OLED display module on the same side. Use solder paste to adhere the switches through a surface mount.
    ![image](./Assets/3d_front.png)
    (right side, two switches)

Plug in the LiPo Battery (JST-PH 2.0mm).

Insert the heat-sets into the two slots above and below. 
![image](./Assets/apart_top.png)
![image](./Assets/apart_bottom.png)

Fasten in the M2 screw on the bottom. 
![image](./Assets/cad_bottom.png)

## Firmware

Flash firmware through USB-C, and a platform like Arduino IDE. Hold the boot button, flick the power switch on and off, select the right USB connection, and upload the firmware.

## PCB
### Layer 1 - Signal
![image](./Assets/pcb_layer1.png)
### Layer 2 - GND
![image](./Assets/pcb_layer2.png)
### Layer 3 - Power
![image](./Assets/pcb_layer3.png)
### Layer 4 - Signal
![image](./Assets/pcb_layer4.png)
### 3D Model Front
![image](./Assets/3d_front.png)
### 3D Model Back
![image](./Assets/3d_back.png)
## Schematic
![image](./Assets/schematic.png) 
## CAD
![image](./Assets/cad.png)
![image](./Assets/cad_back.png)
![image](./Assets/apart_top.png)
![image](./Assets/apart_bottom.png)

## BOM  
- 1x PCB 
- 1x SD Card Module
- 1x 1.54" OLED Display Module
- 1x PJ320-D Jack
- 1x 4mmx4mm Push Switch
- 1x Sliding Power Switch
- 2x Rotary Switch XUNPU
- 2x M2 Heatset 3.5D 4.5H
- 2x M2 Heatset 3.5D 18H
- 2x M2 Screw 20H 