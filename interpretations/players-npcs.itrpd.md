# Controllable NPCs
**Hiring:**  
- Hiring NPCs will always require an increasing amount of renown.
- Hiring increases the renown cost for the next hire.
- Having hired many villagers from the same village additionally increases the renown cost for further hires from that town, but the effect is relatively small (observed in a usual playthrough about +10-20%).
- Once an NPC is hired, their village will get a new villager with the same star rating and profession within 10 minutes. If multiple villagers were hired at once the refills will come in a queue one every 10 minutes.
- Expelling an NPC also returns all renown to you.

**Traits:**  
Villagers can have multiple traits that provide specific permanent buffs or debuffs. So far I've found NPCs with 1 up to 4 traits.

Trait | Effects
--- | ---
Neurotic | Productivity +50%, Hunger Speed +25%, Injury Death Chance +30
Fierce   | Attack Speed +20%, Damage Dealt +50% for cutting, again cutting (probably a bug), blunt, melee piercing, spear piercing and arrow piercing
Prodigy | Skill Exp Gain +30%
Scholar | Researching +3, Strength -1, Agility -1
Defender | Attack Speed +20%, Arrow Piercing Damage Dealt -20%, One Handed +2, Shields +2, Archery -2, Polearms +2, 
Marksman | Arrow Piercing Damage Dealt +20%, Cutting Damage Dealt -20%, Blunt Damage Dealt -20%, Archery +3, Agility +3, Two Handed -3, Shields -3, Polearms -3
Gourmand | Cooking +2, Hunger Speed -30%
Stalwart | Combat Attributes +50%
Swordsman | Cutting Damage Dealt +50%, Attack Speed +20%, Arrow Piercing Damage Received +50%, One Handed +3
Resilient | Damage Received -10% for Blunt, Melee Piercing, Cutting and Spear Piercing, Strength +4, Agility -3, Two Handed +2, Healing +0 (what ever that is?)
Porter | Bonus inventory rows 2 (means 6 more slots), Movement speed -10%
Glutton | Hunger Speed +50%
Coward | Attack Speed -20%, Arrow Piercing Damage Received +20%, Hunger Speed +25%, Damage Dealt -20% for Arrow Piercing, Cutting (twice bug?), Blunt, Melee Piercing, Spear Piercing (twice bug?) 
Nearsighted | Arrow Piercing Damage Received -20%, Agility -3, Archery -2, 
Nomad | Combat Attributes +30%, Injury Death Chance -30
Optimist | Morale +20
Tireless | Movement speed + 10%, Hunger Speed -10
Weakling | Max health -25
Dullard | Skill Exp Gain -30%
Slacker | Productivity -50%
Pessimist | Morale -20

**"Death" of your NPCs**  
- Workers, guards and companions can be killed. However: the first time this happens it just counts just as being **'knocked out'** and immediately gain an **'injury'** for 20 minutes.
- NPCs do respawn after exactly 10 minutes in their settlement (where their house/sleeping place is). One can simply check the injury time in the NPCs attributes: if it's down to 10 minutes the NPC 'wakes up' again.
- While 'knocked out' NPCs can't be managed anymore. Books can't be started but already started books continue in this time.
- Injuries give a debuff to speed, damage, yield, productivity etc.
- While NPCs are injured they have a 30% chance of permanent death if they die again.
- NPCs with the **'Nomad' trait** can't be permanently killed. But they do get injured when knocked out.
- NPCs with the **'Neurotic' trait** will always survive their first 'knock out' just as every other NPC but have a 100% perma death chance if killed while injured (Though the trait only say +30% (so 60% with the injury), tests show the chance is actually 100%).
- Renown is returned to the player upon the permanent death of an NPC.
- Item are always kept on the NPC. Meaning when knocked out they keep everything, but the same goes for perma death: they take all their gear to heavens.
- The only time items are dropped upon NPC death, are delivery items while a worker is on a delivery job. Still the gear is kept.

**Possible Injuries:**  
Injuries seem to be given randomly.

**All injuries: "Chance to die when knocked out 30%"**

Injury | Debuff Effect
--- | ---
Arrow in the Eye| Crafting -15%, Archery -50%
Broken Arm| Cutting Damage Dealt -50%, Crafting speed -15%, Max health -15%
Broken Leg |  Movement speed -20%, Agi -50%
Broken Ribs| Stamina regeneration speed -50%, Crafting speed -50%
Flesh Wound| Max health -15%
Head Trauma | Max health -25%, Crafting speed -15%



## Worker
- Only pick 1 food while being a worker [TODO:**this claim seems to be wrong. Testing regarding amount of food is planned**]
- Workers only need a sleeping place and food to be ‘happy’ aka: have a good morale. Actual sleep is not required, so it’s okay to have them as companions during the night.
- The sleeping place needs to be of the right tier otherwise they get a debuff. [Need to test: This seems to only affect the main settlement or where a village or town hall is created. In these cases houses would need to be of the tier of that building]
- According to the in-game codex high morale helps to increase "productivity" which is a buff. [TODO: but to what extent? The game does not tell. Morale 50 gives what productivity?]
- Productivity increases the speed of everything that has a process bar [TODO 1: found that about productivity online, reddit, must be verified! but would fit description in-game]
- [TODO 2: why is productivity often different for each work attribute if you hover over them? Prod-Food seems to give a base buff but each attribute seems to have a bigger increase. Perhaps due to the resp. skill lvl?]
- Workers that have "hold ground" enabled will engage in combat and alarm others. **NOTE:** They engage in combat but still normally just take 1 food instead of guards who take 3 foods like companions. [TODO: should these others be reservists or also hold ground? How far away may others be to be recruited? I believe pretty far]
- If a weapon is missing and villagers are attacked: they will run away. That’s terrible when escorting a new recruit home: animals always attack NPCs in your party before you. The recruit will run endlessly in the wrong direction and you after both of them.
- Idle workers will walk alone very far out of your settlement. Basically: If there is any bandit camp nearby (in that county) they are very likely to be attacked
- Workers will automatically pick up dropped loot bags. (if there are close to the settlement, unclear: does the worker simply have to be near or does the loot bag need to be within the settlement area?)


## Guards
- They always try to maintain 3 food
- Guards don’t work and walk around your camp at all times (they don't sleep). They the companion gear preset (needs verification that it is companion preset).
- Once a guard encounters any enemy they automatically call every other guard to assist them no matter how far the others are away (like attacking a single bandit of a bandit camp)
- Need to check: how do guards interact with hold-ground workers?
- Guards wander off like idle villagers
- The wandering of guards is stopped once a wall is built. From then on they mostly walk close to the wall but all guards distribute themselves evenly across the wall.
- From experience: If there are bandit camps close by guards are normally very likely to die bc others come to assist pretty late (does not matter if with or without a wall). Exceptions are if the bandits are super weak compared to the guards or similar things. 
- Guards won’t pick up loot bags of fallen enemies

## Companions
- They always try to maintain 3 food
- Can be ordered to follow you, move to positions, hold ground, charge, or harvest a resource
### Harvesting with companions
- They can’t be used to harvest/ destroy a specific resource. Just try to harvest everything in an area.
- If you want to use companions for harvesting ‘on command’ it’s a good idea to use them during the night. Crafting and researching can only be done by workers during the day but workers will auto sleep during the night. So raising them at night doesn’t cost you production time
