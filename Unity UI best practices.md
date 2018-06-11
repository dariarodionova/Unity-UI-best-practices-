
# Unity UI best practices
## General
### Naming
__Name UI elements sensibly__
Just like objects in the scene, UI elements should be named sensibly with an indicator of the element type.
Every separate UI entity (for ex. Health Bar, Ammo counter, Stamina Bar) should be organized using an empty gameObject, with a consistent name, for instance “Content”.
![Alt](element_naming.png)

__Stick to it__
Stick to whatever format of name you chose internally and follow it across all projects.
## Components
### Canvas Scaler
 Use consistent Canvas Scaler component across all Canvases.
 
If you have more than 1 canvas, make sure to utilize a preset for Canvas Scaler that will have have a **certain UI Scale mode** and a **Reference Resolution**.  
Depending on prevailing shape of content on a certain canvas, adjust Match appropriately.
## Design
## Programming

<!--stackedit_data:
eyJoaXN0b3J5IjpbOTA4Nzc1ODc5LC0xNzgzMjI2NjA5LC0zOD
E1ODI5MjEsMTQyMTA3NjU3MywtMTIzNTgxMTA0NywtMTg0NDk0
MTkyXX0=
-->