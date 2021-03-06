# Domino-MayaRenderingTool
***A python script for rendering in Maya renderView by frame.***  
  
![alt text](http://i.imgur.com/2dMnoeQ.png "dp_Domino")


## Features

* #### **Visualize rendering progress**  
 > ###### *A mission window showing each layer's rendering progress.*
 > ![alt text](http://i.imgur.com/OQdKNMj.png "Visualize rendering progress")

* #### **Layer/Frame custom render order**  
 > ###### *Define rendering priority by layer or frame, and choose rendering forward or backward.*
 > ![alt text](http://i.imgur.com/MDHod7e.png "Layer/Frame custom render order")

* #### **Scenes rendering queue**  
 > ###### *Automatically switching files to render and available to auto saving file.*
 > ![alt text](http://i.imgur.com/llWPCfh.png "Scenes rendering queue")

* #### **Custom frame range**  
 > ###### *Rendering sequence or non-sequence by custom range.*
 > ![alt text](http://i.imgur.com/vCvIt4q.png "Custom frame range")

* #### **RenderJob layer**  
 > ###### *Multiple layers with different renderSettings but output same sequence name images.*
 > ![alt text](http://i.imgur.com/auarUSI.png "RenderJob layer")

* #### **Layer override remote**  
 > ###### *Create or adjust camera/frame's layer override attribute without switching layer.*
 > ![alt text](http://i.imgur.com/hNS4xQj.png "Layer override remote")

* #### **Records rendering time**  
 > ###### *Record each frame's rendered time. V-Ray's renderSlave number can also be recorded.*
 > ![alt text](http://i.imgur.com/TGqEdGd.png "Records rendering time")

* #### **Send email notice**  
 > ###### *Sending notice by the events you choose.*
 > ![alt text](http://i.imgur.com/7AZmbs5.png "Send email notice")



## Latest Version
* **1.1.0-Beta**

* Supported Maya Version
  - **Maya 2014**
  - **Maya 2015**
  - *Others not tested yet, better with pySide.*

* Supported platform
  - **Windows**
  - *Others not tested yet, should work.*  



## Installation
1. Put this file `dp_Domino.py` into your Maya script folder, restart maya if necessary.
2. Copy the following code as `shelf button(python)`.

   ```python
   import dp_Domino
   reload(dp_Domino)
   dp_Domino.init_dp_Domino.dp_init()
   ```
3. Have a nice render.



## Usage
    [video here]

1. Open the scene that you want to render.

2. Press the shelf button of dp_Domino.

3. Adjust frame range, renderable camera and check other settings.

4. Press `READY` to open the progress window.

5. Adjust layers' rendering order if you have multiple layers.

6. Save scene.

7. If there's other scenes need to add in queue, close progressWindow. If not, jump to step9.

8. Repeat step 1 to 7.

9. Add other scenes into sceneQueue if current scene is not the only one needs to be  rendered.

10. Press `START` to start render.

11. Hit `Esc` if you need to stop. But when rendering with V-ray, press `STOP` first and then `Esc`.

12. Wait for rendering progress complete and check images output.



## Known Issues
- **The current frame number showing in time slider is one frame ahead than actual rendering frame.**
  > Might be maya's ui evaluation problem, yet image output is correct.

- **Maya went critical crash when you open renderSetting panel after `dp_domino` automatically open next scene in `sceneQueue`.**
  > Reason unknown. Try not to touch anything when using sceneQueue and it will work properly.
