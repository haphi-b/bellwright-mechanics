# Game/Real Time
## General
- A whole day in-game takes 45 min real time (from now real time is implicit and in-game is written)
- So 1 min in-game is 1.875 seconds but this assumes that time is progressing at a constant rate (could be that combat, different parts of the day etc. have a different time progression speed, but right now I did not find any indication of that)  
  
**Examples:**
game time| real time | relevance
---      | ---       | ---
24 hrs   | 45 min    | whole wake day
16 hrs   | 30 min    | summer NPC wake/work time
13 hrs   | 24 min 22.5 sec | winter NPC wake/work time
5 hrs 20 min | 10 min | despawn time of dropped items
1 hr     | 1 min 52.5 sec | useful: 1 hr in-game take almost 2 min
1 min    | 1.875 sec | smalles unit

Data ref: [/data/time.data.md](/data/time.data.md#test-1-Game-time-vs-real-time)


## Despawning of items
Despawning is time based, for that reason you find it here.

- When the player drops items on the ground (there is no difference between a loot bag = different items or an item stack = just 1 item type) it takes exactly 5 hrs and 20 min in-game or 10 min for that drop to despawn. (not yet tested: is it the same when NPCs drop sth.? )
- **NOTE:** When storage is full you sometimes see drop bags in fron of storage. If this happens before NPCs go to bed, the items will probably despawn till next morning [TODO: should check that]
- Only in-game ticks (minutes) are counted for that so once you drop sth. you can calculate the exact in-game it will despawn
- When just inspecting the drop without add/remove the despawn time is not changed
- When adding sth. the timer starts again from zero from the time of adding. This counts for the whole drop/stack. The drop will always despawn completely, never partially. 
- So e.g. if you are mining, have an overflowing inventory (items drop to the ground) and are able to add new items to that drop within 5:20 in-game hrs, the drop survives completely

**Note:**  
A chopped down tree is not yet any form of item bag. You can chop the tree and even cut the logs and they won't despawn.

[TODO: That's currently personal experience. Wished a couple of times that simply chopped trees would disapper but needed to collect logs for it. Better also test this]

## NPC schedules
### Summer and Winter
Data ref: [/data/time.data.md](/data/time.data.md#Test-2-Summer-and-Winter)

- There are two seasons in Bellwright: Summer and Winter

**Winter:**  
- Duration is 2-3 days 
- Can’t harvest anymore: berries, mushrooms, flax, hemp, cotton, garlic, wheat, everything on the farm, mud, peat, moss
- Can still harvest: Reed, stone, sticks
- There is a debuff NPCs and players get (can’t be avoided with clothing/capes)

**Summer:**  
- Duration is 7-8 days 

**Schedules**  
- Schedules for worker are fixed and not configurable
- Workers will only be active during working/awake hours, while companions, guards will always be awake. Caravaneers are technically workers but they will always work caravans only depending on if a caravan should be sent. So if during the night the automatic condition for a deployment is triggered or the player explicitly sends a caravan it’s done instantly also during the night.

### Wake and sleep times
Regarding sleeping times it makes no difference if it is one of your NPC workers or a not-yet-recurited villager NPC: the times are the same.

For quests it's nice to know how much time remains until village quest NPC go sleeping. Its just the same time your NPCs would normally go to sleep. However: Keep in mind that your NPCs often stay a wake much longer due to tasks. There are often tasks NPC rather run to completion instead of going to sleep.

**Sleep Buff**  
When sleeping you get a buff with +10 Stamina and +1 Stamina regen speed. This is not much and normally not worth for getting sleep.  
Your workers don't get this buff or any other for sleeping. Also keeping them awake (e.g. as companions) the whole night till next morning doesn't come with any debuff.

**During summer**  
- **NPCs:**
  - wake up at 6:00
  - go to sleep at: 22:00 (after finishing their current last job. This often takes more than an hour.)

- **player:** 
   - wakes up at 6:05
   - can go to sleep at: 20:00

**During winter**  
- **NPCs:** 
   - wake up at 7:00
   - go to sleep at: 20:00

- **player:**
   - wakes up at 7:05
   - can go to sleep at: 18:00

So during summer you get a theoretical worktime bonus of about 23% (3 hours more work done per day)

## Timed Events and Quests
- Whenever a quest says “come back next day”, or just “wait till…” it normally mean to wait exactly 24 in-game hrs and not strictly the next day
- For raids it’s often not 100% clear: If the raid threshold is reached you get the message a raid will come ‘tomorrow’. But if you get the message at 10pm you actually have the whole next day and the raid will start during the day the day after tomorrow. I guess raids are only at sometime during working hours (bandits respect their working hours)
