# Sakura Dungeon Cheat Guide

Sakura Dungeon was made with the visual novel engine [Ren'Py](https://www.renpy.org/).  
It makes it harder to hack with something like Cheat Engine but it's based on [Python](https://www.python.org/), so scrips can be easely decompiled and modified.  
But in case of Sakura Dungeon we don't have to decompile anything, the game got an developer console, that can be simple enabled. And this is what this guide about.

## Index
* [Get Started](#get-started)
* [Console usage](#console-usage)
  *



## Get Started
At first we want to activate the developer console.  

1. Save and close the game.
2. Go to your Sakura Dungeon directory.
![Step 1](http://i.imgur.com/zxrWI2B.gif)  
3. Go to renpy\common\ folder and search for 00console.rpy.
4. Open 00console.rpy and go to line 98.
5. Change `config.console = False` to `config.console = True`
![Step 1](http://i.imgur.com/xknDyqz.gif)
6. Done, now you can use the developer console ingame.


## Console usage
After [activating](#get-started) the console, you can open it ingame.  
Try to open it with Shift+o.  
![Console](http://i.imgur.com/qqlsKVO.gif)

Generelly the console can execute any valid python command.  
We will use it to manipulate the game.  

### Modify stats and attributes
