# Sakura Dungeon Cheat Guide

Sakura Dungeon was made with the visual novel engine [Ren'Py](https://www.renpy.org/).  
It's makes it harder to hack the game with something like Cheat Engine, but it's based on [Python](https://www.python.org/), so the game scrips can be easily decompiled and modified.  
In case of Sakura Dungeon we don't have to decompile anything, the game got an developer console, that can be simple enabled and used to modify the game while playing. This is what the guide about.  
  

## Index
* [Get Started](#get-started)
* [Console usage](#console-usage)
 * [Modify stats and attributes](#modify-stats-and-attributes)
    * [Generally](#generally)
    * [Stats](#stats)
    * [Attributes](#attributes)
 * [Add or remove consumable, valuable items and outfits](#add-or-remove-consumable-valuable-items-and-outfits)  
    * [Consumables](#consumables)
    * [Valuables](#valuables)
    * [Outfits](#outfits)
 * [Add or remove companions](#add-or-remove-companions)
* [Actors list](#actors-list)
* [Items list](#items-list)
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
Some Stats like VP or AP are dynamic and will be reseted to max value.  
Attributes are more static and will be only modified by items you use.
#### Generally
Each ally got an [object](https://en.wikipedia.org/wiki/Object_\(computer_science\)), you can modify anything about him through his object. Normally this objects got the same name as the character, but there are exceptions. See the *[actors list](#actors-list)* for more informations.  

There are two main characters, **Yomi**(the player) and your first companion **Ceri**.  
Yomi is coincident the player himself, so you can access her/players object through `player` or `fox`.  
And Ceri's object is named `knight`.
With this information you can start modify their stats and attributes.  
At fisrt, let us modify our **Mana shards** amount, attribute `currency` hold this information:    
`player.currency=991337` or `fox.currency=991337` (is the same)  
[animation](http://i.imgur.com/8Z42gsu.gifv)  

All object id's and attributes you can find in the [actors list](#actors-list) .

#### Stats
Possible stats are `VP`, `AP`, `CP`, `XP`, `max_vp` and `max_ap`.  
`VP`, `AP`, `max_vp`, `max_ap` and `XP` can be directly modified, but `CP` need two methods.  

Example for Ceri:   
VP: `knight.vp=999` (will be reseted to max)  
AP: `knight.ap=999`  (will be reseted to max)  
Max VP: `knight.max_vp=200`   
Max AP: `knight.max_ap=200`  
XP: `knight.xp=99`

CP methods:  
To change CP: `knight.cp_change(10, force=True)`  
Reset CP:   `knight.reset_cp()`  



#### Attributes
The list of all attributes you can find in the [actors list](#actors-list).  
Resistance work a bit different, 1 point = 25%.  
Examples for Ceri:  
level: `knight.level=20` (set level to 20)  
Vit (vitality): `knight.vit=100` (set vit to 100)  
fire (resistance): `knight.fire=4` (4 \* 25% = 100%)  
shock (resistance): `knight.shock=2` (2 \* 25% = 50%)  
and so on  
[animation](https://gfycat.com/BreakableBigArrowworm)

**Attention! Modify attributes like `type`, `skills`, `abilities`, `hit`, `suffer` or `info` only if you know what you are doing!**

[Full actors(characters) list](#actors-list)

### Add or remove consumable, valuable items and outfits
Objects `player`, `fox` and `knight` got [lists](https://en.wikipedia.org/wiki/Linked_list), which can be filled with another objects. A list got two necessary [mehtods](https://en.wikipedia.org/wiki/Method_\(computer_programming\)), `append()` and `remove()`.  This methods will be needed to add and remove items.  
Full items list can be found here: [Full items list](https://docs.google.com/spreadsheets/d/1ZtdCNY44I7SRhcCkU0ZzTvG5PptmZHj4Kfen7Lh2p8M)
##### Consumables
`player` got list `items`, to add an item, we have to append it:  
`player.items.append(warp_stone)` (will add an Warp Stone to the "Consumables")  

If you want to remove an item, use the remove method:  
`player.items.remove(warp_stone)`
##### Valuables
"Valuables" got the type `valuable` in the items list.  
You can add valuable to your "Consumables", but they can not be used.  
To add a valuable item, use this command:  
`player.valuables.append(fabric_leaf)`  

To remove, like before:  
`player.valuables.remove(fabric_leaf)`
##### Outfits
Only `fox` and `knight` got both a list named `dresses`.  
Yomi's list can only be filled with items type `fox`.  
`fox.dresses.append(fox_bikini)`  
`fox.dresses.remove(fox_bikini)`

Ceri's list can only be filled with items type `knight`.  
`knight.dresses.append(knight_bikini)`  
`knight.dresses.remove(knight_bikini)`

[Full items list](#items-list)

### Add or remove companions
**Be careful, some actors like Ceri(knight) can't be removed! Always save before you add someone!**  

There are two objects, `party` and `backup`.  
You can execute two methods on both objects, `append` and `remove`.  
**Get sure that your `party` isn't full before you add someone!**  
Example:  
`backup.append(bunny)` will add a bunny to your "BackUp".  
Then you can remove a bunny with  
`backup.remove(bunny)`  
same with `party`.

## Actors list
[Full actors (characters) list](https://docs.google.com/spreadsheets/d/12vLrKiqmfnh0nwrKD5HbC9Qk7lWj77fPff1_-cSj5Os) (Google Table)

## Items list
[Full items list](https://docs.google.com/spreadsheets/d/1ZtdCNY44I7SRhcCkU0ZzTvG5PptmZHj4Kfen7Lh2p8M) (Google Table)

## Credits
[Guys from CE Forum](http://forum.cheatengine.org/viewtopic.php?t=592226)  
[happybrother](http://forum.cheatengine.org/profile.php?mode=viewprofile&u=391862) for hint about console commands.  
[glebsa](http://forum.cheatengine.org/profile.php?mode=viewprofile&u=448688) for actors info.  
