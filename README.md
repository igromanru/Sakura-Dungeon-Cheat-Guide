# Sakura Dungeon Cheat Guide

Sakura Dungeon was made with the visual novel engine [Ren'Py](https://www.renpy.org/).  
It's makes it harder to hack the game with something like Cheat Engine, but it's based on [Python](https://www.python.org/), so the game scrips can be easily decompiled and modified.  
In case of Sakura Dungeon we don't have to decompile anything, the game got an developer console, that can be simple enabled and used to modify the game while playing. This is what the guide about.

## Index
* [Get Started](#get-started)
* [Console usage](#console-usage)
 * [Modify stats and attributes](#modify-stats-and-attributes)
 * [Add or remove consumable and valuable](#add-or-remove-consumable-and-valuable-items)
* [Credits](#credits)



## Get Started
At first we want to activate the developer console.  

1. Save and close the game.
2. Go to your Sakura Dungeon directory.  
[gif tutorial](http://i.imgur.com/zxrWI2B.gifv)  
3. Go to renpy\common\ folder and search for 00console.rpy.
4. Open 00console.rpy and go to line 98.
5. Change `config.console = False` to `config.console = True`  
[gif tutorial](http://i.imgur.com/rrRn9ce.gifv)
6. Done, now you can use the developer console ingame.


## Console usage
After [activating](#get-started) the console, you can use it ingame.  
Try to open it with shift+o.  
[gif tutorial](http://i.imgur.com/qqlsKVO.gifv)

Generally the console can execute any valid python command.  
We will use it to manipulate the game.  

### Modify stats and attributes
After starting a new game or loading a save (not in main menu), you can modify your companions(actors) stats and attributes.  
Stats like VP or AP are dynamic and will be reseted to max value in special situations.  
Attributes are more static and will be only modified by items you use.
#### Generally
-- coming soon --
#### Stats
-- coming soon --

[Full actors(characters) list](https://docs.google.com/spreadsheets/d/1ZtdCNY44I7SRhcCkU0ZzTvG5PptmZHj4Kfen7Lh2p8M)

### Add or remove consumable and valuable items
-- coming soon --  

[Full items list](https://docs.google.com/spreadsheets/d/12vLrKiqmfnh0nwrKD5HbC9Qk7lWj77fPff1_-cSj5Os)


## Credits
[Guys from CE Forum](http://forum.cheatengine.org/viewtopic.php?t=592226)  
[happybrother](http://forum.cheatengine.org/profile.php?mode=viewprofile&u=391862) for hint about console commands.  
[glebsa](http://forum.cheatengine.org/profile.php?mode=viewprofile&u=448688) for info about actors.  
