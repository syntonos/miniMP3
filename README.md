# miniMP3
![image](./Assets/apart_top.png)
![image](./Assets/cad.png)

## About
A compact music player. 59.3 x 32 x 27 (mm), or around 2 x 1 x 1 inches, around half the size of an earpod case. Bluetooth and 3.5mm jack compatible. mp3, wav, and flac compatible. 5-band EQ, and more functions when the firmware updates. 

Really more of a fun PCB tiling exercise than anything. 

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

(Firmware currently in testing, will be in release notes when fully finished.)

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

## BOM (List)
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
- 1x 1000 mAh 102050 LiPo 

## BOM (Expanded)

- 1x PCB 
    - $118.54 + variable shipping + tariffs ([JLCPCB](jlcpcb.com)) 
- 1x SD Card Module
    - $2.22 ([Aliexpress](https://www.aliexpress.us/item/3256810092532833.html?spm=a2g0o.detail.pcDetailBottomMoreOtherSeller.20.4a9c4827KucpTU&gps-id=pcDetailBottomMoreOtherSeller&scm=1007.40050.354490.0&scm_id=1007.40050.354490.0&scm-url=1007.40050.354490.0&pvid=48008c8b-14f3-4bec-a2a7-858a0f19360f&_t=gps-id%3ApcDetailBottomMoreOtherSeller%2Cscm-url%3A1007.40050.354490.0%2Cpvid%3A48008c8b-14f3-4bec-a2a7-858a0f19360f%2Ctpp_buckets%3A668%232846%238113%231998&pdp_ext_f=%7B%22order%22%3A%22502%22%2C%22eval%22%3A%221%22%2C%22sceneId%22%3A%2230050%22%2C%22fromPage%22%3A%22recommend%22%7D&pdp_npi=6%40dis%21USD%212.22%211.11%21%21%2114.87%217.43%21%402101ea8f17861045160773710e0f03%2112000051759912175%21rec%21US%21%21ABX%211%210%21n_tag%3A-29910%3Bd%3A32a296a5%3Bm03_new_user%3A-29895&utparam-url=scene%3ApcDetailBottomMoreOtherSeller%7Cquery_from%3A%7Cx_object_id%3A1005010278847585%7C_p_origin_prod%3A))
- 1x 1.54" OLED Display Module
    - $5.01 ([Aliexpress](https://www.aliexpress.us/item/3256807368835856.html?spm=a2g0o.productlist.main.2.7ff4pLmCpLmCYY&algo_pvid=83d0ca85-7b2b-4d53-a13f-587b26adf1f2&pdp_ext_f=%7B%22order%22%3A%22134%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005007555150608%7C_p_origin_prod%3A&gatewayAdapt=glo2usa4itemAdapt#nav-specification))
- 1x PJ320-D Jack
    - $1.29 ([Aliexpress](https://www.aliexpress.us/item/2255800475593383.html?spm=a2g0o.productlist.main.5.7a37165c4wg8d5&algo_pvid=d4e30b7e-5e70-4b23-910d-9174d61dcc92&algo_exp_id=d4e30b7e-5e70-4b23-910d-9174d61dcc92-4&pdp_ext_f=%7B%22order%22%3A%22280%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21USD%211.29%210.99%21%21%211.29%210.99%21%402103094f17861049205907001e0e9b%2110000005519439913%21sea%21US%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3A3c5a3cb9%3Bm03_new_user%3A-29895%3BpisId%3A5000000210792324&curPageLogUid=lgUlXJGyB23m&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A4000661908135%7C_p_origin_prod%3A))
- 1x 4mmx4mm Push Switch
    - $4.70 ([Aliexpress](https://www.aliexpress.us/item/3256812363662693.html?spm=a2g0o.productlist.main.2.9f2afc6hfc6hgc&algo_pvid=ce5fb20e-1501-429b-bf35-2a32c0622efe&algo_exp_id=ce5fb20e-1501-429b-bf35-2a32c0622efe-1&pdp_ext_f=%7B%22order%22%3A%2215%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21USD%214.37%210.99%21%21%2129.36%216.66%21%402101e81117861057478814823e0e95%2112000058673759179%21sea%21US%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Abf24fdfb%3Bm03_new_user%3A-29895%3BpisId%3A5000000210792324&curPageLogUid=IB3bPPIi35gd&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005012549977445%7C_p_origin_prod%3A))
- 1x Sliding Power Switch
    - $3.18 ([Aliexpress](https://www.aliexpress.us/item/3256809238668355.html?spm=a2g0o.productlist.main.5.73ee3b50pr4ynz&algo_pvid=e15007de-cf57-41c3-bf81-98b1eed3ce96&algo_exp_id=e15007de-cf57-41c3-bf81-98b1eed3ce96-4&pdp_ext_f=%7B%22order%22%3A%2213%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21USD%213.18%210.99%21%21%213.18%210.99%21%40210328c017861059128021204e0db7%2112000049056299795%21sea%21US%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Abf24fdfb%3Bm03_new_user%3A-29895%3BpisId%3A5000000210792324&curPageLogUid=Vd35dkvN3lM2&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005009424983107%7C_p_origin_prod%3A))
- 2x Rotary Switch XUNPU
    - $4.83 ([Aliexpress](https://www.aliexpress.us/item/3256806896633044.html?spm=a2g0o.productlist.main.3.451215b2cE25ay&algo_pvid=7b264ad5-283b-484e-a52d-678e4ecfdac7&algo_exp_id=7b264ad5-283b-484e-a52d-678e4ecfdac7-2&pdp_ext_f=%7B%22order%22%3A%224%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21USD%214.83%210.99%21%21%2132.44%216.69%21%4021032c8d17861060857714961e4bdc%2112000039340479749%21sea%21US%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Abf24fdfb%3Bm03_new_user%3A-29895%3BpisId%3A5000000210792324&curPageLogUid=fBZcXmDou4el&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005007082947796%7C_p_origin_prod%3A))
- 2x M2 Heatset 3.5D 4.5H
    - $5.54 ([Aliexpress](https://www.aliexpress.us/item/3256806611972099.html?spm=a2g0o.productlist.main.4.258012795phy4k&aem_p4p_detail=202607030045232645786979741340002311817&algo_pvid=48fed4a3-d046-4065-9380-83ce295cbbc4&algo_exp_id=48fed4a3-d046-4065-9380-83ce295cbbc4-3&pdp_ext_f=%7B%22order%22%3A%223867%22%2C%22spu_best_type%22%3A%22price%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21TWD%21237.09%21189.65%21%21%2148.63%2138.90%21%400b1bf20a17830647230337253ec923%2112000038340344511%21sea%21TW%217611495303%21ABX%211%210%21n_tag%3A-29910%3Bd%3A8099445a%3Bm03_new_user%3A-29895&curPageLogUid=pmRS9OHkPpDI&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005006798286851%7C_p_origin_prod%3A&search_p4p_id=202607030045232645786979741340002311817_1&gatewayAdapt=glo2usa4itemAdapt))
- 2x M2 Heatset 3.5D 18H
    - $8.00 ([Aliexpress](https://www.aliexpress.us/item/3256806611972099.html?spm=a2g0o.productlist.main.4.258012795phy4k&aem_p4p_detail=202607030045232645786979741340002311817&algo_pvid=48fed4a3-d046-4065-9380-83ce295cbbc4&algo_exp_id=48fed4a3-d046-4065-9380-83ce295cbbc4-3&pdp_ext_f=%7B%22order%22%3A%223867%22%2C%22spu_best_type%22%3A%22price%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21TWD%21237.09%21189.65%21%21%2148.63%2138.90%21%400b1bf20a17830647230337253ec923%2112000038340344511%21sea%21TW%217611495303%21ABX%211%210%21n_tag%3A-29910%3Bd%3A8099445a%3Bm03_new_user%3A-29895&curPageLogUid=pmRS9OHkPpDI&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005006798286851%7C_p_origin_prod%3A&search_p4p_id=202607030045232645786979741340002311817_1&gatewayAdapt=glo2usa4itemAdapt))
- 2x M2 Screw 20H 
    - $3.86 ([Aliexpress](https://www.aliexpress.us/item/3256801577619187.html?spm=a2g0o.productlist.main.16.b7047f20Gvg4hM&aem_p4p_detail=202607030206362312824948692800002217653&algo_pvid=bb9c3ac2-a29e-44a3-bcaa-9b5e252f7fca&algo_exp_id=bb9c3ac2-a29e-44a3-bcaa-9b5e252f7fca-15&pdp_ext_f=%7B%22order%22%3A%222238%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21TWD%2122.81%2121.82%21%21%210.69%210.66%21%402140f54217830695966233289eecdc%2112000017472413080%21sea%21TW%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3Aae87e3a4%3Bm03_new_user%3A-29895&curPageLogUid=MdcYnRM4XBCg&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005001763933939%7C_p_origin_prod%3A&search_p4p_id=202607030206362312824948692800002217653_4&gatewayAdapt=glo2usa4itemAdapt))
- 1x 1000 mAh 102050 LiPo 
    - $9.54 ([Aliexpress](https://www.aliexpress.us/item/3256812631640799.html?spm=a2g0o.productlist.main.14.2795V6V3V6V3Ci&algo_pvid=47981000-d41c-4af4-80eb-60457e2c9e29&algo_exp_id=47981000-d41c-4af4-80eb-60457e2c9e29-13&pdp_ext_f=%7B%22order%22%3A%22-1%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21USD%219.57%214.69%21%21%2164.21%2131.46%21%402101e7a317861054336146098e0cfe%2112000059462118130%21sea%21US%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3A3c5a3cb9%3Bm03_new_user%3A-29895&curPageLogUid=SGpK83WOjezf&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005012817955551%7C_p_origin_prod%3A))


