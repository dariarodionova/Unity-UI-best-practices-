
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
1. Use **consistent Canvas Scaler** component across all Canvases.
 
If you have more than one canvas, make sure to utilize a preset for Canvas Scaler that will have have a **certain UI Scale mode** and a **Reference Resolution**.  
![Alt](canvas_scaler.png)

2. Depending on prevailing shape of content on a certain canvas, **adjust Match appropriately**.
Here is an example how different Match setting effect a **centered 1000*800 rectangle**.
![Alt](match_example.png)
## Design
## Programming

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTg4NzA5NzY4MCwtMjAyOTc3ODc1MiwxNT
U3MzM0MjM1LDkwODc3NTg3OSwtMTc4MzIyNjYwOSwtMzgxNTgy
OTIxLDE0MjEwNzY1NzMsLTEyMzU4MTEwNDcsLTE4NDQ5NDE5Ml
19
-->