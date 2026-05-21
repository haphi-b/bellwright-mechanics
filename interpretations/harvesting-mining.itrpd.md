# Harvesting and mining
## Trees
- Young Trees: 
   - can be hit 3 times giving 1-2 wood each time
- normal trees 
   - need 7 hits to be felled
   - 8 hits to cut a log
   - independent of weapon damage or tier, always just the number of hits
- Hardwood trees
   - need an axe with “Wood cutting tier 2”
   - right now that’s only the “Rugged Axe”
   - other axes are tier 2 (weapons!) are normally tier 1 in wood cutting!

## Rocks/Boulders
Currently crude stone is not really a resouce in demand. Normally it's just important to know rock mining for removing it.

Removing strone is possible with any mining pickaxe:
- small rocks take 25 hits
- small stone walls take 25 hits
- bigger rocks / boulders take 50 hits
- [TODO: I think there is another bigger category or rocks?]

## Metal mining
Data ref for the whole section: [/data/mining.data.md](/data/mining.data.md)  

Mining is the job category 'harvesting' and also gives xp to the respective skill.

The effective impact of harvesting skill on mining is:
  - It gives you a chance to gain another ore when successfully mining an ore normally
  - You'll always have a min. 5% chance of an additional harvest (harvesting lvl. 1 AND 0)
  - Max. chance will be 30% (at lvl. 10)

Mining works by searching places with ore nodes (tin rock, copper rock, garnite, iron rock) and mining them with a pickaxe. After over earth metal rocks are depleted you can continue at the same spot underground with pits (T3 building).

Mining - unlike most other resources - is not endless. However underground mines (pits) have a much higher amount of ores than over earth mining.

Ore nodes in the map will always be in the same spot and in the same number. You get more ore at spots with more nodes. The number of ore nodes you can mine has the biggest impact on the overall ore yield.

Additional info:
- Testing and modkit inspection did not yet show any impact of productivity buff on mining
- There is no indication of significant differences in yield between player vs NPC overground mining. However: players can hit the rocks much faster with click timing for animation canceling which would give players a potential speed boost for mining. 

### General **over earth** mining (data from modkit):
- You and NPCs can do mining. NPCs can do it either as companions being ordered to 'havest ore' or via a mining building.
- Rock, tin, copper, iron, granite: do not respawn after depleting them over earth!
- Mining gives xp to harvesting:
   - Ore gives 3xp
   - Crude stone gives 1xp
- Mining mechanics:
   - Each over earth node (e.g.: a tin rock) has a fixed amount of 'outputs'.
   - Hitting a node with the correct tier pickaxe removes an output and applies a certain chance to get **an ore** and **crude stone**.
   - Chances and number of outputs vary depending on the ore type.
   - The visual representation of a metal rock has no impact on the number of outputs
   - Once a node lost all outputs it is removed forever from over earth mining



### General **underground** mining (data by testing)
After the over earth metal rocks are gone you can continue mining underground with the T3 building 'Pit'. Place a pit always close to former over earth nodes.

- When placing a pit it shows 'nearby resources'
   - All 'nearby resources' shown before placing the pit define what ores will be mineable in that pit
   - The numbers for specific ores shown in 'nearby resources' tell you how many underground nodes/veins are within reach of the pit.
   - The old over earth nodes seem to define the number and position of the underground nodes (but give different yield underground). 
      - So it's recomended to keep track of the former overground nodes and make sure that they are all within reach of the pit before placing it. 
      - If they don't fit, you can reach the remaining nodes with another pit or by moving the building after the mining capacity depleted at the old spot.
- It is assumed that underground nodes also work with the concept of 'outputs' like over earth nodes
- Underground nodes will be depleted forever. Once 'mining capacity' displayed goes below 1% it will say 'depleted'
- For copper and iron it was shown that underground nodes give about 5 times the yield that over earth nodes have. E.g.: a 4 copper node deposit gives about 240 ores over earth and an additional 1200 ores underground. 4 Iron nodes will give about 6000 iron ore from underground mining.
- Transitively because copper and tin behave the same as iron and garnite do, it's likely that that the 5x times factor for pits counts for tin and garnite as well.

### Copper and Tin nodes
 - 907 outputs
 - 5% chance of stone on hit
 - 6.5% chance for tin/copper ore on hit
 - [calculated per node] 
   - on avg. ~62 ore at harvesting lvl 0 to 1 
   - on avg. ~77 ore at harvesting lvl 10
   - Pits: on avg. ~300 ore at harvesting lvl 0 to 1, [TODO: daily output?]
 - No bonus from higher tier pickaxe
 - Needs tier 1 pickaxe
 - Durability dmg 1 to the pickaxe
 - [TODO: pit mining duration per underground node, but probably the same as for iron]

### Iron and granite nodes
- 3143 outputs
- 10.5% chance of iron
- 3% chance of stone
- [calculated per node] 
   - on avg. ~346 ore at harvesting lvl 0 to 1
   - on avg. ~429 ore at harvesting lvl 10
   - Pits: on avg. ~1577 ore at harvesting lvl 0 to 1, about ~42 ores daily
- needs tier 2 pickaxe
- durability dmg 2 to the pickaxe
- pit mining duration per underground node and fully operated pit: 37.5 days


## Open Questions (TODOs)
I'd say there are still some open points but they don't seem to be too pressing. This information seems to be important only for real crazy min/maxing.
- Get missing numbers for tin/copper daily output from a pit
- Get missing number for expeced duration of a tin/copper underground node in a pit
- Can we see quantitative differences (yield or speed?) between player mining, NPC workers and NPCs in companion mode? [Although: overall yield between players and NPCs was already be shown to be at least in the same range. Tests would likely only be needed to very clearly show that there is no real difference]
- How can total yield and harvesting speed (mainly on NPCs) be influenced, or can they at all? 
