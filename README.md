# Sakura Dungeon Cheat Guide

Sakura Dungeon was made with the visual novel engine [Ren'Py](https://www.renpy.org/).  
It makes it harder to hack the game with something like Cheat Engine, but it's based on [Python](https://www.python.org/), so the game scrips can be easily decompiled and modified.  
In case of Sakura Dungeon we don't have to decompile anything, the game got an developer console, that can be simple enabled and used to modify the game while playing. This is what the guide about.

## Index
* [Get Started](#get-started)
* [Console usage](#console-usage)
 * [Modify stats and attributes](#modify-stats-and-attributes)



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
After [activating](#get-started) the console, you can use it ingame.  
Try to open it with shift+o.  
![Open Console](http://i.imgur.com/qqlsKVO.gif)

Generally the console can execute any valid python command.  
We will use it to manipulate the game.  

### Modify stats and attributes
