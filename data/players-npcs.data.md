# Player controlled NPCs (Data)

## Test 1
**Intention:**  
Does a perma death refund the NPCs renown?

**Test setup:**  
Repeatedly send 4 injured NPCs to fight enemies. I used the Brigands HQ for their strong fighters. Once perma death occurs check the renown.

**Results:**  
After several attempts one of the 4 actually died. The exact renown for that NPC was 100% returned

## Test 2
**Intention:**  
For how long will NPCs be unconscious (fallen in battle, not available)? And how long are their injuries?

**Test setup:**  
3 naked NPCs with clubs are send against Brigands HQ. Once the first falls the stop watch is started. The others should be falling shortly after. Their time to respawn is not exactly measured but should be just seconds after the first fallen if all fall at a similar moment.

**Results:**  
The 3 NPC fell pretty quickly after each other. The first fallen needed exactly 10 minutes to respawn. The others came back just seconds afterwards. 

**Side observation 1:**
The injuries appeared immediately when the NPCs fell and had a visible timer counting down from 20 minutes. So actually once the NPCs reappear in your camp they have injuries for 10 minutes (real time). The injury timer is helpful to predict when exactly an NPC will respawn if the timer reaches 10 minutes. Also: their bodies disappear in that moment.

**Side observation 2:**
The injury icon shows what effects it has on hovering over it. It shows for all injuries a +30% death chance (meaning perma death), and some other debuffs (crafting, movement speed, etc) depending on the type of injury (head trauma, broken leg, broken rib).

## Test 3
**Intention:**  
There are traits that increase the chance for perma death. Does this affect already the first time an NPC falls (is 'knocked out'), or are even these NPC safe the first time?

**Test setup:**  
Repeatedly kill NPCs having increased death chance (right now neurotics). Make sure that they are not injured before. The trait says 30 to "injury death chance". Make sure to not chose NPCs with a conflicting trait that give less death chance. For also testing the second chance (with injury) get them with their injury after 10 min - make a save - and kill them again. If they die load the save and let them heal the injury. Repeat from there.  
(Used mod for killing Averys Kill-Stuck-Villagers)

**Results:**  
I've found 2 neurotics and let them be killed 10 times without injury and 10 times with injury:

Kill attempt | Deaths without injury | Deaths with injury 
---| --- | ---
1 | 0 | 2
2 | 0 | 2
3 | 0 | 2
4 | 0 | 2
5 | 0 | 2
6 | 0 | 2
7 | 0 | 2
8 | 0 | 2
9 | 0 | 2
10| 0 | 2

**Conclusion:**  
The results are unexpected. It might make sense that neurotics never get perma death the first time but it seems too much that they never survive the second time. If a normal injury gives 30% and the trait increases this by adding 30% we should be expecting about 4 cases of each one surviving. Or due to small sample size there should be at least 1 case.

One explanation for this could be that there is only pseudo probability used and the taken actions did not yet lead to a proper chance re-roll. The test should be repeated with normal NPCs.


**Side observation 1: Injuries**  
This provided the opprtunity to collect injuries:

- All injuries: "Chance to die when knocked out 30%"
---
- Head Trauma: Max health -25%, Crafting speed -15%
- Broken Leg:  Movement speed -20%, Agi -50%
- Broken Arm: Cutting Damage Dealt -50%, Crafting speed -15%, Max health -15%
- Arrow in the Eye: Crafting -15%, Archery -50%
- Flesh Wound: Max health -15%
- Broken Ribs: Stamina regeneration speed -50%, Crafting speed -50%

**Side observation 2:**  
While "knocked out" NPCs can't be given books to read.

## Test 4
**Intention:**  
How is the perma death chance distributed for NPCs without any modifier to their injury death chance?

**Test setup:**  
This time we needed 'normal' NPCs in regard to death chance. That made it easy to find 10 NPCs to test at the same time. We killed them, waited for 10 min till they came back with an injury and immediately saved (because here we only want to test 'injured death') killed them again, and made sure everyone died within the 20 min timer. Reloaded and send killed them again and so on.  
(Used mod for killing Averys Kill-Stuck-Villagers)

**Results:**  
The dying NPCs were different ones each time.

Run | Deaths | Total NPCs
--- | --- | ---
1   | 3 | 10
2   | 3 | 10
3   | 4 | 10

**Conclusion:**  
So this shows that 'injury death normal' NPCs behave as expected. Here we had 30 deaths while injured and got 10 perma deaths. This gives a probability of ~33% which is close enough to the expected 30%.

# Test 5
**Intention:**  
Collect all current traits and their effect

**Test setup:**  
Currently a large settlement with 100+ NPCs is available.

**Results:**  
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
Porter | Bonus inventory rows 2, Movement speed -10%
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

## Test 6
**Intention:**  
How is the perma death chance distributed for NPCs with the "Nomad" trait? Can they perma die at all?

**Test setup:**  
I had 5 nomads available. They were killed immediately each time they woke up. It was checked that they died within their injury time.  
(used mod for killing Averys Kill-Stuck-Villagers)

**Results:**  
The dying NPCs were different ones each time.

Run | Deaths | Total NPCs
--- | --- | ---
1   | 0 | 5
2   | 0 | 5
3   | 0 | 5
4   | 0 | 5
5   | 0 | 5
6   | 0 | 5
7   | 0 | 5
7   | 0 | 5
8   | 0 | 5
9   | 0 | 5
10   | 0 | 5

**Conclusion:**  
It was not possible to kill nomads even with 50 attempts. It makes sense

## Test 7
**Intention:**  
What happens to the contents of an NPCs inventory upon being knocked out? Is there a difference between worker and companions? What happens to the worn gear, ammo and contents in the food bag and eaten food? What is lost if the death is a perma death?

**Test setup:**  
NPC preparation: Use an NPC that is ideally a neurotic or at least can get perma death. Give it armor, a weapon, some quiver with ammo, additional ammo in the backpack and normal inventory. Make sure it has 3 meals and some food in the food bag. Also have food somewhere in the inventory. Additionally add some resource A into the inventory and another into the back pack. Same with books.

1. Have that NPC be knocked out as companion
2. Have that NPC perma die as companion
3. Have that NPC be knocked out as worker
4.  Have that NPC perma die as worker

In case of knock outs: check if inventory and gear is complete after 'wake up'.

In case of knock outs and perma death: check if anything drops on the ground upon death.


**Results:**  
**1. Knocked out as companion:**  
The complete NPC inventory survives

**2. Dying as companion:**  
Everything is gone with the NPC

**3. Knocked out as worker:**  
Everything stays on the NPC

**4. Dying as worker:**  
Everything is gone with the NPC

**Side observation 1**  
This however is different if workers are carrying items for a delivery job. In this case specifically the delivery items only are dropped to the ground. Probably so that potentially valuable items are not locked for the 10 minute knock out time.

**Conclusion:**  
Inventory items stay in most cases with the NPC. In case of a knock out this means the items are 100% kept, which is much better than for the player character that loses everything.

NPCs however seem to have once exception where they drop items upon being killed: When being killed while doing a delivery job.