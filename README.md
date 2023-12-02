# AnturniaQuests  
**Overview:**
AnturniaQuests is a versatile quest plugin for Minecraft, allowing server administrators to create a personalized quest system. With this plugin, players can engage in captivating quests and earn exciting rewards. Configuration is straightforward, offering complete customization of quests and rewards.

**Features:**
- **Custom Quests:** Effortlessly create your own quests through an intuitive configuration file.
- **Rewards:** Define unique rewards for completed quests, ranging from items to experience points and currencies.
- **Categories:** Organize quests into different categories for improved visibility.
- **Menu System:** Players can view their available quests in-game and track their progress.
- **Configuration-Friendly:** All aspects of the plugin are customizable via the configuration file to meet your server's needs.

**Installation:**
1. Place the JAR file in your Spigot server's "plugins" folder.
2. If you want to use the money feature please follow the instructions under "Special Note for Monetary Rewards".
3. Start or restart your server.
4. Adjust the configuration file as needed.

**Commands:**
- `/quests`: Open the ingame quest menu.
- `/quests reload`: Reload the plugin configurations

**Permissions:**
- `quests.open`: permission to execute the /quests command
- `quests.admin.reload`: permission to execute the /quests reload command

**Special Note for Monetary Rewards:**
If you intend to provide monetary rewards, ensure you have Vault and a compatible economy plugin installed on your server. This allows seamless integration with in-game currency systems.

**Help and Support:**
Visit our [Discord server](https://discord.gg/89Dv8rqkpC) for assistance, feedback, and additional information.

**Feedback:**
We appreciate your feedback! Share your experiences, ideas, and suggestions on the [Discord server](https://discord.gg/89Dv8rqkpC).

**Images:**

![](https://i.imgur.com/x9SDfyR.png)
![](https://i.imgur.com/s7kweus.png)
![](https://i.imgur.com/gASsAKD.png)
![](https://i.imgur.com/U2UJC6p.png)
![](https://i.imgur.com/vLlW5TS.png)

**Configs:**

`config.yml`:
``` yml
database:
  type: sqlite #currently only sqlite is supported
```
`categories.yml`:
``` yml
combat:
  friendlyName: Combat
  description: You want to kill mobs? Here are the right quests for you!
  material: DIAMOND_SWORD
mining:
  friendlyName: Mining
  description: Just mine some stuff
  material: IRON_PICKAXE
farming:
  friendlyName: Farming
  description: You also like potatoes?
  material: GOLDEN_HOE
foraging:
  friendlyName: Foraging
  description: Everything can be made out of wood!
  material: JUNGLE_WOOD
```

`quests.yml`:
``` yml
combat1:
  friendlyName: Zombie Slayer
  description: The zombie apocalypse is upon us! Eliminate 20 zombies and collect
    their rotten flesh.
  category: combat
  oneTime: false
  requirements:
    ROTTEN_FLESH: 20
  rewards:
    IRON_SWORD: 1
    GOLDEN_APPLE: 2
    money: 60
combat2:
  friendlyName: Skeleton Archer
  description: Archery skills are no match for you! Defeat 30 skeletons and gather
    their bones for crafting purposes.
  category: combat
  requirements:
    BONE: 30
  rewards:
    BOW: 1
    ARROW: 32
    money: 60
combat3:
  friendlyName: Spider Exterminator
  description: Arachnophobia be gone! Annihilate 25 spiders and retrieve their eyes
    as trophies.
  category: combat
  announce: true
  requirements:
    SPIDER_EYE: 25
  rewards:
    IRON_CHESTPLATE: 1
    money: 20
#--------------------------------------------------------------
farming1:
  friendlyName: Wheat Farmer
  description: Become the master of agriculture! Cultivate and harvest 128 wheat to
    fill your granary.
  category: farming
  requirements:
    WHEAT: 128
    IRON_HOE: 1
  rewards:
    IRON_HOE: 1
    BREAD: 64
    money: 60
farming2:
  friendlyName: Melon Enthusiast
  description: The thirst quencher! Gather a bountiful harvest of 64 melons for a
    refreshing feast.
  category: farming
  requirements:
    MELON_SLICE: 64
  rewards:
    GOLDEN_AXE: 1
    GLISTERING_MELON_SLICE: 16
    money: 60
farming3:
  friendlyName: Carrot Harvest
  description: Dig deep into the earth! Harvest 96 carrots to create a carrot paradise.
  category: farming
  requirements:
    CARROT: 96
    IRON_SHOVEL: 1
  rewards:
    IRON_SHOVEL: 1
    GOLDEN_CARROT: 16
    money: 60
#--------------------------------------------------------------
foraging1:
  friendlyName: Wood Collector
  description: Embrace nature! Gather 256 logs of any type and become a master lumberjack.
  category: foraging
  requirements:
    OAK_LOG: 128
    SPRUCE_LOG: 64
    BIRCH_LOG: 32
    JUNGLE_LOG: 32
    ACACIA_LOG: 16
    DARK_OAK_LOG: 16
  rewards:
    DIAMOND_AXE: 1
    WOODEN_PLANKS: 512
    money: 60
foraging2:
  friendlyName: Berry Picker
  description: The forest is a treasure trove of delicious berries! Collect 128 sweet
    berries for a tasty treat.
  category: foraging
  requirements:
    SWEET_BERRIES: 128
  rewards:
    LEATHER_CHESTPLATE: 1
    SWEET_BERRIES: 64
foraging3:
  friendlyName: Flower Power
  description: Embrace the beauty of nature! Collect 64 different flowers and create
    a stunning garden.
  category: foraging
  requirements:
    DANDELION: 4
    POPPY: 4
    BLUE_ORCHID: 4
    ALLIUM: 4
    AZURE_BLUET: 4
    RED_TULIP: 4
    ORANGE_TULIP: 4
    WHITE_TULIP: 4
    PINK_TULIP: 4
    OXEYE_DAISY: 4
    CORN_FLOWER: 4
    LILY_OF_THE_VALLEY: 4
    WITHER_ROSE: 4
    SUNFLOWER: 4
    LILAC: 4
    ROSE_BUSH: 4
    PEONY: 4
  rewards:
    BONE_MEAL: 64
    FLOWER_POT: 4
#--------------------------------------------------------------
mining1:
  friendlyName: Coal Miner
  description: Descend into the depths! Mine 128 blocks of coal ore to fuel your adventures.
  category: mining
  requirements:
    COAL: 128
  rewards:
    TORCH: 128
    COAL_BLOCK: 8
mining2:
  friendlyName: Iron Seeker
  description: Iron is the backbone of any thriving civilization. Mine 64 iron ore
    to bolster your resources.
  category: mining
  requirements:
    IRON_ORE: 64
  rewards:
    IRON_PICKAXE: 1
    IRON_INGOT: 64
mining3:
  friendlyName: Diamond Prospector
  description: Diamonds are a miner's best friend. Unearth 16 diamonds to add sparkle
    to your collection.
  category: mining
  requirements:
    DIAMOND: 16
  rewards:
    DIAMOND_PICKAXE: 1
    DIAMOND: 16
#--------------------------------------------------------------
```

**bStats:**
![Bstats](https://bstats.org/signatures/bukkit/AnturniaQuests.svg)
