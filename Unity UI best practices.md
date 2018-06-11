
# Unity UI best practices
## General
### Naming
1. __Name UI elements sensibly.__ </br>
Just like objects in the scene, UI elements should be **named sensibly** with an indicator of the element type.
Every separate UI entity (for ex. Health Bar, Ammo counter, Stamina Bar) should be organized using an empty gameObject, with a consistent name, for instance “Content”.

3. __Stick to it.__</br>
Stick to whatever format of name you chose internally and follow it across all projects.

![Alt](element_naming.png)
## Components
### Canvas Scaler
1. **Use a Canvas Scaler with consistent resolution across all Canvases.** </br>
If you have more than one canvas, make sure to utilize a preset for Canvas Scaler that will have a **certain UI Scale mode** and a **Reference Resolution** that will match your target platform's most common resolution.  

![Alt](canvas_scaler.png)


2. **Adjust Match appropriately.**</br>
If target platform has many possible resolutions that vary in the orientation, it is important to make sure that UI scales correctly. Depending on the prevailing shape of the content on a certain canvas, adjust the Match accordingly. 

Here is an example how different Match setting effect a **centered 1000*800 rectangle** (that could be a inventory menu that in a PC game that usually has a landscape-aligned shape:

![Alt](match_example.png)
## Design
## Programming

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk4MTU2MzI1Miw4OTcyMDg0NjcsLTE1Mj
IxMTY3MzgsLTE2MzIzMTAzNiwtMTAyMjkwMjU0OCwxNTQwNzY4
MjcxLDc3NjE3NjYyNywyOTk4NzEwMzAsLTIwMjk3Nzg3NTIsMT
U1NzMzNDIzNSw5MDg3NzU4NzksLTE3ODMyMjY2MDksLTM4MTU4
MjkyMSwxNDIxMDc2NTczLC0xMjM1ODExMDQ3LC0xODQ0OTQxOT
JdfQ==
-->