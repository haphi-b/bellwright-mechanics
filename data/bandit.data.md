# Bandits (Data)

## Info from "Preview Branch Changelog from Nov. 2024"
*Source:*  
https://steamcommunity.com/app/1812450/discussions/0/4634860720019833781/

A part of the whole post treats the bandit topic:
>...  
>Villages 2.0
>
>After liberation, villages gain a "Prosperity" bar, unlocking a stronger Militia that patrols against bandits and occasionally aids the player. Prosperity grows with village improvements and clearing threats but declines if threats go unchecked.
>
>Each region now has a dynamic threat level influenced by bandit camps, patrols, and the threat in adjacent regions, affecting patrol difficulty and migration
>
>Camps now send migration parties to nearby areas when threat is high enough, forming stronger camps as prosperity rises, while migration frequency decreases as regions become populated with camps
>
>Militia from neutral villages can now be temporarily called to arms, >strengthened and upgraded as prosperity grows and Village improvements are >built, and will start sending patrols when their numbers are large enough.  
>...

**Remark:**  
Seems like the village militia patrolling against bandits doesn't happen anymore or only rarely. Never observed it and when I discovered it on the map as region stat: never got an entry for a patrol.


## Data from using dev cheats
Launching the game with the `-cheats` option and in game using `ShowSubregionAdditionalInfo 1` you are shown additional data to the threat info about regions.

- There is a **max. threat difficulty** ranging from 0 (Hearndean) to 16 (Hollow Creek and Crescent Valley)  
**\[Interpretation:\]**  
This might define what tier bandits specific camps can be. So that in the north you'd see more tier 1 and 2 camps while in the south almost only tier 3 and 4.
- Each region has a current and max. number of **camp points**. For example Hillside had 10/144 when inspecting it while it had a bandit camp.  
**\[Interpretation:\]**  
It seems these camp points are used when bandits create new camps or upgrade existing ones.
- There is a out/in migration between 0 and 1 per region. Brigands HQ has 1/1 so perhaps this makes it impossible for camps to spawn there. When all camps are destroyed each region normally seems to get 0/1. So no out migration and full in migration. In regions where a camp exists out migration was seen to range from 0 to almost 1 but never 1.  
**\[Interpretation:\]**  
Referencing the official explanation *"migration frequency decreases as regions become populated with camps"* I'd assume in migration lowering OR out and in migration going to 1/1. This should be testable.  
Still it is somewhat stays unclear what 'migration' actually is? Is that the increase in threat level in this region (in migration) and the increase in threat level to neighboring regions from this region (out migration) at the cost of threat level in this region?

## Test 1
**Intention:**  
Unterstand bandit camps and what can be done with them.
- How do they 'spread' (aka migrate)
- How does a regions threat level rise?
- How do bandits spawn
- How do new patrols come to life?
- Do patrols of brigands and bandits fight?
- How do worker and caravans interact with any hostile patrol?

**Test setup:**  
Launch the game with the `-cheats` option. Use `ShowSubregionAdditionalInfo 1` to understand as much as possible while its happening. Go to a bandit camp and use `SetPlayerInvisible 1`. Wait there with the help of `Speed up and Slow Motion by Misper` mod in 10x speed until you find a bandit patrol. Follow them and observe what they do.

Stick to a camp for longer to see how they respawn.

**Results:**  
I followed 5 bandit patrols over some time. Horndean was at prosperity 5 and their caravans destroyed three of the bandit patrols.

The first patrol was relatively small 2x archers and 1x 2H melee. That was at about threat level 10%.  
That first patrol went as all others for a round trip starting at the bandit camp, reaching about 2 target points and then turning back to the main camp to repeat the process. 

At some point when threat level reached 20% a second and larger patrol also met at the camp. Later caravans from Horndean were defeating the patrols and one time even the camp. But it did not show up as defeated patrols/camps. Threat level didn't go down or just 1% if at all (but that could have be normal variation). I would have guessed if a player defeated the same patrols and camps: a stronger decline in threat level would occur.

After the camp respawned (it seemed to spwan 1 new bandit every 2 in game hours up to the camps 6 bandits) I followed a newer larger bandit patrol. After about 100-200 m in front of one bandit suddenly a camp appeared out of thin air. The patrol did not inhabit the camp but continued to patrol. This must have been a 'migration party' as described in the changelog from 2024. Out/In migration didn't show anything that made sense for me just the usual ~0.6/1 I had these values a couple of times already.

Checked how fast they respawn (all times as in-game): Killed all except one. Waited. Nothing happened after multiple hours and even a day.
Repeated but this time went so far away I barely could see the last one on the 'radar'. After about 1 hr new bandits spawned. The distance seemed to be pretty exactly 1 hr for all 5 of them. I killed them all within 10 minutes so the respawn seems to be queued, with a 1 hour timer.

**Side observation 1:**  
threat level actually did not go down much. This came as a surprise, but not taking the flag seemed to be the cause. Each bandit just gave about 80 renown (all together 6 of them). The flag gave 1240 and eliminated the threat from 20.2% to 0.2%.  

Seeing village caravans often clearing camps it might be that this is to preserve threat progression.

**Side observation 2:**  
Number of bandit patrols seemed to be correlated with the regions "+Bandit patrol activity". A camp seemed to have 1 patrol at 1%, two at about 2%. At 3.5% I could identify 4 different patrols according to their weapons. Identification of patrols belonging to the camp was made by checking that the patrol came into touch distance of the camps fence. I waited for 3 days to check if more different patrols showed up.

**Side observation 3:**  
Took an image of the cleared map of the initial game start and checked all bandit camps. Checked my current map and the location of spawned bandit camps (all original ones were gone/claimed). The spawned ones were actually in different locations. So either there are more predefined spawn locations or they can spawn at random places. OR it depends on some fixed possible bandit patrol waypoints.

**Side observation 4:**  
For some reason the threat development of my preferred observed camp (but also neighboring camps) did not continue development after reaching a threat level of 20%. I'd exclude killing the bandits as cause as the development of the neighboring camp that was not touched was the same.

**Side observation 5:**  
Bandit patrols returned to camp within 1 day and a half (at max). But that could have been specific to the location.

**Side observation 6:**  
Killed bandits except for 1 and let them respawn: min. distance from center of the camp for them to respawn 50 m!
- There will always be the same number of bandits 
- also the same renown/equiment tier
- additionally: archer and crossbow man will always cam back as such
- 2H came back as 2H but could switch to other weapons (mostly blunt or spear)
- 1H came back as 1H again but switched between axe and sword.

patrols without camp

is "militia patrol activity still used?"

**Conclusion:**  
Catching the event of a bandit migration must have been rare. One could try to recreate this by waiting a region with 1 camp to reach threat level 20% (make sure no other migration occurred already) and wait for a patrol that is not coming to the camp but spwans directly from the camp.

Considering the spawning of individual bandits needing you about 70 m (perhaps just 50?) away I wait at a distance.

- Every bandit patrol could be a 'migration party'
- Bandit patrols always do round trips. If one wants to catch just patrols waiting in the proximity of camps is a good idea.
- Killing a complete camp without taking the flag keeps threat level and possibly threat progression up while also gaining some renown (here the deal was 480 vs 1720, so 1/3 of the complete renown).
- 