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
a lot of cross referencing datasheets on this one. 

also apparently the esp32-wroom-32e does not have usb support ! so i need a new ic that converts the d+ d- differential pair to to uart transmission. 

![image](https://cdn.hackclub.com/019f1559-aefb-7677-ad9b-2343e78ab866/image.png)

i basically had just enough pins for this to work. 

![image](https://cdn.hackclub.com/019f16a4-c21d-7b5e-8a23-38216b1cb9a9/image.png)

put them into the firmware before i forget!

i also need two more switches. one tactile one for boot and one latching one for disconnecting the battery and turning on and off the mp3 player. 

![image](https://cdn.hackclub.com/019f16c8-032f-7860-8332-a6148c7e1220/image.png)

placed down most of the components... oh no. i can sort of already tell this is going to be a nightmare to wire. and i'm still going to have to find space for the two push switches...

# log #6: started wiring...
![image](https://cdn.hackclub.com/019f1928-75e4-7e64-a701-2b7d531e8231/image.png)

made a footprint for the boot switch and the power switch. 

![image](https://cdn.hackclub.com/019f1928-e4df-739f-b29b-9af3d2169b7d/image.png)
![image](https://cdn.hackclub.com/019f1929-2682-7394-a93d-d660c8405b65/image.png)

should be fine?? worst come to worst i have to use wires

![image](https://cdn.hackclub.com/019f1930-f8a3-7c78-94d0-f2bae9cf052e/image.png)

well this is a minor nightmare. i'll figure it out though
# log #7: wiring done !
![image](https://cdn.hackclub.com/019f1ca0-35cf-7a0b-af41-d20c5d883f6c/image.png)
well this seems like a bad idea. it was generally impossible to wire it any other way. unless i'm using like four vias per wiring. 

![image](https://cdn.hackclub.com/019f1cea-fa27-72dd-8f52-2de00e1b840d/image.png)
done???? oh god i'm not looking forward to doing design check. 

![image](https://cdn.hackclub.com/019f1cf7-9cae-7de5-be7a-609bf1a40f5b/image.png)
there used to be way more but c'est la vie. 

![image](https://cdn.hackclub.com/019f1d00-0455-7d56-8613-186b954cd983/image.png)
ok got rid of the errors. i'm probably just going to have to leave the warnings because they're just stuff about silkscreen getting clipped, and i can't help that because there's physically no space. 

well this was a horrifying board. if it works it will be a minor miracle. 
![image](https://cdn.hackclub.com/019f1d02-5ba0-73ae-ba8e-406a1ae9b6e9/image.png)
![image](https://cdn.hackclub.com/019f1d03-180e-7107-ad71-583e3e4c17d7/image.png)

# log #8: oh boy pcba is expensive (assembling bom)
![image](https://cdn.hackclub.com/019f1e01-1c32-7a3f-be98-87b6d14f1c6c/image.png)

so apparently the esp32-wroom-32e makes this a standard assembly... which is fun. i love that. so this is a little more expensive than i had hoped. but still cheaper than an mp3 player on the market 

![image](https://cdn.hackclub.com/019f1e00-fb3c-703c-b6b6-3a68adb1406c/image.png)

also apparently pick and place is a little bad when it comes to parts, and it doesn't really specify orientation, so minor wrangling had to happen. i've finally realized what the little silkscreen and the little dot on ics is for !

![image](https://cdn.hackclub.com/019f1e28-a482-7f39-ab2f-8a07e0589ee7/image.png)

again aliexpress is 66% shipping costs .... always fun. i do get why shipping to taiwan is so expensive in a political sense but really geographically this should be easy

and highkey i cannot get lipos that ship to taiwan in aliexpress. so i'm using amazon for this one part. 

![image](https://cdn.hackclub.com/019f1e40-5fa6-787e-8524-c8d4431a086e/image.png)

ig i'll do the programming and testing while it's attached to my computer? which isn't the worst thing in the world

# log #9: oops back to wiring
![image](https://cdn.hackclub.com/019f1efb-2855-7945-89d1-993fecc89bcd/image.png)

so as i was making the case, i did section analysis to get the ports and i realized that i've set the ports way too far in while making the pcb. so back to wiring... 

honestly this is probably good, because it give me the chance to fix some fixes now that i have the power of hindsight on my side. and a little more space now that the jacks are moved up

for example: 
![image](https://cdn.hackclub.com/019f1efd-034f-796c-b0ef-af2cc5c57267/image.png)
this absolute nightmare of a situation

![image](https://cdn.hackclub.com/019f1efd-6967-73ae-a297-976f02e5b11a/image.png)
actually not that bad with a little more space and planning. 

![image](https://cdn.hackclub.com/019f1f13-ac47-7106-9fed-ebdcff460dae/image.png)
got everything routed up this time without using any signals in the gnd or power plane

![image](https://cdn.hackclub.com/019f1f20-7004-7abe-a802-4f4db3b5dd60/image.png)

# log #10: cad done
![image](https://cdn.hackclub.com/019f274b-1a59-77e2-bc4f-03b3a3365c46/image.png)
it's donee. actually it's almost done. i just need to divide it into the top and bottom so that it actually makes sense. (the heatsets on either side of the pcb, combining around the ports so that things don't jam horribly)

![image](https://cdn.hackclub.com/019f2761-4407-783d-849f-00b07b6a852a/image.png)
ok so i had to get rid of all the fileting to start separating

![image](https://cdn.hackclub.com/019f277a-be4e-70ef-bfb4-c7d127e9a0b2/image.png)
this is how i want the split and now i just need to figure out how to do it. 

ok so apparently this is an absolute nightmare and there are no tools in fusion360 that will just do it. this was after two hours of research . 
- main problem: the dividing line looks different on different sides of the object. so a lot of the tools that requires the same height or the same plane don't work. plus i don't want to lose any volume so some other tools are off the table. 

![image](https://cdn.hackclub.com/019f27cb-5264-713b-ade4-9b26cefe73e0/image.png)
my awful solution is to split it into three parts first. then divide the above bit 
![image](https://cdn.hackclub.com/019f27ce-00a5-784e-953a-8b505e7309ca/image.png)
and recombine the pieces into a top and bottom half. 

top: ![image](https://cdn.hackclub.com/019f27cf-76d1-78e3-8438-6abd017a9126/image.png)
bottom: ![image](https://cdn.hackclub.com/019f27d1-396c-7688-bedd-3c3c209bd7ea/image.png)

![image](https://cdn.hackclub.com/019f27d3-9250-7c06-9ea2-e2dfc2734536/image.png)

![image](https://cdn.hackclub.com/019f27dc-3d59-7841-8732-f30a4a191bec/image.png)
done!

# log #11: more pcb + bom nonsense
![image](https://cdn.hackclub.com/019f27f2-b4ab-770d-8040-76fbe935eadf/image.png)

ok so i did change up the pcb a little bit so i need to do this process again. again pick and place is my sworn enemy. and i still don't know why esp32s are standard assembly

so shipping to the usa is scarily expensive, so i'm probably just going to ship to taiwan
![image](https://cdn.hackclub.com/019f27f7-c5e1-7f07-99e7-d1ef3f4436f5/image.png)

![image](https://cdn.hackclub.com/019f27fc-0e1d-78b6-b099-c7155b8db34f/image.png)
so shipping is still the bulk of the cost, which is always fun

# log #12: wrangling bom
![image](https://cdn.hackclub.com/019f5272-5e20-7557-b582-d3cbea4bedad/image.png)
so i've managed to get the aliexpress thing down to a reasonable amount. aliexpress is just incredibly annoying because i haven't used up the welcome deal thing on this account, so i just need to avoid those items because it just teleports me to another screen. this does seem like the absolute minimum i could get the bom tho. a lot of this is just because i don't have supplies while i'm here. 

the main gate on this is just that the pcba is so expensive, and the second I stop being in taiwan, the shipping and tariff costs go up by so much. so this is really time gated by quite a few things.

also did a lot of minor fixes on the pcb. didn't change the outline so i think i'm fine on not changing the step