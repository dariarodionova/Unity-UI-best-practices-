
# Unity UI best practices
## General
1. __Name UI elements sensibly__ </br>
Just like objects in the scene, UI elements should be **named sensibly** with an indicator of the element type.
Every separate UI entity (for ex. Health Bar, Ammo counter, Stamina Bar) should be organized using an empty gameObject, with a consistent name, for instance “Content”.

2. __Stick to it__ </br>
Stick to whatever format of name you chose internally and follow it across all projects.

![Alt](element_naming.png)
## Components
3. **Use a Canvas Scaler with consistent resolution across all Canvases** </br>
If you have more than one canvas, make sure to utilize a preset for Canvas Scaler that will have a **certain UI Scale mode** and a **Reference Resolution** that will match your target platform's most common resolution.  

![Alt](canvas_scaler.png)


4. **Adjust Match appropriately** </br>
If target platform has many possible resolutions that vary in the orientation, it is important to make sure that UI scales correctly. Depending on the prevailing shape of the content on a certain canvas, adjust the Match accordingly. 

Here is an example how different Match setting effect a **centered 1000*800 rectangle** (that could be an inventory menu in a PC game that usually has a landscape-aligned shape):

![Alt](match_example.png)

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

15. **Keep uniformly coloured textures white** </br>
All uniformly colored textures should be white and colored in the Image  component. This promotes wise usage of resources.

16. **Strive for good typography** </br> 
Great typography is a must for achieving a professional look for your game/app. Use high quality fonts and make sure that there are only one or two fonts used. </br>
As a rule of a thumb, if you are using one font, you can use up to 3 different styles of that font, including regular, bold and italic. If number of fonts is more than one, consider cutting on the number of styles to 1 or 2 for each font.
You can find good fonts preselected specifically for apps at [fontshop.com](https://www.fontshop.com/) or [Google Fonts](https://www.fontshop.com/).

## Programming

17. **No hiding in alpha** </br>
Do not use alpha adjustment as a way to hide parts or whole UIs. If any element is invisible but his state is still set to **active**, it will take part in rendering process and use computational resources. Make sure to disable such element for the period of inactivity.

18. **Pull that scroll** </br>
Use pooling approach for scroll views for cases like leaderboards or any long lists. This will ensure smooth loading, updating and behaviour of element-heavy UI objects. For specific pulling techinques check this. [link](http://example.com).

<!--stackedit_data:
eyJoaXN0b3J5IjpbNTAyNzM2NDI5LC04NzI4Nzk1ODAsLTMwNz
I0NzQxMCwtMTk1MTUyMTU3NCwtMjA2NDM4OTQxMywtODYwMzgz
MjkyLC0xOTAxMzY4NTIsMTAwOTg2ODgwMCwtNjM3MTgxMTE2LD
IwNjU5ODMwNDIsLTQ3MzU1OTMxNSwyNDUxNzY5NTYsMjAyODUx
Nzg5NSwyMDUyODAzMzYsLTY2NDQwNzM0NywyMDI3NTEwMzE4LD
gxMzQ3OTA1NiwyMTIzNjAzMTIzLDEwNDU5NTc4NjksLTk4MTU2
MzI1Ml19
-->