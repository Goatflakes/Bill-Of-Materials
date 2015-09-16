### Basic Parts
 Parts which can not be broken down in to further subassemblies.

### Bill of materials
 A directed acyclic graph (DAG) representing the hierarchical break down
 of all materials used in the construction of a desired end product. It is
 hierarchical because the desired end product may contain a collection of
 subassemblies which themselves consist of a collection of further
 subassemblies.
 
 Although this describes a tree, it becomes a DAG because each assembly may
 consist of multiple instance of the same subassembly. For instance a car
 might have several of the same screw in any of its many subassemblies.
 The leaf nodes in the DAG represent the most primitive items or basic
 parts. Usually enumerating the basic parts is what is required. Sometimes
 however it is not. For instance we may have several already completed
 subassemblies on hand and wish to use those first before making new
 subassemblies from the basic parts.

### Block
 In [Minecraft](###Minecraft) the world is constructed of 1 meter cubes called
 blocks. As well as being pregenerated in the Minecraft world, blocks are also
 available as placable items.
 
### Botania
 A botanical magic style [mod](###Mods) for [Minecraft](###Minecraft) by @Vazkii
 with a focus on automation and making life easier for the player.
 https://github.com/Vazkii/Botania

### Breakdown
 An list of requirements to build an item or set of items. It is the recursive
 expansion of the subassemblies or ingredients of a recipe, down to a certain
 desired level.
 
 It may be broken down to the level of [basic parts](###Basic-Parts) or it may be
 some higher level, for instance down to a set of [on hand](###On-Hand) 
 subassemblies. Once one of these subassemblies is found, one is removed from 
 the set of on hand parts and added to the breakdown or requirement set. That 
 subassembly is not further expanded, but the other ingredients will be.
 
 Expansion of remaining parts then proceeds until either they are found in the
 set of on hand items or until basic parts are reached. If basic parts are
 reached there are two possibilities.
   1. the basic part is on hand, in which case they are handled the same as
   other on hand items, that is removed from on hand and added to the breakdown
   2. they are not on hand, in which case they are added to the set of parts
   required but not on hand, and also added to the breakdown.

 It may also be useful to allow breakdowns to stop at non basic parts that are 
 not necessarily on hand. In that case if such a part is encountered but not on
 hand it will be added to the list of required but not on hand parts rather
 than proceeding to a full breakdown to basic parts.
 
 Finally, it may be useful in the last case to attempt to break down to basic
 parts, but if the required basic parts are not on hand, to add the listed non
 basic part rather than the full breakdown to basic parts.

### Entity
 Actors in the [Minecraft](###Minecraft) game. This includes anything present in 
 game that either isn't an [item](###Item) in an [inventory](Inventory) or that
 can't be represented as a [block](###Block) that is the same as all other blocks
 of its type. They can be tied to a block position such as a treasure chest.
 These are called "tile entities" and are a special kind of block. They can
 even take up multiple blocks and are then usually referred to as "multiblocks.
 
 Or they can be free to move around like the player, animals, boats, falling
 sand or gravel, items thrown on the ground, experience orbs, monsters, passive
 animals like pigs and even villagers. These are all simply referred to as
 entities.

### Fuel
 In [Minecraft](###Minecraft) A combustible material. Solid versions exist in
 [vanilla](###Vanilla) as and [mods](###Mods) add them as well. Many different
 liquid fuels exist in mods as well.
 
 Most [machines](###Machine) require either a solid or a liquid fuel to operate
 or else they  can receive [power](###Power) directly, although some machines
 operate without any fuel or power.
 
 Machines that need power or fuel to operate typically only support one way 
 or the other, and typically the ones that take fuel only either solid fuel
 or liquid fuel. Some are even more fussy. For instance the small coal
 boiler from [Gregtech](###Gregtech) can only take coal, coal blocks or charcoal.
 
 Solid fuels burn for a given number of [ticks](###Tick). In a normal 
 [furnace](###Furnace) an item takes 10s or 200 ticks to smelt. The typical fuel,
 coal or charcoal, can heat a furnace for 1600 ticks or 80s, thus smelting 8
 items in a regular furnace.
 
 It may be useful to track how much fuel is used in the production of a
 particularly complex build. The most convenient unit might be ticks, seconds,
 or number of "smelts" in a [vanilla](###Vanilla) furnace. Or more likely
 equivalents pieces of coal consumed.
 
 Note that different [modded](###Mods) furnaces are often more efficient,
 so if they are available, the fuel might well be discounted.
 
### Furnace
 A basic [block](###Block) or [machine](###Machine) in [Minecraft](###Minecraft). A 
 furnace consumes solid [fuel](###Fuel)  to smelt items into a more usable state.
 For instance raw pork to pork chops and iron ore to iron [ingots](###Ingot).

### Gregtech
 A technical style [Minecraft](###Minecraft) [mod](###Mods) written by @GregoriusT,
 with a focus on extending game play into multiple tiers of technology.
 http://forum.industrial-craft.net/?page=Thread&threadID=7156

### Hit Box
 The geometrical object around an in game object that is tested for 
 collision detection.

### Ingot
 In [Minecraft](###Minecraft) metallic [ores](###Ore) are melted down or
 otherwise processed into [items](###Items) called ingots.
 
 Although ingots have a [recipe](###Recipe), in many cases it makes more sense to
 consider the ingot the [basic part](###Basic-Part) when dealing with metals.
 
 Ingots can be broken down or created 9 smaller items called *nuggets* and can 
 usually be made into a placable [block](###Block) form, although depending on
 what [mods](###Mods) are installed, a [machine](###Machine) might be necessary to
 do any of these steps.

### Ingredient
 A subassembly in a [recipe](###Recipe). It may be a [basic part](###Basic-Part) or
 it may have one or more recipes for its production. These alternatives must be
 considered and a list of sensible recipes returned for the user to choose
 from.
 
 Ingredients may be consumed in the making of the recipe or they may just be
 necessary equipment that is returned unharmed. They might be equipment that
 looses durability when making the recipe, but is still returned if not
 completely worn out.
 
### Item
 A material object in [Minecraft](###Minecraft) that doesn't currently represent
 an [entity](###Entity) or a placed [block](###Block). Items exist in an inventory
 or used as crafting [ingredients](###Ingredients). Some can be worn, some eaten,
 some used as tools. These sorts of items often have durability and other data
 which distinguishes them from other items of the same type. Others are simply
 blocks waiting to be placed. Both kinds find use in crafting other items.
 
 ### Machine
 In [Minecraft](###Minecraft), Usually a tile [entity](###Entity), that either
 provides some sort of processing of raw materials to the player, or that
 automates the same. The [furnace](###Furnace) is the simplest example of a
 machine. The processing step the machine does can be considered a
 [recipe](###Recipe)
 
 To complete a recipe, Machines typically require [power](###Power) or
 [fuel](###Fuel) as  well as material inputs in the form of [items](###Items).
 They may also require a variety of liquids, [Thaumcraft](###Thaumcraft)
 essentia or other inputs as well. All these things Should properly be
 considered part of the recipe. 
 
 The use of a machine to complete recipe needs to be tracked so it is possible
 to filter out recipes that require a machine that the player doesn't yet have.
 A machine therefore constitutes a non-consumable [ingredient](###Ingredient).

### Minecraft
 A popular sandbox construction and exploration game produced by Mojang and
 originally authored by Markus "Notch" Persson @notch.
 
 Every static piece of geometry is a is a 1 meter cube, called a
 [block](###Block). The player builds things by placing, collecting, processing
 and destroying these blocks.
 
 The player does this by crafting (items)[#Items] and blocks made from
 resources gathered by breaking blocks. Items can also be found on enemies or
 even traded with villagers.
 
 Some geometry appears to be are smaller than the 1m cube, both
 visually and their [hit box](###Hit-Box), but still, nothing else can fit in
 the same cubic position, so in effect they fill up the entire 1m cube.
 
 Also present are a  variety of [entity](###Entities) which may or may not be
 tied to a particular collection of 1x1x1m cubes. Still, even the free moving
 entities are almost invariably constructed of cuboids, including the player.

### Mods
 A *modification* to [Minecraft](###Minecraft), often that adds
 [blocks](###Block), [items](###Items), (entities)(#Entities) or
 [machines](###Machine) or otherwise adds content and game play extensions or
 changes to the game.

### On Hand
 Parts available and already acquired.

### Ore
 In the Minecraft game metal is found usually by mining ores. They are then
 processed into [ingots](###Ingot). There are other non-metallic ores that may be
 processed differently, either by mining or by putting the mined block into a
 [machine](###Machine).
 
 At the start of the game, ores are typically processed in a 
 [furnace](###Furnace), which typically gives 1 ingot per ore. As the player
 progresses, they can build machines that give more ingots per ore.
 
### Power
 Many modded machines add some sort of power to run their machines. Over
 time there has also been some standardisation of power system across
 [mods](###Mods). For instance RF and EU. If necessary these power requirements
 can be tracked the same as other consumable [ingredients](###Ingredient).

 Some sources of power blur the line between fuel and power. For instance
 steam is a fluid that is consumed just like a liquid fuel. But it doesn't
 "burn" so it usually is considered a type of power rather than than a liquid
 fuel.
 
 There are other sorts of power such as Botania's mana and Thaumcraft vis,
 but these can be tracked just the same as other sorts of power or other
 consumable ingredient.
 
### Recipe
 A list of subassemblies that can be put together to make a desired end
 product.
 
### Thaumcraft
 A magic [mod](###Mods) for [Minecraft](###Minecraft) geared around alchemy,
 essences, golems, wands, staves, armour, magic mirrors, magical constructions
 and more. Written by @Azanor https://github.com/Azanor/thaumcraft
 
### Tick
The smallest possible quanta of time in [Minecraft](###Minecraft). A tick usually
happens twenty times per second, but may be less if the Minecraft server is
heavily loaded. But usually it can be considered to be 1/20th of a second.
 
### Vanilla
 [Minecraft](###Minecraft) without any additional [mods](###Mods).