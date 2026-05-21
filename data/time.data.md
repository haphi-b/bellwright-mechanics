# Data regarding game time

## Test 1 - Game time vs real time
- Measured a whole day (not sure if summer or winter) with a normal stop watch. Starting at 0:00 to 23:59. Measured pretty exacly 45 min with about 1 sec delay. I'd attribute that to not hitting start/stop 100% accurately. Also: assumung 1.875 sec for 1 in-game minute give flat numbers for 24 hrs in-game and a flat 10 min despawn time. So I assume it's the correct factor.

## Test 2 - Summer and Winter
**Intention**  
How log in number of days is the summer and winter period?

**Setup**
- Use 'AdvanceTime' cheat to advance the time until you can sleep
- Then sleep so you get the messages about winter 
- Immediately after waking up make sure it's summer/winter by checking if flax, mushrooms or berries can or can't be harvested

**Results**
Day | Message for this day   | is summer?
--- | ---                    | ---
1   | "One day until winter" | yes
2   | none                   | yes
3   | none                   | no
4   | none                   | no
5   | none                   | yes
6   | none                   | yes
7   | "5 days till winter    | yes
8   | "4 days till winter    | yes
9   | "3 days till winter    | yes
10  | "2 days till winter    | yes


**Evaluation**  
- 8 days of summer
- 2 days of winter
- The day after the day with the message "One day until winter" starts off as a summer day but changes in the night. So to be super precise one could also say it's somehow 7.5 days summer and 2.5 days winter. But during this test it was more like the changes happend, during the night when workers weren't active anyways, so that 8 summer days and 2 winter days fits actually better.
- However: From experience/gaming I remember times when the switch occured mid day so it seems to be somewhat like 7-8 summer days and 2-3 winter days.

## Test 3 - Despawning
**Intention**  
When do dropped items despawn? What actions keep items from despawning or reset the timer

**Setup**
1) Drop items on the ground and stop time until they disappear. Get the normal despawn time.
2) Drop items on the ground and **inspect them** after about 80% of the despawn time. Check if the action delayed despawning (180% despawn time now?) or if despawning happens after another 20% of the time.
3) Like 2. but instead of inspecting: Add another item.
4) Check if there is a difference when creating a loot bag (multiple items of different type) or a stack (just one item type dropped)
5) Try if only real time is relevant by halting the game via ESC for the despawn time and check if items immediately despawn.

**Results**
1) Despawning was observed after **5 in game hours and 20 minutes**. This was exactly 10 minutes in real time.
2) Insepcting did not change despawn time.
3) Adding an item to the ground resets the timer. When despawning the whole thing despawns. It's not that after 10 minutes the items individually despawned and just the newly added item despawned after the resetted time.
4) No difference could be found between loot bags and stacks: both droppings were gone after 10 min
5) Items only despawn after the 5:20 in game time. Pausing via ESC also pauses the despawn timer.

## Test 4 - Sleeping Times
Not super exiting to put it here but basically during summer and winter I checked at which times villages and NPC went to sleep. Also at what times the player can go to sleep.

**Results**
- Villager / NPCs go to sleep at the same time
- The player wakes up at 5 minutes after the NPCs woke up
- There is a difference during winter and summer.
   - Summer sleeping time: 22:00, player can sleep at 20:00
   - Summer wakeup time: 6:00
   - Winter sleeping time: 20:00, player can sleep at 18:00
   - Winter wakeup time: 7:00
