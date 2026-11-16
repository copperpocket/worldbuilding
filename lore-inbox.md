# Lore Inbox

New lore captured by `/handoff` from any project, waiting for `/lore-review`. Entries are appended below; do not edit them by hand unless you want to.


### 2026-10-23 — still-blade
- **Three separate resources.** Every still-blade character has health, stamina and one discipline pool, Magic or Martial. Stamina is a separate pool that everyone has and that restores by sitting. "Magic" and "Martial" are the names of the discipline pools; path skills spend them, and weapon skills spend stamina.
  - Status: CANON (user decided)
  - Source: still-blade `docs/PLAN.md` (Phase 16), `ScriptableObjects/Resources/SO_Res_Stamina`, `SO_Res_Martial`, `SO_Res_Magic`
  - Conflicts: `projects.md` says Martial energy restores only out of combat (the stamina loop), and Q42 builds on that. Stamina is now its own pool, and Martial restores during combat (see the next item). Also relates to Q39 (power types tied to Magic and Martial).
- **How the disciplines restore.** Magic and Martial both restore the same way for now: a steady trickle, including during combat.
  - Status: DRAFT (user: "keep them both the same for now")
  - Source: still-blade `SO_Regen_Discipline`, `docs/PLAN.md` (Phase 16)
  - Conflicts: as above (`projects.md` and Q42).
- **Skills come from the path, not the weapon.** Q is the path's basic line attack and E is a skill only that path has; both need one of the path's weapons in hand. Weapons no longer grant skills.
  - Status: CANON (user decided; a game mechanic)
  - Source: still-blade `docs/PLAN.md` (the design section and Phase 18)
  - Conflicts: Q45 assumes still-blade grants skills from weapons; that is no longer true.
- **Path identities.**
  - Attacker masters the line attack and is far stronger with it in the open world.
  - Defender blocks line attacks.
  - Ranged clears groups and can briefly fly out of melee reach.
  - Magic will be an easy-to-aim, area-damage caster that is fragile (Attacker lines can one-shot it).
  - Every path can line attack, and lines are equal except for damage, so a tournament can count hits landed fairly.
  - Status: DRAFT (agreed design, may change after testing)
  - Source: still-blade `docs/PLAN.md` (the "Design: path identities and the line attack" section)
  - Conflicts: none known. Ranged flying has no in-world explanation (how a human flies through Martial training); not invented.
- **Magic weapons.** Staff, Wand or Focus; the game currently has a Staff type with a "Training Staff".
  - Status: PLACEHOLDER
  - Source: still-blade `ScriptableObjects/Items` (the staff type and weapon)
  - Conflicts: "Focus" is also a beautiful-tree power-type name (glossary, Q39).
- **Skill names.** Line Strike, Guard Cut, Piercing Shot, Staff Bolt, Fan Shot, Snare Shot, Brace, Take Wing, Vault, Lunge, Frenzy, Challenge, Bash, Ward, Repel and Storm. Hail and Wide Sweep are set aside.
  - Status: PLACEHOLDER
  - Source: still-blade `ScriptableObjects/Skills/SO_Skill_*`
  - Conflicts: none.

### 2026-10-23 — still-blade
- **Two tournaments.** The grand tournament, where gear matters and Attackers win most of the time, with rare exceptional players from other paths winning in creative ways. The lesser tournament counts landed line attacks only (no damage, no E skills), so anyone can compete without maxed gear. More tournaments for other paths may come later.
  - Status: DRAFT (user's design direction, "not a focus yet")
  - Source: still-blade `docs/PLAN.md` ("Design: tournaments", Phase 21)
  - Conflicts: none known.
- **Martial Power and Magic Power.** Gear carries power of one energy; only someone trained in that energy can draw on it, so Martial gear does nothing for a Magic user's power and the reverse. User's reasoning: individuals must train to use Martial or Magic, so a peon can't wear a Martial ring and use it, and a Martial fighter harnessing Magic is "illegal in lore anyway".
  - Status: DRAFT (mechanic agreed; the stat names are PLACEHOLDER, following the energy names)
  - Source: still-blade `docs/PLAN.md` (Phase 22), `Scripts/Runtime/Items/GearDefinition.cs`, `GearRules.cs`
  - Conflicts: `magic-and-martial.md` says holding both energies is possible but very rare (CANON, TCG) and describes prejudice against mages; it doesn't say using Magic as a Martial fighter is illegal. The "illegal" claim needs confirming.
- **Line attacks from kill-earned power (idea, unsettled).** User floated that the ability to line attack comes from a power gathered only from creature kills and other experience in this region, which would explain why line attacks aren't a thing in other regions. User called it "a cheap out" and was torn.
  - Status: DRAFT (undecided)
  - Source: none (discussion only)
  - Conflicts: close to "Bloodrush" in `glossary.md` (Martial energy gained from kills, PLACEHOLDER, TCG). Whether line attacks are region-specific is not recorded anywhere.
- **More skill and item names.** Skills: Surge (Magic's targeted lightning-like strike), Keen Edge (Attacker's line-empowering skill). Items: Training Charm (a Magic ring), plus Training Band, Cap, Vest, Pendant and Boots; gems Strike, Guard, Vigor and Swift Gem.
  - Status: PLACEHOLDER
  - Source: still-blade `ScriptableObjects/Skills/SO_Skill_Surge`, `SO_Skill_KeenEdge`, `ScriptableObjects/Armor/SO_Armor_Training*`, `ScriptableObjects/Gems/`
  - Conflicts: none.

### 2026-11-01 — magic-vs-martial
- **Hybrid spec prerequisites.** A Hybrid spec's prerequisites would be very demanding (both energies, great discipline), which keeps Hybrids rare.
  - Status: DRAFT (listed under "Ideas" in the old lore file)
  - Source: magic-vs-martial `docs/lore/World.md`, before commit `5f33375` (the "Classes and skills" section)
  - Conflicts: none known.

### 2026-11-11 — still-blade
- **The Guide and the Quartermaster in the starting area.** The RPG's first zone is a walled training ground where new characters start. Two NPCs stand by the spawn: the Quartermaster, who gives starter orders based on where the character is (gruff drill-sergeant tone, reusing the existing DRAFT character), and the Guide, a separate, friendlier NPC who gives general gameplay tips on request (inspired by the guide NPC in sandbox games). A gate east leads "out there" to the field.
  - Status: DRAFT (user decided to have both NPCs; "Guide" is a PLACEHOLDER name; their dialogue is placeholder game text)
  - Source: still-blade `Scripts/Editor/Builders/FirstZoneSceneBuilder.cs`, `ScriptableObjects/Dialogue/SO_Dialogue_Quartermaster.asset`, `SO_Dialogue_Guide.asset`, `docs/PLAN.md` (Phase 28)
  - Conflicts: `characters.md` calls the Quartermaster "the only NPC and quest giver" (RPG prototype); still-blade now has the Guide and the Artisan as well. `locations.md` describes the prototype's zone ("Alpha Island") as having the Quartermaster, dummies and wolves; still-blade's first zone has no monsters.
- **Correction to the item above (same day): an intro, then the first city.** The user reshaped it. New characters start in a one-way **intro** (a training ground run by the Quartermaster, with dummies and a pen of weak monsters); once they leave they can never return. The gate leads to the **first city** (unnamed placeholder), where the **Guide** stands prominently in the central plaza as the obvious first NPC to talk to, with the artisan's yard, a market of placeholder vendors (Weapon, Armor, Goods; shops not open yet), and a north gate to the fields. The user cited Conquer Online's flow (intro, then its first city) as the model; none of its names are used. A separate **Training Grounds** players can enter any time may come later.
  - Status: DRAFT (user's design direction; all names PLACEHOLDER)
  - Source: still-blade `Scripts/Editor/Builders/IntroSceneBuilder.cs`, `CitySceneBuilder.cs`, `ScriptableObjects/Dialogue/SO_Dialogue_CityGuide.asset`, `SO_Dialogue_IntroQuartermaster.asset`, `SO_Dialogue_VendorClosed.asset`, `docs/PLAN.md` (Phase 28)
  - Conflicts: as above for the Quartermaster ("the only NPC"); the prototype's "Alpha Island" had wolves, still-blade's intro has generic weak monsters.
- **Correction (same day): one open world.** The first city is no longer its own scene: it sits inside the open world, walled, with openings straight into the surrounding fields (camps tougher the farther from the city). The user's long-term goal is one continuous world, with a few separate places (e.g. the tournament grounds, possibly a market). The intro stays separate and one-way.
  - Status: DRAFT (user's design direction; names PLACEHOLDER)
  - Source: still-blade `Scripts/Editor/Builders/WorldSceneBuilder.cs`, `docs/PLAN.md` (Phase 29)
  - Conflicts: none known.

### 2026-11-13 — still-blade
- **Metal coin currency.** Money is copper, silver and gold coins (100 copper to a silver, 100 silver to a gold, shown as e.g. "1g 20s 5c"). Humanoid monsters carry coin. Beasts don't; they drop sellable parts instead.
  - Status: PLACEHOLDER (a game-system choice; no lore reason was given for either)
  - Source: still-blade `Scripts/Runtime/Items/CurrencyDefinition.cs` (`Money`), `docs/PLAN.md` (Phases 39-40)
  - Conflicts: `items.md` says the RPG prototype has no currency. Nothing contradicts metal coins.
- **Beast parts, a tonic and new skill names.** Items: Pelt and Fang (beast parts, sold to vendors) and Second Wind Tonic (a potion that refills the area skill's resource). Skills: Whirl (a melee area spin). Skyiron and Shardstone are now rare finds that glow on the ground and are announced nearby.
  - Status: PLACEHOLDER
  - Source: still-blade `ScriptableObjects/Items/`, `ScriptableObjects/Skills/SO_Skill_Whirl`, `docs/PLAN.md` (Phases 40-45)
  - Conflicts: `glossary.md` also uses "Second Wind" as a path skill and a TCG Martial healing name; the tonic reuses it.
- **The world around the first city.** The first city sits in the corner of a 400 m open area. Monster regions get tougher the farther from the city (levels 1-2 near it, up to 9-10 at the edge), with a level 10 elite in the far corner beside a closed road leading beyond. The user wants a much bigger world later, shaped by routes like bridges and passes rather than an open square, possibly with transport between areas.
  - Status: DRAFT (the layout is the user's direction; numbers and names PLACEHOLDER; where the closed road leads is undecided)
  - Source: still-blade `Scripts/Editor/Builders/WorldSceneBuilder.cs`, `docs/PLAN.md` (Phase 44)
  - Conflicts: none known.

### 2026-11-14 — still-blade
- **The world is one seamless open world, with separate instanced places.** The first continent is planned at 2 x 2 km, walked or crossed without loading screens. The intro, the training grounds, the tournament grounds and future dungeons stay separate places. For now the area around the first city is 1 x 1 km, with the same five level regions stretched outward (levels 1-2 nearest the city, 9-10 at the far edge, the elite and the closed road in the far corner).
  - Status: DRAFT (the user's structural decision; sizes and names PLACEHOLDER)
  - Source: still-blade `docs/PLAN.md` (Phase 56), `Scripts/Editor/Builders/WorldSceneBuilder.cs`
  - Conflicts: refines the 2026-11-13 inbox entry ("The world around the first city", 400 m), which this supersedes in size; none with the lore files.

### 2026-11-14 — still-blade
- **Charges and momentum.** Two more combat counters beside health, stamina and the discipline: charges (built by landed basic attacks, spent by the E area skill) and a momentum meter (filled by kills in quick succession; full, it gives a short burst of faster attacks and free E). Stamina now pays only the line attack.
  - Status: DRAFT (user chose the direction; a game mechanic, numbers to tune). Names PLACEHOLDER.
  - Source: still-blade `docs/PLAN.md` (Phase 57), `ScriptableObjects/Stats/SO_Res_Charge`, `SO_Res_Momentum`, `SO_MomentumRules`
  - Conflicts: the 2026-10-23 inbox item "Three separate resources" (CANON) says each character has health, stamina and one discipline, and that weapon skills spend stamina; E (an area skill) no longer spends stamina.
- **First open-world area layout.** Beyond the first city's level 1-10 area lies a river (crossed at two bridges and a corner crossing) and, farther out, a ridge with two passes; levels 11-20 lie beyond the river. Two small outposts (vendor, artisan, a keeper) sit along the way, and fallen players wake at the nearest town.
  - Status: PLACEHOLDER (test world geography and names: "Field Outpost", "River Outpost", "Outpost Keeper")
  - Source: still-blade `Scripts/Editor/Builders/WorldSceneBuilder.cs`, `docs/PLAN.md` (Phase 56 step 3)
  - Conflicts: none known (`locations.md`: no named location exists yet).

### 2026-11-14 — still-blade
- **Player killing, with infamy.** Players can attack each other anywhere past the river around the first city, by choosing a mode (Peace, Guard, Fray, Open). Attacking an innocent marks you as an Aggressor for a short time; killing one adds infamy, which fades with time. At higher infamy a player becomes an Outlaw, then Condemned: their name turns red, then black, vendors and artisans refuse them, and they drop more on death (the Condemned also a worn piece). Victims drop a bag item and some coin. Towns are safe, and the level 1-10 area inside the river is protected.
  - Status: DRAFT (the rules are the user's decisions; a game mechanic). Every name is PLACEHOLDER.
  - Source: still-blade `docs/design/pk-and-tournaments.md`, `docs/PLAN.md` (Phases 66-67), `Scripts/Runtime/Combat/PkRules.cs`, `PkStatus.cs`, `Scripts/Runtime/World/PkZones.cs`
  - Conflicts: none known. No in-world law, guards or reason is given for any of it; not invented.
- **Exposure.** A killer's defences against other players weaken gradually the more infamous they are, and recover while they hunt monsters, then weaken again. The user liked the idea and asked that it be gradual, never a sudden drop.
  - Status: DRAFT (mechanic agreed in principle; numbers to tune). Name PLACEHOLDER.
  - Source: still-blade `docs/design/pk-and-tournaments.md`, `docs/PLAN.md` (Phase 68; not built)
  - Conflicts: none known. Why murder would weaken someone, and why hunting restores them, has no in-world explanation; not invented.
- **Tournament rules.** Refines the 2026-10-23 entry "Two tournaments". Both are single-elimination brackets fought at a tournament ground with several rings, watched by spectators standing around them. The grand tournament has one open bracket for any level and exactly one champion (the user rejected level brackets; a bracketed sister tournament may come later), and is held rarely: weekly or monthly, undecided. Winners earn tournament marks, spent on upgrade materials, and the champion holds a title until the next one.
  - Status: DRAFT (user's decisions; schedule undecided). "Tournament marks" and the title are PLACEHOLDER.
  - Source: still-blade `docs/design/pk-and-tournaments.md`, `docs/PLAN.md` (Phases 69-70; not built)
  - Conflicts: none known. Who runs the tournaments and where the ground is are unknown.
- **Class trainers.** Path skills beyond the basics are learned from a trainer of your own path, for coin, once you reach the skill's level. One trainer per path stands in the first city ("Attacker Trainer", "Defender Trainer", "Ranged Trainer", "Magic Trainer").
  - Status: DRAFT (trainers are the user's request; the details were chosen to unblock the build and may change). Names PLACEHOLDER.
  - Source: still-blade `docs/PLAN.md` (Phase 71), `Scripts/Runtime/World/SkillTrainer.cs`, `ScriptableObjects/Dialogue/SO_Dialogue_Trainer_*.asset`
  - Conflicts: `magic-and-martial.md` says Magic is born, never learned, though the gift must be trained; a Magic trainer selling skills for coin fits "trained" but hasn't been checked with the user.

### 2026-11-15 — still-blade
- **The world is a very large planet without global maps.** The user recalls deciding that the world of this repo is a very large planet whose peoples have no complete map of it. Some kingdoms are so far apart that they have no direct contact, and peoples on different continents may not even know each other exist.
  - Status: DRAFT (the user remembers it as decided, but no lore file records it; confirm at review)
  - Source: none yet (stated by the user in a still-blade session)
  - Conflicts: none known. Fits `overview.md` ("conflicts are regional, never universal or planetary"). Raises open questions: which continent and kingdom still-blade is set in and how large a slice of it the game shows (`projects.md` says only "an unnamed region"; Q7, Q11), and where the long-term MMORPG (not yet listed in `projects.md`) and the card game sit relative to it.
- **still-blade's first continent shape is a placeholder.** The game's 2 x 2 km area was given a coastline with sea all round (2026-11-15) as a stopgap; the user found it unnatural and wants the continent's shape decided from references first, then still-blade's region cut from it.
  - Status: PLACEHOLDER
  - Source: still-blade `docs/PLAN.md` (Phase 73), `Scripts/Editor/Builders/WorldSceneBuilder.Continent.cs`
  - Conflicts: none known.

### 2026-11-15 — worldbuilding (placing still-blade in the world)
- **Confirmed: a very large planet, several continents, no complete map.** The user confirmed the 2026-11-15 still-blade entry above as DRAFT. The peoples of still-blade's continent know several other continents through trade (so there is sea contact, and their continent has ports somewhere). Continents beyond those may be unknown to them.
  - Status: DRAFT (user: "Yes, but DRAFT"; "Several, known by trade")
  - Source: user, in a worldbuilding session
  - Conflicts: none. Extends `peoples.md` (CANON): "The world is vast… One kingdom may know of another on the far side of the world only through rumor." Which races live on still-blade's continent is undecided (Q52).
- **still-blade's place in the world.** still-blade's kingdom is one of several human kingdoms. The game's 2 x 2 km open world is one province of that kingdom, not the whole kingdom. The first city is a provincial city, not the capital. Whether the province is coastal or inland waits until a continent shape is chosen.
  - Status: DRAFT (user's answers)
  - Source: user, in a worldbuilding session
  - Conflicts: answers part of Q43 ("one human kingdom or several?": several). `projects.md` says still-blade is "set in an unnamed region"; this narrows it. Coast, capital location and the province's neighbours are open (Q48).
- **The MMORPG is the eventual full RPG.** The user's long-term MMORPG is the "eventual full RPG" that beautiful-tree prototypes. Where it takes place relative to still-blade (same continent, another continent, a later era) is undecided. Which places and eras the card game's cards draw on is also undecided.
  - Status: DRAFT (user: "Yes, same game"; the rest undecided)
  - Source: user, in a worldbuilding session
  - Conflicts: `README.md` and `projects.md` describe the long-term goal as "a complete, polished RPG"; neither says MMORPG. Open: Q49, Q50.
- **still-blade's geography is undecided until the world is shaped.** The user has no fixed climate or major features (rivers, ranges, lakes, forests) in mind yet: "we need to figure out the world still!" The test world's river and ridge stay PLACEHOLDER. Where the sky-fallen impact site and the tournament ground sit is also undecided.
  - Status: undecided (recorded so it isn't mistaken for a gap to fill)
  - Source: user, in a worldbuilding session
  - Conflicts: none. Open: Q51, Q53.

### 2026-11-15 — worldbuilding (the planet and the cosmos)
- **The planet is Earth-like but not Earth, in its own universe.** It is a separate universe from ours, so it is not a far past or future Earth.
  - Status: CANON (user: "definitely earth like. not in our universe though this would be its own")
  - Source: user, in a worldbuilding session
  - Conflicts: none. `locations.md` has a modern-day Earth card shop, but that is the TCG's frame setting, outside the world.
- **The planet is larger than an average Earth-like planet.** The size explains the great distances between kingdoms, and why peoples on different continents may not know each other.
  - Status: CANON (user's decision)
  - Source: user, in a worldbuilding session
  - Conflicts: none. Extends the DRAFT "very large planet" entry above.
- **Several large continents, not one supercontinent.** A handful of big continents, explicitly not a single Pangaea-like landmass. Exact number and shapes are undecided.
  - Status: CANON for "several, not one"; the count and shapes are undecided
  - Source: user, in a worldbuilding session
  - Conflicts: none. Feeds Q48, Q51, Q52.
- **The sky-fallen materials are fragments of a cracked moon.** Skyiron, Starheart and Shardstone come from pieces of a moon that broke. What cracked it is a mystery to the inhabitants and, for now, to the author: it could be a natural cosmic event or something mystical.
  - Status: DRAFT (user likes the idea; cause deliberately left open)
  - Source: user, in a worldbuilding session
  - Conflicts: `history.md` says "something fell from the sky (perhaps a meteor)" in one human kingdom's region; a moon fragment fits, but whether the fall hit one region or many is open (Q46, Q53, Q54).
- **Creation is unexplained for now, but needs an in-world myth before the game ships.** The inhabitants wonder where they came from and hold their own creation myth(s); they need not be correct. The author's own answer stays open and may grow as the world is built. Magic and Martial energy suggest some cosmic or higher power; hint at it early and keep a rough plan.
  - Status: DRAFT (user's direction). The myth's content is not decided.
  - Source: user, in a worldbuilding session
  - Conflicts: none. Open: Q54, Q55.

### 2026-11-15 — worldbuilding (continents and kingdom scale)
- **Five or six continents.** The planet has five or six large continents.
  - Status: DRAFT (user: "yes 5 or 6"; the exact count, sizes and shapes are undecided)
  - Source: user, in a worldbuilding session
  - Conflicts: none. Narrows Q56.
- **No kingdom rules a whole continent, barring a rare exception.** A continent is too vast, and holding it would need too many resources, so every continent holds several realms. This applies to all continents.
  - Status: CANON (user's decision; the rare exception is allowed but none is defined)
  - Source: user, in a worldbuilding session
  - Conflicts: none. Fits `overview.md` ("conflicts are regional").
- **The grand tournament's kingdom is only part of its continent.** still-blade's kingdom, which holds the grand tournament for line attacks, covers only a portion of one continent. Its province is a smaller slice of that kingdom.
  - Status: CANON (user's decision)
  - Source: user, in a worldbuilding session
  - Conflicts: refines the 2026-11-15 entry "still-blade's place in the world".
- **still-blade's playable world is the kingdom plus the wilds beyond, not a whole continent.** The game reaches outside the kingdom so players can venture into the wilds for adventures, but it does not cover the entire continent. The user is making this a new decision, because notes in the still-blade repo suggest the whole continent is the goal.
  - Status: DRAFT (user's new direction for still-blade; where it ends is undecided)
  - Source: user, in a worldbuilding session
  - Conflicts: still-blade `docs/PLAN.md` (Phase 56) and the 2026-11-14 inbox entry "The world is one seamless open world" call the 2 x 2 km area "the first continent". That wording is now wrong: the area is part of a province, and the playable world is bigger than one province. Those notes need updating in that repo.

### 2026-11-15 — worldbuilding (still-blade's continent and coast)
- **still-blade's continent is mid-sized.** A long coastline is not a priority.
  - Status: DRAFT (user: "mid-sized makes sense to start with i think")
  - Source: user, in a worldbuilding session
  - Conflicts: none. Narrows Q56.
- **still-blade's kingdom is coastal.** The first kingdom built out in this repo sits on a coast. Sea travel (boats, ships) is a normal way to travel, which fits a grand tournament that draws entrants from afar.
  - Status: DRAFT (user: "i do like the idea")
  - Source: user, in a worldbuilding session
  - Conflicts: none. Answers the kingdom half of Q48; whether the province itself is coastal is still open.

### 2026-11-15 — worldbuilding (the province's coast)
- **still-blade's province is coastal.** The province touches the sea. The sea can bound the playable map, with the wilds inland.
  - Status: DRAFT (user: "yes coastal province works, go with that")
  - Source: user, in a worldbuilding session
  - Conflicts: none. Answers Q48's coastal-or-inland half; the capital, ports and neighbours are still open.

### 2026-11-15 — worldbuilding (climate and the province's distance from the capital)
- **The province is far from the kingdom's capital.** It is quite a jump away and may not even be the closest province. It is only still-blade's starting area; the player reaches the capital as they progress.
  - Status: DRAFT (user's direction)
  - Source: user, in a worldbuilding session
  - Conflicts: refines the 2026-11-15 entry "still-blade's place in the world" (provincial city, not the capital). Where the capital sits relative to the province is still open (Q48).
- **Climate mixes temperate and cool maritime.** The land around the capital is temperate, chosen as a good place for the kingdom's first settlers to build up. Nearer the province it is cool, misty and maritime.
  - Status: DRAFT (user: "mix of both"; temperate near the capital, cool and misty near the province)
  - Source: user, in a worldbuilding session
  - Conflicts: none. Partly answers Q51 (climate); major features are still open.
- **Seasons exist in the world.** The lore has natural seasons. Whether a game shows them is up to that game.
  - Status: CANON (user: "something that exists in the lore of our world for sure")
  - Source: user, in a worldbuilding session
  - Conflicts: none. An Earth-like planet with seasons implies an axial tilt; not stated, not invented.

### 2026-11-15 — worldbuilding (continent layout)
- **Layout of the kingdom's continent.** A mountain range along one side of the kingdom shelters its heartland. A great river runs from the range to the sea, and the capital sits near its mouth or on its plain in the temperate land. Farther along the coast, a long trip away, lies the cool and misty region with moors, marsh and forest inland. Unclaimed wilds lie inland from it.
  - Status: DRAFT (user: "i like the ideas you suggested for layout")
  - Source: user, in a worldbuilding session (layout proposed by Claude)
  - Conflicts: none. Partly answers Q51 and Q48 (neighbours and ports are still open).
- **The still-blade test world's layout is discarded.** The river, ridge and passes in the test world are not kept. The lore layout is decided here first, then applied to the game in a later session.
  - Status: CANON (user's decision on process)
  - Source: user, in a worldbuilding session
  - Conflicts: supersedes the 2026-11-14 inbox entry "First open-world area layout", which was PLACEHOLDER.
- **The intro place is not the marshy province.** The user wants the intro (starting) place to be something other than the marshy province discussed earlier. What it is, and its relation to the province, is undecided.
  - Status: DRAFT
  - Source: user, in a worldbuilding session
  - Conflicts: refines "still-blade's place in the world" (the province is the 2 x 2 km area with the first city). Which of the two now holds the first city is open.

### 2026-11-15 — worldbuilding (human kingdom structure and titles)
All of the following is for human kingdoms only. Other races will have their own. Every title is a PLACEHOLDER as a name, per the naming rule.
- **Two kinds of word.** Political words describe belonging (kingdom, province, seat, capital, grant); place words describe size (city, town, village, hamlet, fort or outpost). A place can hold a political role: a town can be a province's seat.
  - Status: DRAFT (user: "i like the structure you've laid out")
  - Source: user, in a worldbuilding session
  - Conflicts: none.
- **Settlement ladder, largest to smallest.** City, town, village, hamlet (a few households, no market; a lone dwelling is a homestead), plus fort or outpost (a garrison). Cities are rare, often one per province, and usually a capital or seat; most settlements are towns or villages.
  - Status: DRAFT
  - Source: user, in a worldbuilding session
  - Conflicts: none.
- **Province and seat.** A province is a large region of a kingdom, run by a ruler the crown appoints, usually from a noble family. Its seat is the settlement where the ruler lives and the province is run from, normally its largest place (a city or a town). A kingdom holds several provinces and is never a whole continent.
  - Status: DRAFT
  - Source: user, in a worldbuilding session
  - Conflicts: none.
- **Who appoints whom.** The crown appoints the province ruler; the province ruler appoints town heads and fort commanders; villages and hamlets choose locally, and a hamlet answers to the nearest village. A settlement that follows no standard is allowed.
  - Status: DRAFT
  - Source: user, in a worldbuilding session
  - Conflicts: none.
- **Titles by level.** Kingdom: King or Queen (heir: Crown Prince or Crown Princess). Province: Duke or Duchess (Count or Countess kept in reserve for a lesser region). City: Consul. Town: Reeve. Village: Elder. Hamlet: no ruler. Frontier fort: Warden; keep: Castellan; lesser post: Captain (military ranks still to be defined).
  - Status: DRAFT (user: "yes, all four, record it as DRAFT")
  - Source: user, in a worldbuilding session
  - Conflicts: none.
- **Written and spoken forms.** The title comes before the name, with "of [place]" for formal use ("Duke Corin Hale of Greywater"). Titles are not gendered except King, Queen, Prince, Princess, Duke, Duchess, Count and Countess. Honorifics ("Your Majesty", "Your Highness") are suggestions.
  - Status: DRAFT
  - Source: user, in a worldbuilding session
  - Conflicts: none.
- **City council.** Every city has a council of up to seven offices, led by the Consul: Marshal (guard and defence), Chamberlain (coin and taxes), Magistrate (law), Guildmaster (the trades), Harbormaster (the port, only in a port city), Speaker (ordinary residents). In a seat city the Duke or Duchess rules and the council reports to the Consul, who runs the city. In a chartered city the council governs by vote, the Consul chairs and breaks ties, and the Duke or Duchess and the crown can overrule. A chartered city is a second city in a province, with a crown charter, and is rare.
  - Status: DRAFT
  - Source: user, in a worldbuilding session
  - Conflicts: none.
- **Town moot.** Large or rich towns may have a Town Moot of guild heads and elders that advises the Reeve. Small towns have none. A village may have an elders' circle.
  - Status: DRAFT
  - Source: user, in a worldbuilding session
  - Conflicts: none.
- **The royal family is small.** The crown, the consort (Queen Consort or Prince Consort), the children (Prince or Princess), the monarch's siblings and parents (a widowed ruling parent is a Dowager). Everyone else is kin of the crown and holds noble titles, so a Duke is often a close kinsman of the crown.
  - Status: DRAFT (user: "small model works")
  - Source: user, in a worldbuilding session
  - Conflicts: none.
- **Allied grants.** The crown can grant land inside a kingdom to an allied race (dwarves, halflings, elves) as a rare grant. They rule it by their own customs and owe the crown allegiance.
  - Status: DRAFT (user: "interesting... here and there when appropriate")
  - Source: user, in a worldbuilding session
  - Conflicts: `peoples.md` says each race governs itself and even allies only tolerate each other; a grant inside a human kingdom fits only as a rare exception.

### 2026-11-15 — worldbuilding (human kingdom military)
Human kingdoms only. Every title is a PLACEHOLDER as a name.
- **Rank order, top down.** Marshal (the whole army), then Warden (a border region and its forts), then Protector (a city's whole military), then the branch leaders below it, then Captain, Sergeant, Veteran, Soldier, Recruit. Veteran, Soldier and Recruit command no one; a Soldier can rise to Veteran without ever leading. Sergeant is the lowest commanding rank (a squad of about 10). The crown appoints the Marshal and the Wardens (Wardens on the Marshal's advice).
  - Status: DRAFT (user: "pretty sold on Marshal > Warden >", Captain through Recruit "i like")
  - Source: user, in a worldbuilding session
  - Conflicts: `characters.md` lists TCG cards named "Oathsworn Warden" and "Warmaster", and a drill sergeant; those are card names, not kingdom ranks. `specializations.md` has "Militia Recruit" and "Militia Captain".
- **City military.** One Protector commands a city's whole military: the city guard (led by a Commander), the castle guard (led by a Castellan) and any other guard in the city. The Protector answers to the Consul, and to a Warden when required, and sits on the city council. The full structure applies to the capital and seat cities; other cities have a Protector alone, adding a Castellan only if they have a castle and a Commander only if they need a separate watch. A town's guard is a Captain under the Reeve. A village has no guard or a militia under the Elder. A Castellan is the leader of a castle or major fort.
  - Status: DRAFT (user: "Protector is pretty good. Commander is great.")
  - Source: user, in a worldbuilding session
  - Conflicts: replaces the draft "Marshal" council seat from the entry "human kingdom structure and titles": the city council's seven seats are Consul, Protector, Chamberlain, Magistrate, Guildmaster, Harbormaster, Speaker. That entry also names the frontier fort commander Warden, keep Castellan and lesser post Captain, which this entry refines. Whether a Castellan outranks a Commander is undecided.
- **Branches and their leaders.** Every branch ranks Captain, Sergeant, Veteran, Soldier, Recruit beneath its leader. City guard: Commander. Castle guard: Castellan. Field army: Commander. Mounted: Commander. Siege and works: Commander. Frontier: Warden. Fleet: Admiral. Royal guard (in the capital): led by the Protector directly. Branch leader titles are not important to the user; reuse is fine.
  - Status: DRAFT (user's choices; the fleet's lower ranks are undecided)
  - Source: user, in a worldbuilding session
  - Conflicts: none.
- **Knights are an honour, not a rank.** The crown grants knighthood and keeps a register of knights, who swear on accepting the title to answer the crown's call. Any rank can be a knight. Address: "Ser" (neutral).
  - Status: DRAFT (user: "Ser is fine for now")
  - Source: user, in a worldbuilding session
  - Conflicts: `characters.md` has a TCG card "Ironclad Knight"; no rule there about knighthood.

### 2026-11-15 — worldbuilding (the intro area is not the seat)
- **The intro area is not the province's seat.** The Duke or Duchess need not live there, and the user wants the intro area smaller than a seat. A Duke or Duchess almost always lives in a city; a remote province that has not developed a city could have its ruler in a town instead.
  - Status: DRAFT (user's correction)
  - Source: user, in a worldbuilding session
  - Conflicts: overrides the 2026-11-15 notes that the first city is "a provincial city" and the proposal that the starting town is the seat. The intro area's size and name are open.

### 2026-11-15 — worldbuilding (the intro town)
- **The intro area is a town.** It holds the Guide and several NPCs with different goods, which makes it a town and not a village. It is a town so that it is at least a little significant in the player's introduction. It is not the province's seat.
  - Status: DRAFT (user's decision)
  - Source: user, in a worldbuilding session
  - Conflicts: refines the 2026-10 to 2026-11 inbox entries that called it "the first city".
- **The artisan's place is undecided.** One artisan stays in the intro town for testing; in the lore the artisan may live only in the capital. Whether only one person can work the sky-fallen materials or several can is also undecided, and the user says it is not important right now.
  - Status: undecided
  - Source: user, in a worldbuilding session
  - Conflicts: `characters.md` and `items.md` say "the one artisan" (DRAFT) in the tournament kingdom.
