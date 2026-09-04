# Bandits
The backing tests and data for the following interpretations can be found in [Bandits (Data)](../data/bandit.data.md).

Generally after many days of testing, there are still several questions open regarding bandits. Here are some first findings.

Though the stat of a regions `threat` is still badly understood, it seems like it's the bandits equivalent to prosperity. More threat might enable them to spawn patrols faster and get better gear. Additionally camps are supposed to upgrade which might also be an effect of higher threat but these things could not yet be tested and observed properly.

The main driver of threat are bandit camps. They provide a `threat from encampments` that over time will increase the regions threat to that percentage. Multiple camps in a region add their threat contribution.

Camp Tier | Camp Threat | Max. No. Patrols
---       | ---         | ---
1         | 10%         | 2 
2         | 20%         | 2 
3         | 20%         | 2 
4         | 30%         | 4 

Each camp normally spawns 2 bandit patrols (only tier 4 camps have 4 patrols). Additionally bandit migration parties can spawn depending on the number of camps and the migration frequency. These are bandit patrols that create a new bandit camp.

## Camps
**Creation and Migration:**  
- They are created with bandit migration parties: a patrol with a destination where they create a camp and immediately disband. (More details about this process in the data)
- Migrations originate from a camp and go to a place in the same or a neighboring region.
- If all bandit camps in Karvenia are cleared and migration is enabled, two initial migration parties will be randomly spawned. The first in about 4 hrs and the second party in 8 hrs. These parties could by chance attack villages, outposts or the main settlement, as they are no longer bound by the neighboring radius of any camp. They do spawn almost everywhere. 
- If migrations are disabled while a migration party is marching, that party vanishes immediately.
- Migrations happen in certain time intervals per camp (time given as in-game):
   Migration Frequency Setting | Avg. Time needed (hrs) | Avg. Time needed (days + hrs) | Speedup 
   --- | --- | --- | ---
   low    | 232:08 | 9d 17h | 1.00x
   medium | 136:45 | 5d 17h | 1.70x
   high   | 87:00  | 3d 15h | 2.67x

   The frequency might decrease when the regions are full with camps. It could be possible that the frequencies might be higher at higher threat (this could not yet be tested).

- The game devs said that at higher prosperity higher tier bandit camps spawn. It seems to fit the observation that only tier 3 or 4 camps spawned when all villages were above prosperity 4.
- Bandit camps do not spawn 1:1 in the same position camps were before. Still there seem to be preferred spots.
- Blocking of camps with buildings was not yet tested, but has been reported by players from discord.

General Infos:
- Threat does not decrease when caravans kill camps or patrols.
- If a camp is cleared by taking the flag it immediately removes all threat from that camp.
- Bandit camps start off empty and spawn a new bandit every 1 hr if the player is at least 50 m away from the camp
- Bandit gear sets seem to be persistent for every camp. They fix the:
  - Number of archers
  - Number of crossbowmen
  - Number of 2H infantry
  - Number of 1h infantry

## Patrols
- Spawn at camps as long as the player is over 150 m away from them.
- Belong to their spawning camp and will do roundtrip routes starting from the camp out to the outer borders of their neighboring regions. They will only go further than a neighboring region if they are aggroed (animals, caravans, villagers or player faction). This happen but it is very rare.
- If a camp is on one side of a river but a neighboring region is on the other side (esp. players outpost or settlement) patrols will still regularly visit in spite of a seemingly natural border (as long as there is any way/bridge via neighboring regions). So if a player wants to be free of patrols, they must eliminate all camps at least so far that their settlements region is surrounded only by bandit free regions. Still bandit patrols will walk up to the borders of these and thus could still attack a player settlement that is close to it.
- If their camp is defeated the patrols will be abandoned. (so for max renown you should first get all patrols)
- Spawn times for patrols were observed between under 1 hr up to 12 hrs.
- Defeating a patrol lowers threat only in the region where it happened (renown farming: better lure patrols away from high threat regions)

## Renown Farming with Bandits
This just theory crafting here and not tested as I'm not personally interested too much in this (the normal means of getting renown are normally enough). But it is still interesting to think about farming. Also I will publish everything possible and not just what I think is best for the gamer. But I'd say it's best for a game not to farm as described below as your longtime fun will suffer if your play style keeps relying on grindy farming methods.

Still generally the following points are interesting and good to know.

- Higher threat should give better bandits and thus more renown. So for renown farming purposes it would be advised to increase threat in a specific harmless region. Harmless means: They won't be removing village caravans or attack village NPCs.
- To increase threat within a region, patrols should never be killed by the player there. However they can be killed in regions that are low threat anyways: It will only lower threat in that region and the patrol should be respawned after half a day or earlier.
- If camps are not claimed by the player, the threat stays even if all bandits are killed. To not auto claim a camp it's important to kill the last bandit at least 20 m away from the camp. Also be cautious as killing any other bandit (e.g.: a patrol) within proximity of the camp claims and removes it.
- After an unclaimed camp was 'emptied' the bandits respawn by 1 bandit every in-game hour.
- Not claiming a camp only grants about 1/3 of the complete renown. But considering the camp migration rates of best 3 days and 15 hrs and bandit respawn rates at the camp of about 5-12 hrs in total one could get more renown in that time by effort instead of waiting for new camps that are completely farmed.
- If a player wants to claim a camp and also farm renown, it is recommended to first get the two connected patrols by waiting at the camp. If threat is high it might be worth respawning a couple of quickly spawning patrols first.
- So the best strat might be: have a(some) high threat spawning region(s) that are regularly farmed without killing patrols in that region. Farm patrols regularly in the low threat neighbor regions. Let new camps be created in the neighbor regions and farm these completely but make sure to first get their patrols

Problems:  
Right now patrols can't be seen on the map and it's unclear to which camp a patrol belongs.

## Additional Infos
- Check the underlying data and tests: [Bandits (Data)](../data/bandit.data.md)
- [Video of a bandit migration spawning a camp](../resources/bandit-migration_low-quality.mp4)