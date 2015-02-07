# Game Development with Unity

> ####Useful Links for the course
>
> **Unity**
>
> - [Download Unity](http://unity3d.com/unity/download)
> - [Unity Scripting API](http://docs.unity3d.com/ScriptReference/index.html)
> - [Unity Video Tutorials](http://unity3d.com/learn/tutorials/modules/beginner/editor)
> - [Unity Community Support](http://unity3d.com/community)

## Foundation Phase

In this phase students will build the two dimensional game Pong as well as slightly more challenging three dimensional game where they navigate a ball through a maze.  By the end of this foundation, the student should be equipped with knowledge pertaining to the Unity application, basic C# knowledge, and how Unity ties all pieces of a game together to make it a functional unit.  All assets will be provided for his phase.

0. Setting up Our project, creating a githug profile and initializing a git repository
    - Explain revision control and why we need it

1. Brief introduction to the Unity Interface

    What is Unity?
    [Unity](http://en.wikipedia.org/wiki/Unity_(game_engine)) is a cross-platform game creation system developed by Unity Technologies, including a game engine and integrated development environment (IDE).  It is used to develop video games for web sites, desktop platforms, consoles, and mobile devices.

    - What do different views in the software do? 
        - Game
        - Scene (explain here that this is effectively a level?)
        - Hierarchy
        - Inspector
        - Project
        - Console
    - Teach the student that the views can be manipulated and dragged around to their liking.
    - Explain the static 'Layers' and 'Layout' button at the top right of the software.

2. Setting up the Environment
    - Creating Your First Game Board: Most games start with an environment or level, in Pong we have a simple board.  In this checkpoint we show how to create the game board for Pong which is effectively creating a GameObject, naming it, setting the proper sprite, then setting the layer properties.

3. Camera Setup
    - Setting Up The Camera: In this checkpoint we show how to set the camera for Pong and why the camera needs to be set in a certain fashion.
    - Setting Up the Boundaries for our Game Board: In this checkpoint we show how to add boundaries to the Pong game so that the players move within the boundary constraints.
        - Breakpoint: Introduction to 'MonoDevelop' which is ehe IDE that Unity has chosen to use.
            - Explain what an IDE is and why we use them
        - Breakpoint: Introduction to C# programming language via overview of GameSetup.cs
            - Class
            - Variables
            - Methods
            - Commenting
            - Imports
        - Set up the "top wall" and "left wall" for the student.
        - Assignment: have the student create the bottom and right walls.

        ![GameManager.cs](http://bit.ly/1I5QELF)

4. Adding Players to your Game
    - Adding Player 1
        - Adding the Sprite and Mapping the Components to the Sprite: In this checkpoint we'll show the student how to add components such as the box collider to a Sprite and explain why we need to do that.
        - Setting Player1 position in GameManager.cs
    - Adding Player 2
        - Assignment: Setting Player2 position in GameManager.cs

5. Adding the Ball to your Game
    - Adding the Sprite
    - How do we make the ball bounce?  There are three components that help define the bounce of the ball, we have seen two of those components used in the past and we will give you the third component.  First, take a stab at adding the two components to the ball sprite that you think would define it's bounce properties.  The third component will be a 2D physics material we define the actual bounciness property on and apply to an aforementioned component. 
        - Assignment: have the student create both the 2D circle collider and a 2D rigid body
        - Adding a 2D physics material
        - Adding a ball script
            - Breakpoint: more programming concepts
                - Introduction to random numbers in CSharp to control start of ball motion.
                - Introduction to debug logging.
                - Introduction to the console (purposefully have them script an error so we can see it in the console and debug it)
            - Add spin onto the ball
                - Adding mass to the players so that they aren't pushed
                - Show student how to do vector math to make the ball have some spin in the Ball script

6. What is a game without a score?  In this section we learn how to display the score in Pong
    - Create the ScoreManager script
    - Add ScoreManager script to GameManager
    - Set left and right wall triggers and create script that attaches to ScoreManager named 'SideWalls'
    - Add the Score skin which is basically a label
    - Set the font on the score by adding a custom asset

7. We now have a functional game, but we can only play through one point.  In this checkpoint you will learn how to reset the ball's position when a point is scored.
    - More scripting in the walls management script to send a signal to the ball script to tell it to reset.
    - More scripting in the ball script to reset it's position when a point is scored

8. Our game is cool but we don't have sound, how do we add sound to our game?
    - Add audtio source to ball strike
    - Adding pitch variation to the ball strike
    - Assignment: now you add a sound when the player scores
    - Lastly, let's add background music to the game
        - Breakpoint: Audio optimization
            - Since the background track is larger in size and longer we will want to make sure that the settings are correct such as:
                - 'Use compression'
                - 'Stream from disc'

9. Miscellaneous Stuff, tweaking our game
    - Physics2D settings
    - Positions iterations
    - Adding a restart button to the game
        - Modifying the score manager script
        - Adding a tag to the ball object so we can reference it later
        - Assignment: change the font on the button

10. Build Settings and Exporting our Game
    - Add the scenes to the Build Settings Scenes pane
    - Modify the Build Settings to build for Android
    - Add an icon for your game
    - Setting the Bundle Identifier    
    - And finally getting the APK onto your phone (or emulator) to test it out

## Intermediate Phase

## Advanced Phase
