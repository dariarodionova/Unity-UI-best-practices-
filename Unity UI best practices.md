
# Unity UI best practices
## General
### Naming
1. __Name UI elements sensibly.__ </br>
Just like objects in the scene, UI elements should be **named sensibly** with an indicator of the element type.
Every separate UI entity (for ex. Health Bar, Ammo counter, Stamina Bar) should be organized using an empty gameObject, with a consistent name, for instance “Content”.

2. __Stick to it.__</br>
Stick to whatever format of name you chose internally and follow it across all projects.

![Alt](element_naming.png)
## Components
### Canvas Scaler
3. **Use a Canvas Scaler with consistent resolution across all Canvases.** </br>
If you have more than one canvas, make sure to utilize a preset for Canvas Scaler that will have a **certain UI Scale mode** and a **Reference Resolution** that will match your target platform's most common resolution.  

![Alt](canvas_scaler.png)


4. **Adjust Match appropriately.**</br>
If target platform has many possible resolutions that vary in the orientation, it is important to make sure that UI scales correctly. Depending on the prevailing shape of the content on a certain canvas, adjust the Match accordingly. 

Here is an example how different Match setting effect a **centered 1000*800 rectangle** (that could be an inventory menu in a PC game that usually has a landscape-aligned shape):

![Alt](match_example.png)

### Rect Transform
5. **Keep values in Rect Transform clean.**</br>
Make sure that all values in Rect Transform are cleaned up manually after eye-balled placement of the element. Try to round up numbers to avoid decimals.

![Alt](rect_transform.png)

6. **Keep Scale at 1.** </br>
The scale of the UI element should always be 1 by default, unless it is slightly changed by animation or a specific use case applies.

7. **Simple layout - Rect Transform, more than several elements - Layout Component.**
Use Rect Transform for creating very simple layouts (like anchoring individual element to a corner of the screen) and Layout Components for layouts with more than several elements or anything that should be stacked.
![Alt](layout_component.png)

8. **Disable Raycast Target** </br>
Disable Raycast Target property for all non-interactive elements straight after you have created them. Grayphic Raycaster will perform intersection checks every frame for all elements that are marked as a Racast Target. In case of complex UI with inappropretely marked elements that  could seriously influence performance.
![Alt](raycast.png)

9. **Use Presets** </br>
Starting from Unity 2018 
## Design
## Programming

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIwODMwNjgxNTIsMjQ1MTc2OTU2LDIwMj
g1MTc4OTUsMjA1MjgwMzM2LC02NjQ0MDczNDcsMjAyNzUxMDMx
OCw4MTM0NzkwNTYsMjEyMzYwMzEyMywxMDQ1OTU3ODY5LC05OD
E1NjMyNTIsODk3MjA4NDY3LC0xNTIyMTE2NzM4LC0xNjMyMzEw
MzYsLTEwMjI5MDI1NDgsMTU0MDc2ODI3MSw3NzYxNzY2MjcsMj
k5ODcxMDMwLC0yMDI5Nzc4NzUyLDE1NTczMzQyMzUsOTA4Nzc1
ODc5XX0=
-->