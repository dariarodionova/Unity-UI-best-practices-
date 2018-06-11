
# Unity UI best practices
## General
### Naming
1. __Name UI elements sensibly__
Just like objects in the scene, UI elements should be **named sensibly** with an indicator of the element type.
Every separate UI entity (for ex. Health Bar, Ammo counter, Stamina Bar) should be organized using an empty gameObject, with a consistent name, for instance “Content”.

2. __Stick to it__
Stick to whatever format of name you chose internally and follow it across all projects.

![Alt](element_naming.png)
## Components
### Canvas Scaler
1. Use a ** Canvas Scaler with a consistent resolu** component across all Canvases.
 
If you have more than one canvas, make sure to utilize a preset for Canvas Scaler that will have have a **certain UI Scale mode** and a **Reference Resolution**.  

![Alt](canvas_scaler.png)

2. Depending on prevailing shape of content on a certain canvas, **adjust Match appropriately**.
Here is an example how different Match setting effect a **centered 1000*800 rectangle**:

![Alt](match_example.png)
## Design
## Programming

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk0MTY3OTIxMCwyOTk4NzEwMzAsLTIwMj
k3Nzg3NTIsMTU1NzMzNDIzNSw5MDg3NzU4NzksLTE3ODMyMjY2
MDksLTM4MTU4MjkyMSwxNDIxMDc2NTczLC0xMjM1ODExMDQ3LC
0xODQ0OTQxOTJdfQ==
-->