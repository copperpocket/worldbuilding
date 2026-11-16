# Projects

How each game uses the world. Development details stay in each project's own docs; only lore-relevant notes are here.

## Magic vs Martial (TCG)
- **A lore introduction to the larger RPG.** CANON
- **Frame story:** the shipped game is planned as a **card shop simulator set on modern-day Earth** that sells this TCG; customers play it in the shop and trade duplicates at the counter for store credit. CANON (setting), DRAFT (details)
- **The card game may also exist inside the fantasy world**, so the RPG can include it or nod to it. A match might be a battle, and tournaments could recreate famous battles. DRAFT ("leaning, not decided")
- **Design feel:** "an RPG party battle": positioning, Casters and fighters each fighting their own way, Champions who level up. CANON
- Race is background only on cards; no race-synergy mechanics. CANON
- Original prototype deck names: The Arcane Circle and The Iron Company. PLACEHOLDER

## beautiful-tree (RPG prototype)
- **The framework for the eventual full RPG:** state-machine movement, animation, attacks, basic quests. One test zone (Alpha Island), one quest ("Training Day"), five abilities, two enemy types, one NPC.
- "beautiful-tree" is the repo and Unity product name; whether it means anything in the world is open. PLACEHOLDER
- **Genre conventions are borrowed openly from WoW-style MMOs:** quest markers, a quartermaster quest giver, evade and leash behavior, global cooldown, Mana/Energy/Rage/Focus, level cap 60. These are mechanical, not in-world, and the class-based parts may conflict with the no-classes vision (see open questions).
- **Quest "Training Day":** "Those dummies won't break themselves. Destroy five of them." Reward 100 XP. On completion: "Not bad. You might survive out there after all." DRAFT (tutorial)
- **Art direction for magic:** fire orange, frost light blue, healing green, melee red-brown; pastel level-up text. DRAFT

## still-blade
- **Set in a human kingdom** on a mid-sized continent: the capital's province, a nearby cool province and the wilds beyond, not a whole continent. See `locations.md` and `human-kingdoms.md`. DRAFT. People there are trained from youth into one of four paths (Attacker, Defender, Ranged, Magic); see `specializations.md`. The player picks a path at creation. DRAFT
- **Structure:** one seamless open world with separate instanced places: the intro (a threshold, levels 1-2), the tournament grounds, the training grounds and future dungeons. The intro town and its surroundings cover about levels 3-10; the capital is introduced around level 10. Sizes and names PLACEHOLDER. DRAFT
- **Three separate resources:** every character has health, stamina and one discipline pool, Magic or Martial. Stamina is its own pool, restores by sitting, and pays the line attack. CANON (user decided; a game mechanic)
- **Charges and momentum:** charges are built by landed basic attacks and spent by the E area skill; a momentum meter fills with kills in quick succession and, when full, gives a short burst of faster attacks and free E. DRAFT (a game mechanic; numbers to tune)
- **Player killing and infamy:** players can attack each other past the protected starting area by choosing a mode (Peace, Guard, Fray, Open). Attacking an innocent marks an Aggressor; killing one adds infamy, which fades. Higher infamy makes an Outlaw, then Condemned, refused by vendors and artisans and dropping more on death. Towns are safe. An "exposure" idea weakens a killer's defences gradually. DRAFT (game rules; all names PLACEHOLDER; no in-world law or reason is given and none is invented)
- **The player character is always human** (male or female, human customization). The idea: only humans may take part in a tournament held in the human kingdom, and only humans are allowed there. Other races can still appear out in the world. DRAFT ("the idea could be")
- Martial energy restores only out of combat (stamina loop). See `magic-and-martial.md`. DRAFT
- A prestige / rebirth system is a deferred idea. DRAFT

## Third project
TBD. Add a section here when it starts: what the game is, and which parts of the world it uses or develops.
