## Build the disco floor

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step you will build the disco dance floor for your project. 
</div>
<div>
![The Stage view with the tiles and four walls framing the tiles.](images/fourth-wall.png){:width="350px"}
</div>
</div>

--- task ---

Launch the Unity Hub and open the project you created for [Rainbow run](https://projects.raspberrypi.org/en/projects/rainbow-run/0){:target='_blank'}.

--- collapse ---

---
title: I haven't got my Rainbow run project
---

If you are unable to open your project, launch the Unity Hub and click **Projects** then select **New project**:

![A screenshot of the black bar at the top of the Unity Hub with the 'New Project' button highlighted in red.](images/new-project.png)

From the list choose **All templates** then select **3D Core**:

![A screenshot of the left pane in the Unity Hub. The 3D core option is highlighted in red.](images/3D-core.png)

Edit the project settings to give your project a sensible name and save it to a sensible location. Then click **Create project**:

![A screenshot of the right pane in the Unity Hub. The filename and the 'Create Project' sections are highlighted in red.](images/create-project.png)

Your new project will open in the Unity Editor. It may take some time to load.

Download and unzip the [More Unity starter package](https://rpf.io/p/en/rainbow-run-go){:target="_blank"} to your computer. 

**Tip:** Choose a sensible location such as your Documents folder.

The Unity starter package you downloaded for this More Unity path contains a number of **Assets** for you to use in your project.

To import them into your new project, click on the **Assets menu** and select **Import package > Custom Package…** then navigate to the downloaded Unity starter package.

--- /collapse ---

--- /task ---

--- task ---

In the **Project** panel right-click and select **Create --> Scene**.

![The right-click menu with Create and Scene highlighted](images/create-scene.png)

In the pop-up window, name your Scene `Disco Dance Floor`:

A new file will appear in the Assets folder in the Project window:

![Project window with Disco Dance Floor scene in the Assets folder.](images/disco-dance-floor-scene.png)

Drag the new Scene into the 'Scenes' folder to organise your files.

--- /task ---

### Build a floor

--- task ---

In the Project window, click on **Parts**.

**Drag** the '8x8Floor' object to the Scene view: 

Your scene should look like this:

![The Scene View with a grey grid of 8*8 square tiles.](images/tiled-floor.png)

--- /task ---

--- task ---

In the Inspector window, change the Transform properties of the '8x8Floor' GameObject: Position X=`0`, Y=`0`, Z=`0`.

![The Inspector window with the Transform component of the 8x8Floor GameObject, with position values all set to 0](images/floor-position.png)

--- /task ---

--- task ---

In the Hierarchy window, right-click on the '8x8Floor' GameObject and select **Create Empty Parent**. 

A new parent 'GameObject' will be created:

![The Hierarchy window with the 'Floor' GameObject nested inside a new object called 'GameObject'.](images/empty-parent.png)

Right-click on the new GameObject and rename it to 'Dance Floor':

![The Inspector window with the name property highlighted and the typed name 'Dance Floor'.](images/rename-gameobject.png)

--- /task ---

--- task ---

From the Hierarchy window you can see that the 'Floor' GameObject contains 64 individually numbered cubes.

Click on the 'Cube' GameObject. Hold down the <kbd>shift</kbd> and scroll to the bottom of the list of cubes then click on 'Cube.0063'. All of the cubes will be highlighted: 

![The Hierarchy window with the 'Floor' GameObject expanded showing a number of cube objects within it. The cubes are names 'Cube', 'Cube.001', 'Cube.002' and so on. All of the cubes are highlighed with a blue background.](images/hierarchy-cubes.png)

--- /task ---

--- task ---

With all the cubes selected, go to the Inspector window and click 'Add Component'. Type 'Box' into the search box then click on 'Box Collider'. This will add a box collider to each of the cubes:

![The Inspector window with the Add Component search box and the word 'box' typed in the top search bar. The top result returned is 'Box Collider' and this is highlighted](images/add-box-collider.png)

![The Scene view showing some of the tiles. There is a thin green line around the edges of each tile to show the box colliders.](images/box-collider-scene.png)

--- /task ---

### Add walls

--- task ---

Go to the Hierarchy and right-click on the 'Dance Floor' GameObject. Select **3D Object > Cube**:

![The Hierarchy window with the 'Dance Floor' GameObject expanded. Inside is a 'Floor' GameObject and a new 'Cube' GameObject.](images/hierarchy-wall.png)

In the Inspector window, change the Transform properties of the new cube: Position X=`9.25`, Y=`1`, Z=`0` and Scale X=`1`, Y=`2`, Z=`19.5`. 

![The Inspector window with the Transform property showing updated values.](images/transform-wall.png)

![The Stage view with the tiles and one wall positioned at the bottom left edge.](images/first-wall.png)

--- /task ---

--- task ---

Go to the Hierarchy and right-click on the 'Cube' GameObject. Select **Duplicate**.

In the Inspector window, change the Transform properties of the new cube to. Position X=`-9.25`.

![The Stage view with the tiles and two wall positioned opposite each other.](images/second-wall.png)

--- /task ---

--- task ---

Go to the Hierarchy and right-click on the original 'Cube' GameObject again. Select **Duplicate**.

In the Inspector window, change the Transform properties of the new cube to Position X=`0`, Y=`1`, Z=`9.25` and Rotation X=`0`, Y=`90`, Z=`0`.

![The Stage view with the tiles and three walls.](images/third-wall.png)

--- /task ---

--- task ---

Go to the Hierarchy and right-click on the 'Cube (2)' GameObject you just rotated. Select **Duplicate**.

In the Inspector window, change the Transform properties of the new cube to Position Z=`-9.25`.

![The Stage view with the tiles and four walls framing the tiles.](images/fourth-wall.png)

--- /task ---