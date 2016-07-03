# Sakura Dungeon Cheat Guide

Sakura Dungeon was made with the visual novel engine [Ren'Py](https://www.renpy.org/).  
It's makes it harder to hack the game with something like Cheat Engine, but it's based on [Python](https://www.python.org/), so the game scrips can be easily decompiled and modified.  
In case of Sakura Dungeon we don't have to decompile anything, the game got an developer console, that can be simple enabled and used to modify the game while playing. This is what the guide about.

## Index
* [Get Started](#get-started)
* [Console usage](#console-usage)
 * [Modify stats and attributes](#modify-stats-and-attributes)
 * [Add or remove consumable and valuable](#add-or-remove-consumable-and-valuable-items)
  * [Generally](#generally)
  * [Stats](#stats)
  * [Attributes](#attributes)
* [Credits](#credits)



## Get Started
At first we want to activate the developer console.  

1. Save and close the game.
2. Go to your Sakura Dungeon directory.  
[gif tutorial](http://i.imgur.com/zxrWI2B.gifv)  
3. Go to renpy\common\ folder and search for **00console.rpy**.
4. Open **00console.rpy** and go to line **98**.
5. Change `config.console = False` to `config.console = True`  
[gif tutorial](http://i.imgur.com/rrRn9ce.gifv)
6. Done, now you can use the developer console ingame.


## Console usage
After [activating](#get-started) the console, you can use it ingame.  
Try to open it with `shift+o`.  
[gif tutorial](http://i.imgur.com/qqlsKVO.gifv)

Generally the console can execute any valid python command.  
We will use it to manipulate the game.  

### Modify stats and attributes
After starting a new game or loading a save (not in main menu), you can modify your companions(actors) stats and attributes.  
Stats like VP or AP are dynamic and will be reset to max value in special situations.  
Attributes are more static and will be only modified by items you use.
#### Generally
Each ally got an [object](https://en.wikipedia.org/wiki/Object_\(computer_science\)), you can modify anything about him through his object. Normally this objects got the same name as the character, but there are exceptions. See the *full actors list* below for more informations.  

There are two main characters, **Yomi**(the player) and your first companion **Ceri**.  
Yomi is coincident the player himself, so you can access her/players object through `player` or `fox`.  
And Ceri's object is named `knight`.
With this information you can start modify their stats and attributes.  
At fisrt, let us modify our **Mana shards** amount, attribute `currency` hold this information:    
`player.currency=991337` or `fox.currency=991337` (is the same)  
[animation](http://i.imgur.com/8Z42gsu.gifv)  

All object id's and attributes you can find in the [full actors list](https://docs.google.com/spreadsheets/d/12vLrKiqmfnh0nwrKD5HbC9Qk7lWj77fPff1_-cSj5Os) .

#### Stats
Possible stats are `VP`, `AP` and `CP`.  
Example for Ceri:   
VP: `knight.vp=200`   
AP: `knight.ap=200`  
CP: `knight.cp=200`

#### Attributes
The list of all attributes you can find below in the full actors list.  
Examples for Ceri:  
level: `knight.level=20`   
Vit (vitality): `knight.vit=100`  
fire (resistance): `knight.fire=100`  
shock (resistance): `knight.shock=100`  
and so on  

**Attention! Modify attributes like `type`, `skills`, `abilities`, `hit`, `suffer` or `info` only if you know what you are doing!**


[Full actors(characters) list](https://docs.google.com/spreadsheets/d/12vLrKiqmfnh0nwrKD5HbC9Qk7lWj77fPff1_-cSj5Os)

### Add or remove consumable and valuable items
-- coming soon --  

[Full items list](https://docs.google.com/spreadsheets/d/1ZtdCNY44I7SRhcCkU0ZzTvG5PptmZHj4Kfen7Lh2p8M)


## Credits
[Guys from CE Forum](http://forum.cheatengine.org/viewtopic.php?t=592226)  
[happybrother](http://forum.cheatengine.org/profile.php?mode=viewprofile&u=391862) for hint about console commands.  
[glebsa](http://forum.cheatengine.org/profile.php?mode=viewprofile&u=448688) for actors info.  
