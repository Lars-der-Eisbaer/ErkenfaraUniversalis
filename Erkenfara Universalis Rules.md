# Erkenfara Univeralis
## Basic Rules

### Abstract
Erkenfara Univeralis is an eternal strategic board game for any number of competing empires.
These rules are kept simple on purpose to ensure maximal flexibility and easy bookkeeping.
Usually there is a simple basic rule which then is modified by status effects of participating parties.
For Example: An army might be exhausted and therefore have lower chances in battle.
This game has no inherent victory or loss condition and can only function
if all engaged parties and empires have an internal goal in mind while remaining open to the political aspects of the game.
These rules define how economics and military mechanics function.
They doesn't strive to simulate how an empire's internal affairs function or how empires engaged in diplomacy with each other.

### Design principles
To guide in the interpretation of the rules, the design principles are defined here:
1. It is supposed to be an eternal game.
	- No snowball (rich get richer) mechanics.
	- Create mechanics that slow winning parties down.
2. It is supposed to be a conflict simulation / strategy game.
3. It is supposed to work with any kind of map.
4. It is supposed to be easily modified to allow the integration of other games (parallel role playing game / trading card game).
5. Keep it as simple as possible.


### Table of Contents
1. Order of Play
	1. Structure of a Round
	1. Tools of Play
2. The Economy Round
	1. Generate Income
	1. Pay Upkeep
	1. Build new Troops
	1. Update Region status
3. The Military Rounds
	1. Update Status
	1. Movement of Armies
	1. Resolve Conflict or take action
	1. Recovery of Moral
4. Resolving Conflict

### 1. Order of Play
A round in Erkenfara Univeralis (short EU) consists of 1 economy round followed by and 3 consecutive military rounds.
This round structure represents the four seasons starting with the economy round in winter.
While the military rounds occur in a fixed order one empire taking its turn after another, the economy round can be performed simultaneously.

Each Empire in EU is represented by 3 factors:
1. The treasury
2. The regions owned by the empire
3. The armies executing the will of the empire

Each region and army can be influenced by one or more status effects.

Each region can contains up to one land army and up to one sea army.
In addition to that, each region is one of the following 3 types.
Sea region, land region, or fortification.
Sea regions can be traversed by any army, land or sea. They have no production value and can't be owned by any empire.
Land regions can't be traversed by sea armies. They have a production value and can be owned by an empire.
Fortifications are a special kind of land regions. They only are adjacent to a single land region and have 1-4 levels of fortification.

Each army has a current and maximal value and a location.
The location is the current region the army resides in.
The value of an army is both its production cost and its measure of strength.
If for any reason and at any time the current value of an army drops below 1000, the army is scattered and removed from the game.
Armies differentiate real and moral damage. Once real damage is sustained, there is no possibility to regain it. The losses have to be replenished by newly recruited troops.
Moral damage on the other hand regenerates at the end of the empires military turn.
In addition to that each army if one of two types:
Sea army or Land army.
Sea armies can only exist in sea regions and move faster than land armies.
Land armies can exist in any region, but do no take part in conflicts resolved in a see region. If involved in a conflict in a sea region they are either protected by a friendly sea army or destroy outright.

### 2. The economy round
During the economy round all empires can go through the following steps in parallel.
	1. Generate Income
	2. Pay Upkeep
	3. Build new Troops
	4. Update Region status

#### 1. Generate Income
Each region generates its production value in gold and adds it to the treasury.
This production might be modified by the following condition:  
	**Taxed/Plundered:** A taxed/plundered region is considered to have a production value of zero.  
	**Salted/Burned:** A salted region is considered to have a production value of zero and will be marked as taxed/plundered on the next economic round.  
	**Occupied (by a hostile empire):** An occupied region doesn't provide its production value to the owner, but instead provide 20% of its production to the occupying empire.

#### 2. Pay Upkeep
Sustaining a military is a costly matter and the bigger it gets the higher the expanses get.
At this point the value of any owned army may be reduced to any lower number.
The remaining maximal value of all owned armies is summed up and used to calculate the cost of upkeep using this formula:  
**Upkeep Cost** _f(x) = (3/140000)\*x^2 - 1,35714285714286\*x + 21428,5714285713_  
**Exception:** Should your total army value be below 30.000, the upkeep cost is 0.

#### 3. Build new Troops
Now it is time to build new armies and reinforce the existing ones. This process is called raising troops.
The amount of gold that can be used to raise troops is limited to the total production value of the entire empire at the current time.
There is no limit to the amount of troops that can be raised at a single location, but troops can only be raised at specific locations.
These location are:  
- all own fortifications not affected by a negative status effect
- all sea regions adjacent to an own fortifications with no negative status or enemy army inside
- all own rested armies in owned regions not affected by a negative status effect.  

Each gold coin spent is added to both the current and the maximal value of the army.

#### 4. Update Region status
The last step in the economy round is to update the status in each region.
Remove all the taxed/plundered status effects. Then convert all salted/burned status effects to taxed/plundered.
Occupied status effect is not changed.

### 3. The military rounds
In a military round each empire takes a turn in turn order.
During its military turn each empire performs the following steps:
	1. Update Status
	2. Movement of Armies
	3. Resolve Conflict or take action
	4. Recovery of moral

#### 1. Update Status
Clear all status effects from all owned armies. This includes both negative and positive status effects like exhaustion and well rested.
If the status of a region (like dangerous, bare, or salted/burned) affects an army located in it, resolve them now.

#### 2. Movement of Armies
Move all armies of an empire at the same time.
Land armies may move 1-2 regions without penalties or 3-4 regions and get the exhausted status.
Sea armies may move 1-4 region without penalties or 5-8 regions and get the exhausted status.
During this movement an army may move into a region with an enemy army, but not trough it.
If needed, any owned army may be split into smaller armies at no additional cost at the start of movement.
Should any region contain more than one friendly land army after moving and updating the locations of all armies, unite them into one single land army. Do the same for all sea armies.
These united armies have each status of the constituent armies. Each pair of _well rested_ and _exhausted_ cancels each other out.

#### 3. Resolve Conflict or take action
Should one of your armies now stand in the same region as an enemy army it is time to resolve a conflict with **_glorious_** combat.
As this will be a longer segment, it is be addressed in its own section after the military turn is completely described.
For now it is enough to understand that all participating armies may sustain a reduction to their current and/or maximal strength and one or both armies will be destroy and/or retreat to an adjacent region.
Should an army retreat, it gets the exhausted status and must move to an adjacent region without enemy troops in it.
If more than one army retreat they are resolved in turn order, starting with the next empire in that order, such that the current empire resolves last.

If an army is not resolving a conflict it may perform any of the following action with the region it is currently in:
	1. plunder/tax: Add the production value of the region to the army's empire treasury.
		The region gets the taxed/plunders status. (Its production value is now considered zero)
	2. salt the land/burn the earth: This works similar to plunder/tax but the region gets the status salted/burned instead of taxed/plunders.
	3. siege: If the region is adjacent to a fortification, the fortification gets the besieged status.
			The besieged status is removed at the start of a turn if there is no hostile army in the region neighboring the fortification.
	4. occupy/free the region: The region gets the occupied (by the current empire) status effect or removes the occupied status.
	5. rest and recover: If an army didn't move and takes this action it gets the well rested status.

#### 4. Recovery of moral
At the end of the empire's military turn, the current value of all their armies becomes the maximal value.

After this the next empire in turn order takes its military turn, until all have taken a turn and the next round begins.

### 4. Resolving Conflict
When resolving conflict in **_glorious_** combat, it is done between two sides in the following steps:
1. Calculate the current total strength of both sides  
	Simple announce the current value of each army. This is their strength.
2. Calculate the strength advantage of the bigger army  
	A = current Value Stronger Army,  
	B = current value weaker Army,  
	Strength advantage = (A-B)/B in % or (A/B) in percent - 100%
3. Determine the Strategic Advantage of each side  
	For each side consult the strategic advantage table and determine the total advantage in %
		well rested status +10%
		exhausted status -20%
		Defending main homeland +20%
		Fortification level 1-4 +10% per level
		In enemy territory -20%
		Last Stand (No retreat possible) +30%
		Heroes in the Army +3% / Grad
		Enchantment Trading Cards level 1-3 +10% per level
4. Roll the dice and add advantages  
	Each side rolls a w100/w% and adds its strategic advantage and the stronger army also adds it's strength advantage.
	The higher result it considered the winner, the lower result is considered the loser.
5. Determine and inflict loses  
	Subtract the losers result from the winners result and consult this table for the damage each side sustain.
	The damage is always a percentage of the current or maximal value that is deducted from the respective stat.


		| Difference | Outcome | Winner | Loser takes damage |
		|---|---|---|---|
		| -+50 | Draw | 10% of current + 5% of maximal | 10% of current +  5% of maximal |
		| 51-100 | Minor | 10% of current + 5% of maximal | 20% of current + 10% of maximal |
		| 101-200 | Major | 5% of current + 5% of maximal | 30% of current + 15% of maximal |
		| 201+ | Superior | 10% of current + 5% of maximal | 100% of current + 50% of maximal |
6. Retreat  
	Should any army now be reduced below a current value of 1000 it is disbanded and removed from the game.
	Each side decides simultaneously if they want to abandon the conflict and retreat.
	If none retreat, the conflict continues. Repeat the steps 1-6.
	If only one side retreats it moves to a adjacent region and the other side stays in the region.
	Should both sides retreat, the defender decides first where to retreat to.
