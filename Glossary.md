### Bill of materials
 : A [directed acyclic graph] (DAG) representing the hierarchical break down
 of all materials used in the construction of a desired end product. It is 
 hierarchical because the desired end product may contain a collection of
 subassemblies which themselves consist of a collection of further
 subassemblies.
 : Although this describes a tree, it becomes a DAG because each assembly may 
 consist of multiple instance of the same subassembly. For instance a car
 might have several of the same screw in any of its many subassemblies.
 : The leaf nodes in the DAG represent the most primitive items or basic
 parts. Usually enumerating the basic parts is what is required. Sometimes
 however it is not. For instance we may have several already completed subassemblies on hand and wish to use those first before making new
 subassemblies from the basic parts.

### Block
 : In [Minecraft] the world is constructed of 1 meter cubes called blocks.
 As well as being pregenerated in the Minecraft world, blocks are also 
 available as placable items.
 
### Botania
 : A botanical magic style [mod] for [Minecraft] by @Vazkii with a focus on
 on automation and making life easier for the player.
 https://github.com/Vazkii/Botania

### Entity
 : Actors in the [Minecraft] game. This includes anything that can't be
 represented as a block that is the same as all other blocks of its type. They
 can be tied to a block position such as a treasure chest. These are called
 "tile entities". Or they can be free to move around like the player, animals,
 boats, falling sand or gravel and monsters. These are simply referred to as 
 entities.

### Fuel
 : In [Minecraft] A combustible material. Solid versions exist in [vanilla]
 as and mods add them as well. Many different liquid fuels exist in [mods].
 Most [machines] require either a solid or a liquid fuel to operate or else
 they  can receive [power] directly, although some machines operate without
 any fuel or power.
 : Machines that need power or fuel to operate typically only support one way 
 or the other, and typically the ones that take fuel only either solid fuel
 or liquid fuel. Some are even more fussy. For instance the small coal 
 boiler from [Gregtech] can only take coal, coal blocks or charcoal.
 : Solid fuels burn for a given number of [ticks]. In a normal [furnace] an 
 item takes 10s or 200 ticks to smelt. The typical fuel, coal or charcoal,
 can heat a furnace for 1600 ticks or 80s, thus smelting 8 items in a regular
 furnace.
 : It may be useful to track how much fuel is used in the production of a
 particularly complex build. The most convenient unit might be ticks, seconds,
 or number of "smelts" in a [vanilla] furnace. Or more likely equivalents of
 pieces of coal consumed.
 : Note that different [modded Minecraft] furnaces are often more efficient,
 so if they are available, the fuel might well be discounted.
 
### Furnace
 : A basic [block] or [machine] in [Minecraft]. A furnace consumes solid
 [fuel]  to smelt items into a more usable state. For instance raw pork to
 pork chops and iron ore to iron [ingots]

### Gregtech
 : A technical style [Minecraft] [mod] written by @GregoriusT, with a focus on
 extending game play into multiple tiers of technology.
 http://forum.industrial-craft.net/?page=Thread&threadID=7156

### Hit Box
 : The geometrical object around an in game object that is tested for 
 collision detection.

### Ingot
 : In [Minecraft] metallic [ores] are melted down into ingots. These are 
 usually considered the basic material unit when dealing with a metal, even 
 though they have a recipe to make them. Ingots can be broken down into 9
 [nugget]s, perhaps requiring smelting in a [furnace]. Usually 9 ingots can be
 combined into a placable [block] of the metal, although depending on what
 [mods] are installed, a [machine] might be necessary to do this.

### Ingredient
 : A subassembly in a [recipe]. It may be a [basic part] or it may have one or
 more recipes for its production. These alternatives must be considered and
 a list of sensible recipes returned for the user to choose from.
 : Ingredients may be consumed in the making of the recipe or they may just be
 necessary equipment that is returned unharmed. They might be equipment that
 looses durability when making the recipe, but is still returned if not
 completely worn out.

### Machine
 : In [Minecraft], Usually a block, that either provides some sort of
 processing of raw materials to the player, or that automates the same. The 
 [furnace] is the simplest example of a machine. Machines typically require
 [power] or [fuel] as  well as material inputs. They may also require liquids,
 essentia or other inputs as well.
 : The use of a machine needs to be tracked so it is possible to filter out
 recipes that require a machine that the player doesn't yet have. A machine
 therefore constitutes a non-consumable [ingredient].

### Minecraft
 : A popular sandbox construction and exploration game produced by Mojang and 
 originally authored by Markus "Notch" Persson @notch. Every static in item
 is a 1 meter cube, called a [block]. The player builds things by placing and 
 destroying these blocks. Some items are smaller than the 1m cube, both 
 visually and in their [hit box], but still, nothing else can now fit in that
 position, so in effect they fill up the entire 1m cube. Also present are a
 variety of [entity](entities) which may or may not be tied to a particular
 1x1x1m cube. Still, even these are almost invariably constructed of cuboids.

### Mods
 : A *modification* to [Minecraft], often that adds [blocks] and [machines]
 and other content to the game and that changes game play.

### Ore
 : In the Minecraft game metal is found usually by mining ores. They are then
 processed into [ingots]. There are other non-metallic ores that may be
 processed differently, either by mining or by putting the mined block into a
 [machine].
 
### Power
 : Many modded machines add some sort of power to run their machines. Over
 time there has also been some standardisation of power system across [mods].
 For instance RF and EU. If necessary these can be tracked the same as other
 consumable [ingredients].
 : Some sources of power blur the line between fuel and power. For instance
 steam is a fluid that is consumed just like a liquid fuel. But it doesn't
 "burn" so it usually is considered a type of power rather than than a liquid
 fuel.
 : There are other sorts of power such as Botania's mana and Thaumcraft vis,
 but these can be tracked just the same as other sorts of power or other
 consumable ingredient.
 
### Recipe
 : A list of subassemblies that can be put together to make a desired end
 product.
 
### Thaumcraft
 : A magic [mod] for [Minecraft] geared around alchemy, golems, wands, staves,
 armour, magic mirrors, magical constructions and more. Written by @Azanor
 https://github.com/Azanor/thaumcraft
 
### Vanilla
 : [Minecraft] without any additional [mods].