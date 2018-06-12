
# Unity UI best practices
## General
1. __Name UI elements sensibly__ </br>
Just like objects in the scene, UI elements should be **named sensibly** with an indicator of the element type.
Every separate UI entity (for ex. Health Bar, Ammo counter, Stamina Bar) should be organized using an empty gameObject, with a consistent name, for instance “Content”.

2. __Stick to it__ </br>
Stick to whatever format of name you chose internally and follow it across all projects.

![Alt](element_naming.png)
## Components
### Canvas Scaler
3. **Use a Canvas Scaler with consistent resolution across all Canvases** </br>
If you have more than one canvas, make sure to utilize a preset for Canvas Scaler that will have a **certain UI Scale mode** and a **Reference Resolution** that will match your target platform's most common resolution.  

![Alt](canvas_scaler.png)


4. **Adjust Match appropriately** </br>
If target platform has many possible resolutions that vary in the orientation, it is important to make sure that UI scales correctly. Depending on the prevailing shape of the content on a certain canvas, adjust the Match accordingly. 

Here is an example how different Match setting effect a **centered 1000*800 rectangle** (that could be an inventory menu in a PC game that usually has a landscape-aligned shape):

![Alt](match_example.png)

### Rect Transform
5. **Keep values in Rect Transform clean** </br>
Make sure that all values in Rect Transform are cleaned up manually after eye-balled placement of the element. Try to round up numbers to avoid decimals.

![Alt](rect_transform.png)

6. **Keep Scale at 1** </br>
The scale of the UI element should always be 1 by default, unless it is slightly changed by animation or a specific use case applies.

7. **Simple layout - Rect Transform, more than several elements - Layout Component** </br>
Use Rect Transform for creating very simple layouts (like anchoring individual element to a corner of the screen) and Layout Components for layouts with more than several elements or anything that should be stacked.
![Alt](layout_component.png)

8. **Disable Raycast Target** </br>
Disable Raycast Target property for all non-interactive elements straight after you have created them. Grayphic Raycaster will perform intersection checks every frame for all elements that are marked as a Racast Target. In case of complex UI with inappropretely marked elements that  could seriously influence performance.
![Alt](raycast.png)

9. **Use Presets** </br>
Starting from Unity 2018, usse presets for as many common components as possible. Components like Text, Shadow or Outline could be good candidates for having consistent values. 

 10. **Avoid Best Fit** </br>
 If using Unity UI, avoid using Best Fit functionality because it is bad both in terms of design practices (limited number of font sizes rule) and perfomance. You can find more information on why you should avoid Best Fit [here](https://unity3d.com/ru/learn/tutorials/topics/best-practices/optimizing-ui-controls)
 
11. **Use TextMesh Pro component instead of Text** </br>
Because of a Signed Distance Field rendering pipeline, TextMesh Pro could be a very good substitution to a Text component if you are looking for a quality text renders for your project. Textmesh Pro uses the same rebuild rules, so optimization consideration is still necessary.

12. **Do not use textures when they are not needed** </br>
For the UI elements that could be build from white rectangles, do not use any textures, use Image component with an empty source instead. ![Alt](empty_image.png)

## Design

13. **Use Unity Editor as an inspiration** </br>
Elements like Input Field, Slider or ScrollBar, **by default** should behave similarly to those in Unity Editor.

14. **Make Debug UI descreet** </br>
All developer (debug) UI should be discreet and not overlap the primary UI in any way.

15. ** Keep uniformly coloured textures white** </br>
All uniformly colored textures should be white and colored in the Image  component. This promotes wise usage of resources.

16. **Strive for good typography** </br> 
Great typography is a must for achieving a professional look for your game/app. Use high quality fonts and make sure that there are only one or two fonts used. As a rule of a thumb, if using one font, 
## Programming

<!--stackedit_data:
eyJoaXN0b3J5IjpbNDA1MTU5NTQxLC0zMDcyNDc0MTAsLTE5NT
E1MjE1NzQsLTIwNjQzODk0MTMsLTg2MDM4MzI5MiwtMTkwMTM2
ODUyLDEwMDk4Njg4MDAsLTYzNzE4MTExNiwyMDY1OTgzMDQyLC
00NzM1NTkzMTUsMjQ1MTc2OTU2LDIwMjg1MTc4OTUsMjA1Mjgw
MzM2LC02NjQ0MDczNDcsMjAyNzUxMDMxOCw4MTM0NzkwNTYsMj
EyMzYwMzEyMywxMDQ1OTU3ODY5LC05ODE1NjMyNTIsODk3MjA4
NDY3XX0=
-->