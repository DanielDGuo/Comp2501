All sprites created by DANIEL GUO with the use of Pixilart.com, and inspiration taken from various sources.
Developed on a Win11 OS system

Modified files include game.h, game.cpp
Modified or new functions and code are signaled with "(DANIEL GUO)" in comments preceding it.

To set up the code, run CMake, and select the correct lbiraries. GLM may not have been correctly sdet up; 
you may need to go into project->properties->C/C++->general and add the lbirary folder into "Additional Include
Directories"
you will also have to set Assignment1 as the startup.

New textures were added into the texture file, and added to the tex[] array in game.cpp. 
	These texture are used by the new game objects.
	
With use of the starting collision code, the position of the collided object is recorded, the object
deleted, and a new temporary "boom" object is stored. A collision counter is also ticked up.
	Every 5 seconds, the game checks for temporary objects and deletes them.

When the collision counter reaches 3, controls are disabled, and on the next check for temporary objects,
the window is closed and game over is shown.