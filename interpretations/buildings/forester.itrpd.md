# Forester
These interpretations about the forester building are based on the [Forester Building (Data)](../../data/buildings/forester.data.md).

The forester management UI combines controls for **growing saplings** and for **growing trees**. The placement of the forester matters and should be centered in a deforested area. It can only grow exactly the same trees that were already existing before. It can handle two workers at the same time: one for growing saplings in its pots and one worker for planting ready saplings. Testing shows planting happens in a **150 m working radius** around the forester.

For both jobs the farming job priority is important. (Skill requirements?!) But no experience to farming is given, instead planting and growing saplings gives crafting experience.

## Growing saplings from seeds
The 16 pots in the building are like the 25 planting spots in farms but dedicated for growing saplings from tree seeds.

**Growing a sapling:**
1. Have an NPC with farming priority.
2. Add Mud and tree seeds. \[Optional: Also add fertilizer and water, it increases yield\]
3. In the forester management have a top up rule that allows growing of saplings.
4. Have any prio except 'disabled' for sapling growing

The NPC should start taking care of the planting pots and saplings should be growing within minutes. Growth took about 41 hrs in-game (almost 2 days) under the used test conditions.

NOTE: Growth of young saplings stops during winter (like crops on farms).

**Yield per pot:**  
Without any care (no fertilizer, no watering in between) a pot usually yields 1 sapling plus about 0-2 extra tree seeds. 

With fertilizer and regular watering it usually yields 2 saplings plus 0-3 extra seeds (average 2). Farming skill might have an additional effect on yield, but it's unknown.

**Counting across foresters:**  
The "growing" count shown in the top-up UI is a shared pool across all foresters in the settlement, not just the pots of one building. Also this number represents just the pots currently growing saplings. Depending on care the yield might be on average about 2x higher.


## Growing trees from saplings
For it to work it's only important that you have saplings in some storage in your settlement. You could grow them in a different settlement but would still need a forester here for tasking planting of saplings and defining the area where to plant (in a 150 m radius around the forester building). 

Tests did not show that wood cutting buildings could somehow increase the working radius of the forester beyond the 150 m radius.

It is not important to have any lumbermill, lumber jack, logging camp etc. nearby for the forester to work.

**Conditions for a tree to be replanted:**  
1. A tree must have been in that spot before (any sapling will become that tree 1:1 again)
2. The tree must be within that 150 m radius around the forester
3. The tree must be about 10 m away from any building
4. That tree must have been completely harvested: all logs of a tree must have been cut and put into an inventory (of any kind: player, NPC, storage...) once. This can also be identified by the stump of the cut down tree despawning (it happens seconds after all logs are harvested).
5. A worker with farming job priority must be present (just farming is enough) and available (no other higher prio jobs)
6. Within the management UI of the forester give a fitting planting prio for the respective wood type the tree provides. So if the harvested tree was softwood there must be a prio for planting that. If it's set only to hardwood but no hardwood tree were ever there or harvested, nothing will happen.
7. A ready sapling must be in some storage somewhere in the settlement

If buildings were removed to free a spot in regard to 3. ("trees won't be planted near buildings") it might take a night for that removal to take effect. The building must be 100% removed, including all resources and the construction site highlighting.

If all above conditions are met: a worker will immediately (within 5 seconds) be assigned to the forester to plant that tree. Planted saplings grow into trees even during winter. It takes 3-4 in game days for the tree to fully grow.

During the whole growth period saplings stay sapling but with a growth indicator that is visible if you come close. These saplings are different than others in that they can't be used for wood harvesting, or cut down. They once the growth indicator reaches 100% you often have to back a couple of meters away and shortly look away for the tree to be fully grown.

While doing the job the forester NPC needs to be set to a high **farming job prio**, but it gives **crafting experience** to plant the sapling.

## Additional Infos
- Check the underlying data and tests: [Forester Building (Data)](../../data/buildings/forester.data.md)
- NOTE: The forester has a range of 150 m, the logging camp as well, the lumber jack has 200 m and the lumber mill 250 m
- The statistics page shows log icons but the count refers to the number of trees planted
- The "growing" count shows the number of existing saplings plus the currently growing ones. The growing ones are always counted as 1 but normally due to fertilizer, watering etc. you get more than 1 sapling, thus the number of growing can normally be multiplied by factor 1.5 up to 3.
- While planting the message in the NPC details showed either "taking 1 tree sapling from xy storage" or "harvesting". The image in the forester for the working NPC shows "crafting" and the NPC's crafting skill.
