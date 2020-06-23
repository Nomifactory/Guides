Made by UhahaUhaha#7789

Valid for Omnifactory 1.2.2

# What is PAuto, why is it in pack and how do I use it

Omnifactory involves a lot of automation tasks that can't be done with pure AE2. If you have troubles with Extended Crafting tables automation, don't know how to encode recipes with 10 or more ingredients or can't parallelize your alloy smelters (or any other machine that needs 2 different inputs), this guide is for you!
### Recipes with 10 (or more) different items
That's recipe of LuV field generator:

![LuV field generator](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/Screenshot_1.png?raw=true)

As you can see, you won't be able to encode this recipe with ME pattern terminal. You can build workarounds like prestocking osmium wires in assembly line, but there are also another recipes, so you will need dedicated ALs for each recipe. PackagedAuto will allow you to automate these recipes without any overcomplicated workarounds!

This is your setup for automating AL. The main things are packager, unpackager, crafting CPU and package recipe encoder. Swap their places, make CPU bigger, use another terminal, place another inventory instead of storage crate. Make any adjustements, but be sure that everything is connected and there is inventory for routing stuff into AL near unpackager

![ME system for AL](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/2020-06-23_14.38.17.png?raw=true)

In total, you will need 1 packager, 1 unpackager, package recipe encoder and 2 package recipe holders. Connect packager and unpackager to ME network (preferably with cables because ME conduits can get disconnected from full block devices on world reloads) and place encoder nearby (or not nearby, but then you will have to run between packager and encoder). Open GUI of encoder. It can be confusing at first, but you should just get used to it.

![Encoder GUI](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/2020-06-23_14.32.25.png?raw=true)

Encoder GUI contains several things:

1. Slot for recipe encoder. You will need two for AL, so place both there
2. Slots for recipes. When you will encode recipe, encoded output will appear there
3. Button for saving encoded recipes into holders. Don't forget to click it after encoding recipes!
4. Button for moving recipes from holders into encoder. Useful when you want to change old recipe or add new one
5. Slots for recipe ingredients. Each slot can contain one stack of item, so whole recipe can contain 81 different stacks of items
6. Type of recipe. I will explain it in another part of guide
7. Outputs of recipe. Each PAuto recipe can produce up to 9 items, but now you will need only one
8. Used packages. Each package will contain set of up to 9 items, so every 9 stacks will be contained in one package.

Choose processing recipe and insert recipe holders into 1 slot. Open recipe that you need to encode (for me it's LuV field generator) and click [+]

![Move items](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/2020-06-23_14.47.53.png?raw=true)

Recipe will be inserted into encoder. Change it if you need (for LuV field generator I will want to insert wetware and crystal circuits instead of processors, arrays or mainframes) and click on "Save" button.

![Encoded AL recipe](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/2020-06-23_14.49.31.png?raw=true)

As you can see this recipe will be divided in 2 packages because it has 12 input stacks. Take encoded recipe holders (they should have glowing dot in middle) and place one of them into packager. 

![Packager](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/Screenshot_2.png?raw=true)

If you saved recipe and connected packager to ME, you should be able to see two craftable packages in your ME terminal.

![craftable packages](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/Screenshot_3.png?raw=true)

You can even try to order them! If you will be fast enough, you can see how packager will take items from ME system and package them into one paper box.

*Everything in italics is not neccessary and should be done just to understand how PAuto works.*

*Take one package from ME storage and insert it into unpackager. You will see one green and one red dot.*

![Unpackager missing package](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/Screenshot_4.png?raw=true)

*Unpackager can unpackage items only when it has full set of packages. You inserted only one of them; it's indicated by green dot. It's missing another one; it's indicated by red dot. Take another package (packages have indexes on them, 0 is first one, 2 is second,...) and insert it into unpackager. If there won't be inventory near it, unpackager will have 2 green dots.*

![Unpackager with two packages](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/Screenshot_5.png?raw=true)

*Place any storage block near unpackager (crate, chest, anything that you want) and it will unpackage items there.*

![Unpackaged into crate](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/2020-06-23_14.56.21.png?raw=true)

That was interesting, but should you insert packages in unpackager manually? No! Place second recipe holder in unpackager. If unpackager connected to ME, you will see your item craftable in ME terminal (I will see LuV field generator).

![LuV craftable generator](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/Screenshot_6.png?raw=true)

Try to order it. AE2 will craft packages and then put them in unpackager automatically. Unpackager will output contents of packages into adjacent inventory, from where you can route everything into AL (or let that inventory be all input buses of AL with AA item lasers).

![AE2 crafting LuV generator](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/Screenshot_7.png?raw=true)

### Extended crafting and AA empowering

Extended crafting has automation interface and AA empowering is also automatable, so why should you even bother with this part? Automation interfaces are buggy (they can void or dupe outputs), AA empowerer is hard to automate and slow, and parallelizing of empowering will be too boring. PExC (PackagedExtended Crafting) will provide you with solutions of both problem! You will need packager, unpackager, 2 recipe holders and package crafter for each type of table.

![ME system for PExC](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/2020-06-23_15.02.57.png?raw=true)

Do you recall recipe types from first part of this guide? If you click on furnace button in recipe encoder GUI, it will cycle between recipe modes. There are 3 modes for every ExCrafting table, 1 mode for combination crafter (in this pack it's faster AA empowerer) and processing mode for every other machine.

If you want to encode recipe, change recipe type, open JEI and press [+] near needed recipe. I will automate T7 microminer, ultimate material, crystaltine ingot and empowered palis block.

![Ultimate material](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/2020-06-23_15.06.50.png?raw=true)

![Crystaltine](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/2020-06-23_15.07.37.png?raw=true)

![Palis](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/2020-06-23_15.10.01.png?raw=true)

![Draconium plated MM](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/2020-06-23_15.10.17.png?raw=true)

Place recipe holders into packagers and unpackagers, but be sure that unpackager with [insert type of table] recipe placed near [insert the same type of table] package crafter. Package crafters will output directly into connected ME network, so there is no need in placing additional conduits. Also note that combination package crafter needs external energy connection and 4 marked pedestals in 3 block radius around it.

Valid positions for marked pedestals:

![markedpedestals](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/2020-06-23_15.20.08.png?raw=true)

If everything encoded and connected properly, you will see packages and items as craftable. You can order them!

![PExC craftable](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/Screenshot_8.png?raw=true)

Combination crafter performs empowering really fast (10 ticks if you can provide it with energy), but other crafters are quite slow (10 seconds per recipe). But they are perfect for parallelizing! Place mutliple crafters around one unpackager (up to 6) and recipes will go to all of them.

### Alloy smelters (or anything else with multiple inputs) parallelizing

You (most probably) will want to parallelize your on-demand machines at some point (or you can just wait for all your sunnarium in one alloy smelter if you really want). Wiremills, cutting machines and cluster mills are easy to parallelize (buffer inventory and EIO conduits with round robin enabled), but alloy smelters are definitely not. If you will use EIO conduits with round robin, they will send 5 ingots in one smelter, 10 in another and leave third smelter empty. Also AE2 blocking mode doesn't work properly with GT machines, so you will need to make something on your own.

I present you PAuto! You will need EIO item conduits, extract speed downgrade, one packager and one recipe holder per 20 recipes, buffer inventory, one interface per 9 recipes, one AE2 pattern per recipe, x unpackagers and x machines, where x - amount of machines you want to have parallelized.

Set everything as shown on this picture. Interface pointing into buffer chest, conduits with extraction downgrade and round robin enabled distributing items into unpackagers, unpackagers placed near alloy smelters. Connect RF energy to unpackagers and EU energy to alloy smelters.

![Setting up alloy smelters](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/2020-06-23_15.30.35.png?raw=true)

Open recipe encoder, choose processing recipe, [+] needed recipe from JEI. I will pattern sunnarium because it's really slow.

![Sunnarium recipe](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/Screenshot_9.png?raw=true)

Encode all recipes you want to have (make another holder if 20 recipes is not enough) and place holders into packagers (make sure to connect them to ME). You will see packages in terminal (third time in this guide, wow). Order one and make pattern in pattern terminal Package with ingredients -> result of processing

![pattern](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/Screenshot_10.png?raw=true)

Insert this pattern into interface pointing into buffer chest and order 100 items. If everything is right, you will see how your smelters turn on making their job.

![Alloy smelters are working](https://github.com/UhahaUhaha/OmnifactoryGuides/blob/1.2.2/guides/files/HowToPAuto/2020-06-23_15.32.38.png?raw=true)

### Small tips

I told you about most common uses of PAuto in this pack. I will also give you some tips for further experiments with this mod.

* You can place packages in another package recipes. This way you can parallelize assembly lines post-tank (if you are parallelizing pre-tank... What are you trying to achieve?)
* Unpackagers can work without recipe holders, but they won't be able to automatically get recipes from ME system (I explained it in first part in *italics*). Packagers must have holders to work
* While packagers are not really slow, their speed can be not enough for some setups. Place packager extensions in ring around packager to speed it. If packager with 18 extensions is still not enough, second packager with the same holder will be used to parallelize packaging if it is connected to ME
* PAuto devices can have some troubles with connecting to ME. If you place it near existing ME cable in large network, it won't connect. Place PAuto device first, and then connect cable to it.

That's it. PAuto is really good (but not perfect) addon for AE2. I hope you will have great time using it for your automation.
