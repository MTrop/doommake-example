# DoomMake Example WAD

by MTrop (C) 2021

## What This Is

This is an example DoomMake project to show people how cool this stuff is.


## First Steps

Create a file called `doommake.properties` and throw this stuff in there:

	doommake.iwad=H:/Doom/iwads/DOOM2.WAD
	doommake.run.exe=H:/DoomDev/Exes/ChocoDoom/chocolate-doom.exe
	doommake.run.switch.file=-merge

You'll probably have to change those paths to the pertinent files. Note that `.properties` 
files use backslashes differently (see the [Wikipedia Page](https://en.wikipedia.org/wiki/.properties). 
The first property is for the IWAD to use as a base for texture merging (`DOOM2.WAD`), 
and the other is for locating Chocolate Doom to test (if you don't use Chocolate Doom, 
remove the last line).

This file is ignored in your repository.


## Generated by the Project

Some directories/files in this project are ignored by Git:

	/build               Build directory.
	/dist                Distributables directory.
	doommake.properties  Project property override file.


## To Build This Project

This project requires the [DoomTools](https://github.com/MTrop/DoomTools) toolchain for
building it. Clone this project to a new folder and type the following to build everything
(plus the distributable):

	doommake


To clean the build folder, type:

	doommake clean


To build the DeHackEd patch from DECOHack source:

	doommake patch


To build just the maps WAD:

	doommake maps


To build the assets WAD:

	doommake assets


To extract only the textures used by maps to a separate WAD file:

	doommake maptextures


To run this project (after setting the correct properties):

	doommake run


To build all components:

	doommake all


To build the full release and distributable:

	doommake release
