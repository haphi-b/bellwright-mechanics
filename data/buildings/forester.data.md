# Forester Building (Data)

## Test 1
**Intention**  
The hypothesis is: The forester is like a farm with 16 spots but to grow saplings (only). If you define a top up you get the usual info you have at farms: <count current> + <count growing>. The "count growing" is supposed to be a shared count over all foresters (like with farms).

**Test:**  
Have 12 saplings. Have 2 foresters, one with 16 another with 15 growing (so sum should be 31).

**Result:**  
Each forester shows 12 existing + 31 growing.

**Interpretation:**  
Hypothesis is proven to be right.

## Test 2
**Intention**  
The hypothesis is: No planting will be done if you use disabled prio for softwood and hardwood. Still saplings will be produced if prio for tree saplings is not 0 (disabled).

**Test:**  
Have all foresters planting (soft/hardwood) prio disabled but have saplings available (growing shows existing saplings).

**Results:**  
Saplings are produced, new trees were not planted.

**Side Observation:**  
Forester shows existing saplings + growing. The "growing" assumes 1 sapling per pot but depending on care (watering) and fertilizer (and probably farming skill?) a growing often yields more than 1 sapling. I've encountered 1-3 saplings and sometimes even new tree seeds. So 12 + 28 growing with a top up till 40 almost guarantees more than 40.

**Interpretation:**  
Hypothesis is proven to be right.

## Test 3
**Intention**  
The hypothesis is: Trees are not re-planted unless all their logs are harvested (indicated by despawning of the tree stump).

**Test:**  
Saplings in the barn. A forester building without any sapling growing. 1 NPC worker with prio for framing and nothing else. Trees manually cut but logs are not cut and harvested (so the trees still lay on the ground). Later trees are completely removed to check if that triggers a different behavior.

**Results:**  
Trees were not planted by the NPC as long as logs and the stump still existed. Waited for 20 real time minutes.

Trees were planted immediately after removing all logs so that the chopping stump despawned (happens seconds after the last log is picked up). The NPC would continue planting trees until saplings run out or all places were filled.

**Side observation 1:**  
No wood cutter / woodsman station was required. It's sufficient if just the player cuts them down.

**Side observation 2:**  
It took about 4 days for the trees to be fully grown.

**Side observation 3:**  
Strangely not all spots got saplings: spots closer to the settlement area were not re-planted. Just putting down a fence was enough to increase the area where planting did not take place. So the AI seems to not plant where you have buildings or your settlement is. Removing the fence, planting took place.

## Test 4
**Intention**  
How far would the forester go? And is that distance related to the position of the forester? Is the area expanded if there is a wood cutter?

**Test + Result:**  
Went about 200 m away from the small camp (had a marker where barn + forester + house all were within about 10 m, yet unclear what governs it) started cutting down trees from 200 m and came closer in 10 m steps. At about 150 m he started planting.

Moved the forester building about 100 m into the opposite direction away from the camp center. Chopped at same distance again and then closer: didn't work at the original distance anymore (150 m) but at about 50 m from camp (which was 150 m from the forester).

Went to the new position of the forester (100 m away from the settlement) and went about 145 m into the opposite direction away from the settlement (so the distance from settlement was about 245 m). Cut a tree down: the farmer planted there.

**Interpretation:**  
So it seems planting is done within a 150 m radius around the forester.

## Test 5
**Intention**  
Can wood cutting sites increase the planting radius/area. Like having the 150 m around the forester and additionally all areas around wood cutter stations? This is relevant as normally wood cutting buildings have far larger areas than 150 m.

**Test:**  
Keep setup of Test 4 but add 100 m from the barn/camp and 250 m away from the forester a logging camp. Cut down a tree in a chopping radius around the logging camp but further away from the camp site.

**Results:**  
After chopping and harvesting some trees, nothing is planted in the chopping area of the logging camp.

**Interpretation:**  
It seems the chopping radius is not added to the 150 m radius of the forester.

## Test 6
**Intention**  
What is needed to grow saplings?

**Test:**  
The growth process does not start without mud and tree seeds. So these have to be provided. What impact do fertilizer and watering have?
So one row is without fertilizer and without watering in between: just mud and tree seeds. The other was with fertilizer and watering.

**Results:**  
Player farming 5  
Started at 21:00 with rain (auto watering initially) but no growth activity showed until the next day at 6:00 or 7:00. After the morning start it took them 1 day and 7-8 hrs, (or when counting from 21:00 it would be 41 hrs) to mature. All at once. With the extra care one could yield always 2 saplings and 0-3 seeds with an average at 2. Without care it was only 1 sapling and still about 1-2 seeds. But the bad care batch was ruined a bit by a farmer watering some of them (although farming was disabled for him).

Farmer with farming 7  
Start at 18:00. Farmer gets 0 farming xp. The farmer automatically uses fertilizer and waters them initially. After about half the time the farmer waters them again. The trees didn't need any more watering and were grown after 41 hrs, so the run with the player probably did start at 21:00 already but simply didn't show that. The yield was the same as with the player.

## Test 7
**Intention**  
Buildings have a small area around them so that trees aren't planted again next to them.

**Test:**  
Add a building (camp chests) and chop a tree nearby. Check if it is replanted. If not, increase distance around the chest.

**Results:**  
The furthest tree that was not replanted was about 7-8 m away from the chest, whereas the nearest tree that was replanted was about 8-9 m away. So that gives an idea of the area around buildings. But it's unclear if larger buildings have a zone around them or simply a radius around a center and if these distances are much larger than for a chest.

## Test 8
**Intention**  
How do the statistics work? Do they show logs or trees?

**Test:**  
Get current total statistic. Note the count. Cut down a 2 log tree. Let it be replanted and check the statistic afterwards.

**Result:**  
It showed 1 more - tree - it seems. But it's saying that already, just the icon made me question it.
