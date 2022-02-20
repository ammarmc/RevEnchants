![image](https://user-images.githubusercontent.com/25089437/154840982-0632df3e-2bcb-4c98-8eb3-fdffb4e11b5d.png)
![image](https://user-images.githubusercontent.com/25089437/154840990-0047f1cf-4b39-41d0-8a9d-9b1a588dae8e.png)

![image](https://user-images.githubusercontent.com/25089437/154841002-2395170e-1313-4165-bb8a-12d961658f97.png)
### RevEnchants
- RevEnchants is minecraft plugin for multiple game modes one of them is prison

### Start

- open RevEnchantsPlus.zip 
- drag and drop jars to /plugins
- item-nbt-api-plugin-2.8.0.jar
- RevEnchantsPlus.jar
- RevWorldEditGuardApiOld
	- if you Server version 1.8 to 1.14
	- worldedit-bukkit-6.1.9
	- worldguard-6.2
- RevWorldEditGuardApiNew
	- if you Server version 1.14 - 1.18
	- worldedit-bukkit-7.2.6
	- worldguard-bukkit-7.0.5
- Restart the server
- open /plugins/RevEnchants/License.yml 
- setup your license key
- Restart


### Setup Mines
- get any Mines plugin 
	- Recommended and supported
		- JetsPrisonMines
		- PrisonMines
		- Mines
- Create the mine (must have region the same size as the mine)
  - select the mine with worldguard and do /rg create mine-a
  - now add the flags
    - /rg flag mine-a RevEnchants-Mine allow
    - /rg flag mine-a RevEnchants-Explosive allow
    - /rg flag mine-a RevEnchants-JackHammer allow

### Enchant Chance
  - most Enchants has Chance: and Increase-Chance-by: options
  - Chance: 1
    - is the chance that Enchants start with level 1
  - Increase-Chance-by: 0.1
    - is the chance that each level will increase chance with it
    - that will be  TotalChance = chance + (Increase-Chance-by * Level)
      - if level is 5 and Chance is 1 and Increase-Chance-by is 0.1
      - Total chance of level 5 will be 1.5

### Test Enchant Chance
  - use /re test EnchantsID BlocksAmount
  - example /re test Explosive 1000
  - this will show you current configuration and lot of information
  - ![image](https://user-images.githubusercontent.com/25089437/154818373-28a7e647-68ce-46f1-8108-805621587633.png)
  - this will show you if player has level 1 Explosive if he broke 1000 block
  - Explosive will work 24 at the current chance setup
  - ![image](https://user-images.githubusercontent.com/25089437/154818385-0eb89631-e123-4ead-a224-c983c7a1c9d4.png)
  - other levels info
  - ![image](https://user-images.githubusercontent.com/25089437/154818409-b8846ea3-8be5-4718-b6db-0abb021942bc.png)
  - ![image](https://user-images.githubusercontent.com/25089437/154818417-f630bf85-2ca2-4f74-b8d3-a4a11f99d16d.png)
  - ![image](https://user-images.githubusercontent.com/25089437/154818423-b382c529-8307-4b39-9727-5278ab8f247f.png)
  - ![image](https://user-images.githubusercontent.com/25089437/154818430-a444c474-3ae2-4c66-8294-ea2a134cfd93.png)

### setup Currency.yml
  - to create new Currency just copy Option 1 or 2
  - ID: is the id of the token  (the ID reference of the token)
  - Commands   player type to access token  

### Enchants slots 
  - unlock ability to buy new Enchants
  - you can disable it or enable it in Enchants.yml 
  - Start: 2 this option is how many slots pickaxe start with
  - Max: 9 is the maximum amount of slots
  - you can obtain slots using /re Enchantslots player Amount
  - you can add slots to create/store or give them when player Prestige
### Shard slots 
  - unlock new slot to have more shards on the pickaxe
  - you can disable it or enable it in Shards.yml 
  - Start: 2 this option is how many slots pickaxe start with
  - Max: 6 is the maximum amount of slots
  - you can obtain slots using /re shardslots player Amount
  - you can add slots to create/store or give them when player Prestige
### Energy
  - it's a system to level up your pickaxe
  - you can disable it or enable it in Energy.yml 
  - Start: 1000 this option is how much energy you need to level up to the next level
  - Increase: 500 how much next level coset increase by
  - Percentage: true increase cost by percentage if its set to true
### Level
  - Max: 100 what is the maximum level of the pickaxe
  - to disable this just remove the placeholder from the Lore
  - you can execute commands on level up or give them a slots
  - ![image](https://user-images.githubusercontent.com/25089437/154839955-1119df9e-b527-4036-ad7d-6b152331e8c2.png)
### CustomDurability
  - you can disable it or enable it in CustomDurability.yml 
  - Start: 1000 this option is how much Durability pickaxe start with
  - Increase-by-level: 1000  it's time they buy unbreaking enchantment to increase by this
### LuckyBlock
  - when player break specific block like sponge 
  - it's going to execute commands 
  - you can disable it or enable it in LuckyBlock.yml 
### Drops
  - you can disable it or enable it in Drops.yml 
  - Enabled if you enable this RevEnchants will handle the blocks drop
  - FixDrops: true this option will fix ores like coal and redstone and lapis lazuli to not drop more then one item
  - Change:  Enabled if you enable this you can change specific drop 
  -  on my server i have coalore drop coal ore not coal 
  -  ![image](https://user-images.githubusercontent.com/25089437/154840339-e4041863-35ce-474d-81cd-bd0ab0d47295.png)
### Tools
  - Tools.yml to add more tools if you want like netherite pickaxe
### Lore
  - hear it depend on your settings which I recommend to do it the last
  - if you added more shards slots need to add Placeholder to the lore 
     - %Rev_Shard_4_Name% %Rev_Shard_4_Level%
     - %Rev_Shard_5_Name% %Rev_Shard_5_Level_Formatted%
     - %Rev_Shard_6_Name% %Rev_Shard_6_Level_Roman%
  - Enchants Lore Placeholder
     - %Rev_Enchant_Efficiency_Colour% get player enchants Colour
     - %Rev_Enchant_Efficiency_Name% get enchants Name
     - %Rev_Enchant_Efficiency_Level% get enchants Level
         - %Rev_Enchant_Efficiency_Level_Formatted%
         - %Rev_Enchant_Efficiency_Level_Roman%
  - I highly recommend you to remove placeholders that you did not use or are disabled from the lore
### LostShard
  - it's a way for the player to obtain random Shard
  - you can add LostShard to the crates or sell them on the store
  - you can disable it or enable it in LostShard.yml 
  - LostShard has the ability to create multiple tiers
  - when a player redeem it will give Random shard and level from the list of the tier
  - tier 1: (/re Lostshard player 1 1)  tier 2:  (/re Lostshard player 2 1)
  - ![image](https://user-images.githubusercontent.com/25089437/154840779-2d03325f-e844-4fca-9f66-7115a9098efb.png)
  - ![image](https://user-images.githubusercontent.com/25089437/154840824-d668e6bc-fb78-4b92-9748-709966d7f07a.png)
### questions

### API
  - [Download API](https://github.com/ammarmc/RevEnchants/raw/main/RevEnchantsApi.jar)
  - long getCurrency(OfflinePlayer p, String CurrencyID)
  - depositCurrency(OfflinePlayer p, long Amount,String CurrencyID, CurrencyReceiveReason Reason)
  - withdrawCurrency(OfflinePlayer p, long Amount,String CurrencyID)
  - setCurrency(OfflinePlayer p,long Amount,String CurrencyID)
  - String getCurrencyName(String CurrencyID)
  - String getCurrencySymbol(String CurrencyID)
      CurrencyID can be found is Currency.yml
      as RevEnchants has multiple currencies and also can create more
      this must be an option in your plugin config to get CurrencyID id or what Currency to use
      get players Currency Amount the have


 



