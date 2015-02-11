# Game Development with Unity

> ####Useful Links for the course
>
> **Unity**
>
> - [Download Unity](http://unity3d.com/unity/download)
> - [Unity Scripting API](http://docs.unity3d.com/ScriptReference/index.html)
> - [Unity Video Tutorials](http://unity3d.com/learn/tutorials/modules/beginner/editor)
> - [Unity Community Support](http://unity3d.com/community)


## Foundation Phase (120 hours)

In this phase students will build the two dimensional game Pong as well as slightly more challenging three dimensional game where they navigate a ball through a maze.  By the end of this foundation, the student should be equipped with knowledge pertaining to the Unity application, basic C# knowledge, and how Unity ties all pieces of a game together to make it a functional unit.  All assets will be provided for his phase.

### Introduction to C#: why we chose it and how it will aid with our game development
    - Dissecting Hello World (code sample provided)
        - Syntax Conventions
        - Commenting    
        - Introduction to variables, types and assignment and why we need them
        - Explaining the idea of a library or import
    - Introduction to conditionals (modifying hello world)
    - Introduction to loops (modigyin hello world)
    - Introduction to classes and methods (modifying hello world)
        - What's a constructor?
        - Explain what visibilty on a method is and how it can be used to your advantage as a programmer
        - Explain method overloading
    - Introduction to the most widely used data structures (modifying hello world)
        - Queue
        - Stack
        - Hashtable
    - Introduction to interfaces and what they're good for
    - Introduction to abstract classes and what they're good for
    - Introduction to exception handling 
    - Go over some basic debugging by introducing an error and stepping through code

After Hello World is built, describe the major principles of Object Orient Programming and the difference between functional and object orient programming.
    - Abstraction
    - Inheritence
    - Encapsulation
    - Polymorphism 

### Time to Build our First Game

0. Setting up Our project, creating a githug profile and initializing a git repository
    - Explain revision control and why we need it
    - Student creates github account if they haven't already and initializes a github repository for their game
    - Student makes their first commit
    - Brief overview of basic git commands:
        - git fetch
        - git pull
        - get checkout

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
    - Creating your first branch in git: In this checkpoint you will learn how to create a branch in git 
        - What is branching?  Why do we need/use branches?
        - Creating a branch for our first game
    - Creating Your First Game Board: Most games start with an environment or level, in Pong we have a simple board.  In this checkpoint we show how to create the game board for Pong which is effectively creating a GameObject, naming it, setting the proper sprite, then setting the layer properties.
    - Describe what a 'PreFab' is

3. Camera Setup
    - Setting Up The Camera: In this checkpoint we show how to set the camera for Pong and why the camera needs to be set in a certain fashion.
    - Setting Up the Boundaries for our Game Board: In this checkpoint we show how to add boundaries to the Pong game so that the players move within the boundary constraints.
        - Breakpoint: Introduction to 'MonoDevelop' which is ehe IDE that Unity has chosen to use.
            - Explain what an IDE is and why we use them
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

## Intermediate Phase (120 hours)
    - In this phase, the student will build a more sophisticated 2D game such as Angry Birds which [Unity suggests](http://unity3d.com/learn/tutorials/modules/beginner/live-training-archive/making-angry-birds-style-game) is an "intermediate" level of game to build, or a 3D intermediate game.
    - Student will also learn more advanced git techniques such as merging, rebasing, etc. 

### Game One: Our First Three Dimensional Game - Zombie Slayer - this series of checkpoints will focus heavily on the scripting aspect of Unity

0.  Creating a 3D project

1.  Setting up the Environment
    - Set the lighting for the game

2.  Setting the navigation in the 3D world
    - Add the Mesh Collider component
    - Creating the NavMesh
    - Baking the NavMesh
    - Assignment: Add background music to the game
        - Tip: use a compressed audio file otherwise the game will be too big

3.  Building our Zombie Slayer
    - Importing the 3D asset into Unity
    - Adding the animation controller, this is basically a state diagram within Unity that controls what states the player can be in:
        - Idle, Move, Death
    - Assignment: Build a script that will follow the zombie slayer
    - Assignment: Add an audio source when the zombie slayer gets hurt
    - Assignment: Add an audio source when the zombie slayer fires his weapon
    - Animating our player's movement using scripting
        - Introduction to raycasting
    - Assignment: Build a script that will manage the Zombie Slayer's health

4.  Adding enemies to our game
    - Importing the 3D zombie asset
    - Adding the spwan points for the zombies
    - Assignment: create a script that will randomly spawn zombies in a series of set places and then attach it to the spawn points

5.  Keeping Track of the Score
    - Assignment: Build a script to keep track of how many zombies have been killed.
    - Assignment: Display the zombie kill count in the game

6.  Game Over
    - Assignment: Build a smooth 'game over' state 
        - Give them a partially filled out GameOverManager script
        - When the players dies it should be animated
        - After the animation ends, fade the game out, fade the game over state in and end the game
        - Add a restart button that will restart the game

### Game Two: Angry Birds - this series of checkpoints will introduce some new techniques we haven't seen as well as some scripting techniques

1.  Setting up the Environment 
    - Assignment: Setting the sprite
    - Assignment: Adding grass
    - Assignment: Adding a 2D edge collider to the grass
    - Introduction to sorting layers

2.  Setting up the Camera
    - Setting the size

3.  Adding the catapult (This is sort of analagous to the player module)
    - Adding the components of the catapult and setting layers correctly
    - Adding the asteroid to the catapult
        - Applying the physics engine to the asteroid sprite
            - Adding linear drag
            - Adding angular drag
        - Adding circular 2D collider
            - Modifying the radius
    - Adding the catapult slings
    - Adding the spring joint 2D to the asteroid
        - anchor to the catapult
    - Adding the rubber bands
        - Add the line renderers to the catapult
        - Add the new material to define the band
        - Set material on line renderers
    - Adding the ProjectileDragging.cs script to Asteroid
 
4.  Modifying the camera to follow the Asteroid
    - Adding a script that controls the camera position, add the script to Main Camera
    - Adding boundary markers (left and right)

5.  Getting the game to restart
    - Add Boundary object that is a trigger to restart the game
    - Assignment: Add a reset script

6.  Building the Structures to be knocked down
    - Same patterns as always, add the colliders

7.  Adding the Target
    - Assignment: Add a script to control the amount of damage the asteroid does

8.  Adding a Score System
    - Assignment: Build a script that will manage how many points the player has scored

9.  Adding More Levels
    - Assignment: Build a completely new level (Scene) which we haven't done yet, reuse existing components to create said scene

## Advanced Phase (260 Hours)

Build your own game from scratch (with assets from Unity) from a pool of games that we predetermine are sophisticated enough.
    - Ideas for sophisticated games for students to build:
        - Minesweeper
        - Tetris
        - 3D RPG with certain features such as, levels, inventory system, objectives, etc.
        - A first person shooter like Duke Nukem 3D
