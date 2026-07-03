# log #1: laying out the schematic

so i want this to have as small a footprint as possible for it to be maximally portable. this session was mostly about trying to figure out how to do that. 

![image](https://cdn.hackclub.com/019eee4e-b718-77f2-b9ab-44e623745859/image.png)
this seems to be what's minimally viable. well i need to add a 3v3 buck boost. 

![image](https://cdn.hackclub.com/019eee4f-6873-74cd-a523-0bee1973ecd0/image.png)
![image](https://cdn.hackclub.com/019eee4f-c0c8-75e5-948c-eec89705aa90/image.png)

i don't think it can stay this small ! but hoping

# log #2: changed footprint

![image](https://cdn.hackclub.com/019f0cde-3534-7b3c-8ce7-c83beab2b46b/image.png)

mostly just figuring out how to further compact this. i've decided on two thumbwheel rotary encoders instead of the original controls. they have the advantage of being surface mount, so i can fit components on the back. 

i might swap out the OLED for a 1.5" instead. i feel like this one might actually be too small, and the pin placement is genuinely inconvenient.

# log #3: worked on schematic and changed footprint again.

![image](https://cdn.hackclub.com/019f0f83-4338-7fea-a633-bbbe27b83368/image.png)

finished laying out the schematic! only thing left to do is to check the esp32-wroom-32 datasheet and figure out how to connect all the gpios. 

![image](https://cdn.hackclub.com/019f0f84-9c49-7262-a818-449e77a2f605/image.png)

this seems to be the final arrangement for the pcb. i'm fairly happy with how compact it's going to be. i'm going to add a few mounting holes to the pcb. i will be making a 3d printed enclosure but i'm planning for the final thing to have a case made of acrylic panels

# log #4: finding rotary switches that actually work

so my previous rotary switches did not work! they don't have a push switch, which is fairly necessary. so back to the trenches (lcsc)

![image](https://cdn.hackclub.com/019f12a2-e3ac-7dd5-9f02-e23394a9514d/image.png)

this part seems to work. 

![image](https://cdn.hackclub.com/019f12a2-53ae-7e0b-a3e9-6d704818746c/image.png)

i made a kicad symbol. 

![image](https://cdn.hackclub.com/019f12a5-2095-72e4-a70c-ac4bbcc5bcd1/image.png)

and a footprint!

![image](https://cdn.hackclub.com/019f12a5-93dc-7ad7-ad2e-0df678a4241e/image.png)

now i have this as the hopefully final arrangement

# log #5:  routing ESP32-WROOM-32E pins


