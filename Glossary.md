### Basic Part
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
 In [Minecraft](#minecraft) the world is constructed of 1 meter cubes called
 blocks. As well as being pregenerated in the Minecraft world, blocks are also
 available as placable items.
 
### Botania
 A botanical magic style [mod](#mod) for [Minecraft](#minecraft) by @Vazkii
 with a focus on automation and making life easier for the player.
 https://github.com/Vazkii/Botania

### Breakdown
 An list of requirements to build an item or set of items. It is the recursive
 expansion of the subassemblies or ingredients of a recipe, down to a certain
 desired level.
 
 It may be broken down to the level of [basic parts](#basic-part) or it may be
 some higher level, for instance down to a set of [on hand](#on-hand) 
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
 Actors in the [Minecraft](#minecraft) game. This includes anything present in 
 game that either isn't an [item](#item) in an [inventory](#inventory) or that
 can't be represented as a [block](#block) that is the same as all other blocks
 of its type. They can be tied to a block position such as a treasure chest.
 These are called "tile entities" and are a special kind of block. They can
 even take up multiple blocks and are then usually referred to as "multiblocks.
 
 Or they can be free to move around like the player, animals, boats, falling
 sand or gravel, items thrown on the ground, experience orbs, monsters, passive
 animals like pigs and even villagers. These are all simply referred to as
 entities.

### Fuel
 In [Minecraft](#minecraft) a combustible material. Solid versions exist in
 [vanilla](#vanilla) as and [mods](#mod) add them as well. Many different
 liquid fuels exist in mods as well.
 
 Most [machines](#machine) require either a solid or a liquid fuel to operate
 or else they  can receive [power](#power) directly, although some machines
 operate without any fuel or power.
 
 Machines that need power or fuel to operate typically only support one way 
 or the other, and typically the ones that take fuel only either solid fuel
 or liquid fuel. Some are even more fussy. For instance the small coal
 boiler from [Gregtech](#gregtech) can only take coal, coal blocks or charcoal.
 
 Solid fuels burn for a given number of [ticks](#tick). In a normal 
 [furnace](#furnace) an item takes 10s or 200 ticks to smelt. The typical fuel,
 coal or charcoal, can heat a furnace for 1600 ticks or 80s, thus smelting 8
 items in a regular furnace.
 
 It may be useful to track how much fuel is used in the production of a
 particularly complex build. The most convenient unit might be ticks, seconds,
 or number of "smelts" in a [vanilla](#vanilla) furnace. Or more likely
 equivalents pieces of coal consumed.
 
 Note that different [modded](#mod) furnaces are often more efficient,
 so if they are available, the fuel might well be discounted.
 
### Furnace
 A basic [block](#block) or [machine](#machine) in [Minecraft](#minecraft). A 
 furnace consumes solid [fuel](#fuel)  to smelt items into a more usable state.
 For instance raw pork to pork chops and iron ore to iron [ingots](#ingot).

### Gregtech
 A technical style [Minecraft](#minecraft) [mod](#mod) written by @GregoriusT,
 with a focus on extending game play into multiple tiers of technology.
 http://forum.industrial-craft.net/?page=Thread&threadID=7156

### Hit Box
 The geometrical object around an in game object that is tested for 
 collision detection.

### Ingot
 In [Minecraft](#minecraft) metallic [ores](#ore) are melted down or
 otherwise processed into [items](#item) called ingots.
 
 Although ingots have a [recipe](#recipe), in many cases it makes more sense to
 consider the ingot the [basic part](#basic-part) when dealing with metals.
 
 Ingots can be reversibly broken down into 9 smaller items called *nuggets*
 and can usually be reversibly made into a placable [block](#block) form, 
 although depending on what [mods](#mod) are installed, a 
 [machine](#machine) might be necessary to accomplish any of these steps for
 some metals.

### Ingredient
 A subassembly in a [recipe](#recipe). It may be a [basic part](#basic-part) or
 it may have one or more recipes for its production. These alternatives must be
 considered and a list of sensible recipes returned for the user to choose
 from.
 
 Ingredients may be consumed in the making of the recipe or they may just be
 necessary equipment that is returned unharmed. They might be equipment that
 looses durability when making the recipe, but that is is still returned if not
 completely worn out.
 
### Inventory
 A container to store [items](#item). The player has a personal inventory. The
 input, output and solid fuel slots of a [machine](machine) are considered
 inventories.

### Item
 A material object in [Minecraft](#minecraft) that doesn't currently represent
 an [entity](#entity) or a placed [block](#block). Items exist in an inventory
 and can be used as crafting [ingredients](#ingredients). Some can be worn,
 eaten, used as tools, etc. These sorts of items often have durability and
 other data which distinguishes them from other items of the same type. Others
 are simply blocks waiting to be placed. Both kinds find use in crafting other 
 items, including the crafting of placable blocks and [machines](#machine).
 
### Machine
 In [Minecraft](#minecraft), Usually a tile [entity](#entity), that either
 provides some sort of processing of raw materials to the player, or that
 automates the same. The [furnace](#furnace) is the simplest example of a
 machine. The processing step the machine does can be considered a
 [recipe](#recipe)
 
 To complete a recipe, Machines typically require [power](#power) or
 [fuel](#fuel) as  well as material inputs in the form of [items](#items).
 They may also require a variety of liquids, [Thaumcraft](#thaumcraft)
 essentia or vis or other inputs as well. All these things Should properly be
 considered part of the recipe. 
 
 The use of a machine to complete a recipe needs to be tracked so it is
 possible to filter out recipes that require a machine that the player doesn't
 yet have. A machine therefore constitutes a non-consumable
 [ingredient](#ingredient).

### Minecraft
 A popular sandbox construction and exploration game produced by Mojang and
 originally authored by Markus "Notch" Persson @notch.
 
 Every static piece of geometry is a is a 1 meter cube, called a
 [block](#block). The player builds things by placing, collecting, processing
 and destroying these blocks.
 
 The player does this by crafting (items)[#items] and blocks made from
 resources gathered by breaking blocks. Items can also be found on enemies or
 even traded with villagers.
 
 Some geometry appears to be are smaller than the 1m cube, both
 visually and their [hit box](#hit-box), but still, nothing else can fit in
 the same cubic position, so in effect they fill up the entire 1m cube.
 
 Also present are a  variety of [entity](#entities) which may or may not be
 tied to a particular collection of 1x1x1m cubes. Still, even the free moving
 entities are almost invariably constructed of cuboids, including the player.

### Mod
 A *modification* to [Minecraft](#minecraft) that adds [blocks](#block),
 [items](#item), [entities](#entity) or [machines](#machine) or otherwise adds
 content and game play extensions or changes to the game.

### On Hand
 Parts available and already acquired.

### Ore
 In the Minecraft game metal is found usually by mining ores. They are then
 processed into [ingots](#ingot). There are other non-metallic ores that may be
 processed differently, either by mining or by putting the mined block into a
 [machine](#machine).
 
 At the start of the game, ores are typically processed in a 
 [furnace](#furnace), which typically gives 1 ingot per ore. As the player
 progresses, they can build machines that give more ingots per ore.
 
### Power
 Many modded machines add some sort of power to run their machines. Over
 time there has also been some standardisation of power system across
 [mods](#mod). For instance RF and EU. If necessary these power requirements
 can be tracked the same as other consumable [ingredients](#ingredient).

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
 A magic [mod](#mod) for [Minecraft](#minecraft) geared around alchemy,
 essences, golems, wands, staves, armour, magic mirrors, magical constructions
 and more. Written by @Azanor https://github.com/Azanor/thaumcraft
 
### Tick
The smallest possible quanta of time in [Minecraft](#minecraft). A tick usually
happens twenty times per second, but may be less if the Minecraft server is
heavily loaded. But usually it can be considered to be 1/20th of a second.
 
### Vanilla
 [Minecraft](#minecraft) without any additional [mods](#mod).