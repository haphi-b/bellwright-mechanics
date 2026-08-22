Current BW Version: 2026-06-09

# Storage
- what has higher prio: starred items or min/max rules?
- can you set a order of how storages are filled via building prio? can that be used instead of starring? is this an additional layer semantically orthogonal to starring and min/max rules?
- how does npc behavior change if storage prio is super high (higher than job prios?) or super low?

# Settlement/building/production
- what job priority is important for which building? Butchery being governed by crafting (!). Does this also depend on the respective job or item to be crafted?
- best way of building river docks or anything, that doesn't have workers in the target settlement/location? Test: build a dock with 0 prio/disabled: resources should be gathered but the thing not built. once resources are there: Disassemble and transport everything with companions?
- is fishing animal handling?
- filling up food for animals: it was done by an npc with AH only prio, but is it also done by delivery ppl? is every job related to livestock building simply AH?
- what jobs are actually 'wood cutting'? only getting log or also wood? for wood: good harvesters are useful? What is the job prio for getting wood from logs?
- how to increase efficiency of smelting?
- how does farm growth work? what effect does fertilizer, weeding, watering, and NPC skill have. Also productivity might play a role. Who picks crops from the farm? Delivery or farmer?
- what job is drying rack?
- how do building prios work against job prios? what is the more important one?
- Prios of orders in a crafting station: orders (top up or one time) in a crafting station seem to be prioritized from top to bottom?


# Workers
- do you actually lose the villagers renown on a perma death?
- where is the harvesting skill actually important? only foraging? farming perhaps, or butchering/skinning as well?
- what prios will worker choose if no job prio is given? Will they consider current and/or max. attributes?
- does it make a difference if job a and b are set to a=1 and b=9, or a=8 and b=9 or a=1 b=2. So any additional info besides say a is more important than b?
- how do worker prios interact with building prios? Supposedly building prios are more important than job prios. Idea: Building prios just say which jobs exist in what priority. Job prio simply says for all the jobs with highest prio right now: pick that one you have highest job prio for. But if you are prio 1 crafting but all crafting buildings are prio 2. currently no one handles the wood cutting order of prio 1, so you go wood cutting. But if there is so with wood cutting prio1: that person goes.
- how do they handle food? Do they always try to have 3 foods even as worker, or do they switch to only 1 food if there's not much available?
- what is more efficient: a mining outpost or have a remote mine camp connected to main base? How do deliveries work and how should one optimize them with (local) storage? What if a harvester does not do delivery?
- is delivery actually better than cart? (NPCs can have up to 39 slots vs 50 in a caravan, can the delivery job be used instead of a caravan and wouldn't that be faster?)
- would 2 settlements in one work and exchange via caravans? or should you use complex storage rules?
- what is more efficient regarding caravaneers: having one route like a bus, or individual push?
- "they need to also have crafting and delivery priority for cooking"...how true is that? cooking: does it need delivery? what jobs actually need an aditional prio?
- how are watering pot and seed pouch used? will farmers automatically switch to these? (only interesting as long you only have bags)
- how useful are storage filters? example: input and output storages? Starred storage and limits vs market. Do player caravans distribute items like the market?
- how good is the player sleep bonus? is it relevant? how strong?
- how does player char and NPCs differ in their stats effects?
- what is the advantage of NPCs for construction? can productivity help construction? Quantizise
- What makes a good hunter? Can one 100% avoid hunter death?
- how do NPCs fish and hunt? how long do they follow a task (generally)?
- can smelting speed actually be influenced?


# Villages / Prosperity
- villager hiring: can the number of apprentices be increased? how do prosperity lvls change the composition? -> I just got more 3 Stars compared to unliberated villages.
- prosperity: how do villages do auto-invest?
- caravans: prove that (if) more caravans exist and check their routes. How do caravan guards gear up, and can they sustain t3/t4 bandits at some point?
- how does militia improve? more buildings = more militia or better ones, or both? Or does prosperity affect their gear? initially it looks mid-tier.
- trade: how are villages handling trade? What do they buy? Maintainance first? Gear? Clothing
- How are facilities constructed?
- how long betwenn reclamation parties?
- how do productions work? They seem to only start if there is another village (! not the player) requesting an item
- can you attack NPC caravans to get loot? What are the negative consequences? Trust/Prosperity? Are they building new caravans?
- what acutally happens when brigands sack a village? The prosperity state? Facilities? Perhaps trade and caravans?


# Caravans/market (of player)
- How are carts lost? What happens to the items? How can you bring carts back?
- How does caravan safety work? Statistical thread reduction vs physical existing enemies (animals, bandits, brigands)
- what equipment + food do caravan carriers use?
- are the markets sell/buy prices min/max prices?

# Bandits/Brigands
- how does bandit migration work? how will new camps be spawned? do they only spawn close to each other?
- what exactly is bandit migration?
- why do bandit patrols walk directly to my main settlement when all camps are destroyed/claimed?
- how real are bandit patrols? looking at the map they seem to be spawned out of thin air on a statistical base (like random mob spawning), or are they persistent?
- what is the normal time between reclamations? aka: is there a way to predict when a reclamation will occur?
- how does the strength of raids/reclamations increase with the raid number?

# Animals
- how do new animals spawn? is it somewhat similar to bandits?
- how to hit wolves and boar with sword thrust? seems impossible


# Combat, guards, companions and walls/defences
- cleanly identigy all behavior patterns for: guard, hold ground and reservists. how can workers be recruited to join the fight. how far is that range. how far can guards be away to support each other?
- what can be done? Perhaps write an entry about staging ground: that it's possible to stock up remotely, that before staging ground NPCs will automatically use the "Footman" default preset (or are they?) and that storages can be used instead of a staging ground. That stocking up is a state that can continue indefinitely even when auto combatting bandits inbetween.: The issues of off-screen combats.
- how do combat buffs stack? are they additive percentages? so for the example of 30% + 40% + 50% is it like: attribute * (1 + 0.3 + 0.4 + 0.5) or: attribute * (1.3 * 1.4 * 1.5). Is there a limit to buffs? (check stalwart + nomad + 3 max combat foods)
- Does strenght affect bow damage?
- how do villager chose food? verify that berry harvesters should not be raised. Perhaps report a bug about farmers with water when being raised.
- how problematic is the map/realworld difference when commanding NPCs to go somewhere?
