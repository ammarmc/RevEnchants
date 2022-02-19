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
  - Max: 9 is the maximum amount of slots
  - you can obtain slots using /re shardslots player Amount
  - you can add slots to create/store or give them when player Prestige




  
  
