
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
 Use **consistent Canvas Scaler** component across all Canvases.
 
If you have more than one canvas, make sure to utilize a preset for Canvas Scaler that will have have a **certain UI Scale mode** and a **Reference Resolution**.  
Depending on prevailing shape of content on a certain canvas, adjust Match appropriately.
![Alt](canvas_scaler.png)

## Design
## Programming

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIwMjk3Nzg3NTIsMTU1NzMzNDIzNSw5MD
g3NzU4NzksLTE3ODMyMjY2MDksLTM4MTU4MjkyMSwxNDIxMDc2
NTczLC0xMjM1ODExMDQ3LC0xODQ0OTQxOTJdfQ==
-->