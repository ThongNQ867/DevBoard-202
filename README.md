# DevBoard202
This is a dev board that runs with the RP2040 but structured more simple than Pi Pico. The schematic is inspired by the document "Hardware design with RP2040", the PCB is made with the tutorial from @KaiPereira

While there is a tutorial from Blueprint, I think it is better to fact check stuffs again and get understand more clearly about how to set up the value for resistors and capacitors by myself from these 2 links:
RP2040 datasheet
https://pip-assets.raspberrypi.com/categories/814-rp2040/documents/RP-008371-DS-1-rp2040-datasheet.pdf?disposition=inline

Hardware design with rp2040
https://pip-assets.raspberrypi.com/categories/814-rp2040/documents/RP-008279-DS-1-hardware-design-with-rp2040.pdf?disposition=inline

Pi Pico Datasheet
https://pip-assets.raspberrypi.com/categories/610-raspberry-pi-pico/documents/RP-008307-DS-1-pico-datasheet.pdf?disposition=inline

I also try to add a VSYS pin which include the use of a Schottky diode between the VBUS and VSYS so that I can power it by an external power source. I found it quite challenging to understand how the USB host mode work but I think powering the external power source to the VBUS would probably be fine. Also because of powering externally to VSYS, I also pull VBUS down if its not connected to power source with 2 resistors to GND.

<img width="1130" height="764" alt="image" src="https://github.com/user-attachments/assets/606744dd-49ea-4e4c-9ee4-cdaa2997c876" />


For me, PCB routing is the most problematic part of this project, partly because I'm new to KiCAD, partly because of the enormous diode (which I have changed to a more cost effective and 10 times smaller version). I started trying to make a PCB with the size of a Pi Pico but ended up increase the width to make the wiring easier 


<img width="225" height="347" alt="image" src="https://github.com/user-attachments/assets/1e5f82fc-0b17-4adf-a16b-2884519198a3" />

This project has taught me a lot on how to use KiCAD and choose componets to print for my PCB. 


BOM: 


<img width="827" height="1045" alt="image" src="https://github.com/user-attachments/assets/0123e93d-a82e-48ba-a138-08c6286b8be3" />


