# Lore extract: Magic vs Martial

Everything in this repository that describes the world, collected in one place on 2026-10-20. Nothing here is
new: every entry cites where it comes from, and gaps are listed under Open Questions instead of filled.

**Status labels**
- **CANON**: decided by the developer (marked "Decided" in `docs/lore/World.md`, or stated as a rule or pillar).
- **DRAFT**: clearly meant, but undeveloped (a concept line, a proposal, a "leaning" or an "idea").
- **PLACEHOLDER**: a name or text the repo itself calls temporary, or prototype/test content.

**A note on names.** `docs/lore/World.md` says: "No names yet: everything named in the card game is a
placeholder until the lore has its own." The rules repeat it ("Spec, card and Champion names are placeholders
until the RPG's lore has its own", `docs/rules/GameRules_v0.33.md`). So every proper name below (Champions,
Legendaries, specs, abilities) is a **PLACEHOLDER as a name**, even when the concept behind it is DRAFT or CANON.

**Sources searched:** `CLAUDE.md`, `HANDOFF.md`, `README.md`, `docs/lore/World.md`, `docs/rules/GameRules_v0.33.md`
(and the archived rules), the three `docs/design/Set1_*.md` drafts, `docs/cards/CardList.md`,
`Assets/_Project/Scripts` (data enums, `PrototypeContentGenerator.cs`, `MainMenu.cs`, comments), git history of
`docs/lore/World.md` and the first content commit, and the project's Claude memory notes
(`~/.claude/projects/.../memory/*.md`, outside the repo; cited as "memory"). Short source names used below:

| Short name | File                                                          |
|------------|---------------------------------------------------------------|
| World      | `docs/lore/World.md`                                          |
| Rules      | `docs/rules/GameRules_v0.33.md`                               |
| Set1       | `docs/design/Set1_Draft.md`                                   |
| Expansion  | `docs/design/Set1_Expansion_Draft.md`                         |
| Completion | `docs/design/Set1_Completion_Draft.md`                        |
| CardList   | `docs/cards/CardList.md` (generated from the card data)       |
| Generator  | `Assets/_Project/Scripts/Editor/PrototypeContentGenerator.cs` |
| Enums      | `Assets/_Project/Scripts/Data/Enums.cs`                       |

---

## Overview & Tone

- **The card game is a lore introduction to a larger fantasy RPG** (possibly a future MMO). **CANON.**
  Sources: `CLAUDE.md` (Long-term context), Rules (intro), `README.md`.
- **Dark fantasy, kept grounded:** conflicts are regional, never universal or planetary. **CANON.** Source: World.
- **No "faction vs faction"** (explicitly no WoW-style Alliance and Horde). Each race governs itself, like
  countries or regions in real life (examples given: "human kingdoms, orc chieftains"). **CANON.** Source: World.
- **War between races has broken out many times in history**, and each race has its own conflicts. **CANON.**
  Source: World.
- **Core theme: Magic vs Martial.** Neither is stronger; neither is the villain. Magic must feel just as heroic
  and attractive as Martial. **CANON.** Sources: World ("Magic is not evil"), Rules (Design pillars), `CLAUDE.md`
  ("Never make Magic strictly stronger than Martial", to avoid a "Star Wars Galaxies Jedi" problem in the RPG),
  `README.md` ("Neither is stronger, and neither is the villain"), `MainMenu.cs` tagline ("A trading card game.
  Neither side is stronger.").
- **Rules text never moralizes.** Words like "greed", "drain" or "corrupt" stay out of mechanics; the in-world
  stigma around Magic "is a viewpoint held by characters and factions, not a truth the game asserts, and both
  sides have their own prejudices." **CANON.** Source: Rules (Design pillars).
- **Feel: "an RPG party battle"**: positioning, Casters and fighters each fighting their own way, Champions who
  level up. **CANON** (as a design pillar). Source: Rules.
- **Frame story (outside the fantasy world):** the planned shipped game is a **card shop simulator set on
  modern-day Earth** that sells this TCG; customers play it in the shop. **CANON.** Sources: `CLAUDE.md`, Rules
  (intro), `README.md`, memory (`project-goals.md`, `meta-game-plan.md`: trading duplicates "at a shop counter for
  store credit").
- **The card game may also exist inside the fantasy world** (so the RPG can include it or nod to it); a match
  might be a battle, and tournaments could recreate famous battles. **DRAFT** ("Leaning (not decided)").
  Source: World. See Open Questions for how the two framings fit.

## History/Timeline

The repo holds almost no history. Everything that exists:

- **Wars between races have broken out many times.** **CANON.** Source: World.
- **An ancient history of larger-scale escalations is possible** ("a story for another time"). **DRAFT.**
  Source: World.
- **A great threat that forces the races to band together** is possible later, but is **not** part of the present
  day. **DRAFT.** Source: World.
- **Present day:** no events, dates, eras or calendar are defined. World lists "The world's main present-day
  conflicts (per race)" as an open question.
- **Implied past events on cards** (each only a phrase; see Characters):
  - Vaelith Arandor was exiled "for what she burned." **DRAFT.** Sources: Set1, CardList, Generator.
  - Thoren Ashguard "has never lost a pass he was sent to hold." **DRAFT.** Same sources.
  - "Famous battles from the lore" that tournaments could recreate. **DRAFT.** Source: World.

*Not lore, but easy to confuse:* the dated entries in `docs/rules/`, `HANDOFF.md` and the design drafts are the
development history of the game (rules versions), not in-world history.

## Factions

No factions exist by design ("No 'faction vs faction'", World). What the repo has instead:

### Peoples (races)
- **The six starting races: human, dwarf, halfling, high elf, dark elf, orc.** **CANON.** Sources: World,
  memory (`world-and-races.md`), Enums (`Race`).
- **Others may come later** if the lore fits (undead is the example). **DRAFT.** Sources: World, memory.
- **The races are fiercely independent.** Even allies only *tolerate* each other; some are not allied at all
  and don't allow other races into their capitals unescorted. Which races are allied is not stated. **CANON.**
  Source: World.
- **Governance:** each race governs itself; "human kingdoms" and "orc chieftains" are the only examples of a
  political form. **CANON** (the principle), **DRAFT** (the two examples). Source: World.
- **Magic aptitude is partly in the blood:** some races are more likely to produce Magic users. Any race can
  produce Martial fighters, but culture and available knowledge make some races lean Martial. Which races lean
  which way is **not** stated. **CANON.** Source: World.
- **In the card game, race is background only** (art, name style, a small note on the card), never part of a
  card's or Champion's name, and there are no race-synergy mechanics. **CANON.** Sources: World, `CLAUDE.md`,
  Enums (comment on `Race`), memory.
- **Races should feel like real peoples, not generic units.** **CANON.** Source: memory (`world-and-races.md`).

**Race spread on the current cards** (counted from CardList; units only, tokens excluded). This is what the
cards show, not a stated lore rule:

| Race     | Neutral | Magic (discipline + Binders + Tempest) | Martial (discipline + Bulwark + Reavers) | Champions         |
|----------|--------:|---------------------------------------:|-----------------------------------------:|-------------------|
| Human    |       9 |                                      4 |                                        7 | none (2 raceless) |
| Dwarf    |       2 |                                      1 |                                        5 | Brunhal, Thoren   |
| Halfling |       4 |                                      2 |                                        1 | none              |
| High elf |       1 |                                      5 |                                        3 | Vaelith           |
| Dark elf |       1 |                                      5 |                                        1 | Sylra             |
| Orc      |       1 |                                      3 |                                        4 | none              |

### Combat specializations ("specs")
Specs are paths a character joins, not peoples or nations. The four names are **PLACEHOLDER** ("'Spec' is the
working word; an in-world name can come later", World). Whether a spec is also an organization (an order, a
guild) is not stated; see Open Questions.

- **How a spec is earned:** in the RPG, a character picks a race (not a class) at creation, builds skills over
  their first levels (about 5-10) by training, questing and practicing, and is then offered a **quest to join a
  combat specialization**, which needs skill points and other prerequisites. Leaving one for another "might be
  possible". **CANON** (general vision). Sources: World, Rules ("Lore: characters earn a spec through training and
  a quest... a Champion's deck holds only what their path has taught them"), `Data/SpecData.cs` comment.
- **Tempest** (Magic): destruction, "burn, area damage and damage to the enemy Champion. Fragile, expensive
  bodies." **DRAFT.** Sources: Rules, CardList, Generator.
- **Binders** (Magic): "summoning and control: constructs, Root, slowing the enemy." **DRAFT.** Same sources.
- **Bulwark** (Martial): defense, "Armor, Shield and an unbreakable front line. Wins by making attacks costly."
  **DRAFT.** Same sources.
- **Reavers** (Martial): aggression, "Swift units, finishing damaged enemies, Venom. Low health." **DRAFT.** Same
  sources.
- **Hybrid specs** (both energies) are planned but none exists; "very rare". **CANON** (that Hybrids exist and are
  rare), **DRAFT** (any Hybrid spec). Sources: World, Rules.
- **Sub-specs** (like WoW's Mage -> Frost Mage) are an open idea; the four specs "may turn out to be sub-specs."
  **DRAFT.** Sources: World, Rules, Set1.
- **A Neutral Champion** ("a leader of commoners, beasts and constructs") is listed as a future idea. **DRAFT.**
  Source: Rules (future ideas).

### Other group names
- **The Arcane Circle** (Magic) and **The Iron Company** (Martial): names of the two original 20-card prototype
  decks. **PLACEHOLDER.** Sources: `README.md`, git commit `d3101f8`. The decks were replaced by generated example
  decks ("Brunhal Deepvein Example" etc., CardList).
- **Militia** (Militia Spearman, Militia Recruit "Called to arms", Militia Captain, Call to Arms): commoner
  levies. **PLACEHOLDER** (card names). Sources: CardList, Generator.
- **"Factions"** appears once, as holders of the stigma around Magic (Rules, Design pillars), with no factions
  named. See Inconsistencies.

## Characters

### Champions
Champions are **named characters of the world**, each with a unique ability. **CANON.** Sources: World, Rules.
Who they are (legends of history, present-day leaders, adventurers) is **open** (World). Champions are chosen,
not found in packs (Rules, memory `cards-from-packs.md`).

| Champion         | Race     | Spec    | Concept (verbatim)                                         | Ability (Level 3)                                      | Status                   |
|------------------|----------|---------|------------------------------------------------------------|--------------------------------------------------------|--------------------------|
| Vaelith Arandor  | High elf | Tempest | "A war-mage exiled for what she burned."                   | Ember Lash: damage to a damaged enemy or the Champion  | DRAFT (name PLACEHOLDER) |
| Brunhal Deepvein | Dwarf    | Binders | "A runesmith who raises stone guardians."                  | Runic Binding: strengthen a construct, or a Rune Shard | DRAFT (name PLACEHOLDER) |
| Thoren Ashguard  | Dwarf    | Bulwark | "A captain who has never lost a pass he was sent to hold." | Hold the Line: a unit guards; otherwise Shield         | DRAFT (name PLACEHOLDER) |
| Sylra Vex        | Dark elf | Reavers | "An assassin who leaves no witnesses."                     | Open the Wound: damage a damaged enemy                 | DRAFT (name PLACEHOLDER) |
| The Archmage     | none     | Tempest | "Placeholder Champion from the prototype."                 | Arcane Study: draw a card                              | PLACEHOLDER              |
| The Warlord      | none     | Reavers | "Placeholder Champion from the prototype."                 | Battle Cry: your units get +1 attack                   | PLACEHOLDER              |

Sources for the table: Set1 (Champions), Rules (Champions), CardList, Generator (lines 85-115). The Archmage and
the Warlord "get named and reworked later" (Set1); they are "kept as second Champions of their specs" (Rules).
Their earlier perks: the Archmage's Spells cost 1 less; the Warlord's Vanguard units had +1 attack (Set1, Enums
`ChampionPerk`).

Notes:
- Vaelith is the only Champion with stated pronouns besides Thoren (she / he). The others have none.
- Vaelith's lore phrase "exiled" implies a society that exiled her; who, and what she burned, is not stated.
- Brunhal's "stone guardians" match the Binders' Stone Sentinel and Rune Shard tokens.

### Named Legendary units (cards, not Champions)
All names **PLACEHOLDER**; each has only a name, epithet, race and rules text (no flavor text exists in the data
model: `CardData` has no flavor field; only `ChampionData.concept` holds a description).

| Card                         | Race     | Tier / spec        | What the card says                                         | Status |
|------------------------------|----------|--------------------|------------------------------------------------------------|--------|
| Ilvara, the Last Flame       | High elf | Tempest            | Whenever you cast a Spell, 1 damage to the enemy Champion. | DRAFT  |
| Grandmother Thistle          | Halfling | Binders            | Arrival: Root every enemy unit.                            | DRAFT  |
| Bram Ironvow, the Unbreached | Dwarf    | Bulwark            | Intercept, Armor 1; units next to it have Armor 1.         | DRAFT  |
| The Unbroken Blade           | Orc      | Reavers            | Readies when it destroys a unit in combat.                 | DRAFT  |
| Ysolde, the Unanchored       | High elf | Magic discipline   | Rift Walk (attacks through any lane).                      | DRAFT  |
| Hroth, the Red Harvest       | Orc      | Martial discipline | Sweep (full damage to units next to its target).           | DRAFT  |
| The Ashen Wyrm               | Beast    | Neutral            | Flying; Arrival: 2 damage around it, both sides.           | DRAFT  |

Sources: Set1, Expansion, CardList, Generator. "The Unbroken Blade" dates from the first prototype (commit
`d3101f8`); whether it is a person's title or a weapon isn't said (see Open Questions).

### Roles and archetypes (unnamed characters)
Card names describe roles, not individuals. **PLACEHOLDER** as names; the role idea is CANON ("Names are unique
roles or characters (e.g. 'Grunt', 'Inquisitor')", memory `world-and-races.md`). Grouped by kind, from CardList:

- **Commoners and hirelings (Neutral):** Militia Spearman, Pathfinder, Lookout, Border Scout, Camp Surgeon,
  Lamplighter, Veiled Informant (dark elf), Veteran Sellsword, Tollgate Keeper (dwarf), Slinger, Bounty Hunter
  (orc), Wandering Friar, Herbalist, Caravan Guard, Mercenary Captain, Quartermaster (dwarf), Lorekeeper (high
  elf), Militia Captain.
- **Magic practitioners (Casters):** Apprentice Pyromancer, Hedge Witch (halfling), Ward Apprentice, Battlemage
  Initiate, Spirit Mender, Rift Skirmisher, Rift Mage, Riftweaver (all three dark elf), Storm Adept, Elder Magus,
  Sky Sage; Binders: Stonewright (dwarf), Thornbinder and Archivist of Echoes (dark elf); Tempest: Cinder Zealot,
  Storm Herald, Stormcaller (all orc).
- **Martial fighters:** Longbow Archer, Drill Sergeant, Duelist, Mountain Axeman (dwarf), Outrider, Witch Hunter,
  Blademaster, Griffon Rider, Warmaster; Bulwark: Phalanx Veteran, Shieldbearer, Oathsworn Warden, Shieldwall
  Captain, Ironclad Knight; Reavers: Gap Runner, Venomblade, Bloodrager, Raider Chief.
- **The Witch Hunter** and "inquisitors" are named as **Martial cards with an anti-magic flavor that fit the
  prejudice** against mages; Magic cards "could include mages who hide, protect, or heal." **DRAFT** (Ideas).
  Source: World. The Witch Hunter exists (Arrival: 2 damage to an enemy Caster); no Inquisitor card exists.

## Locations

**No named location exists anywhere in the repo.** What is described:

- **Capitals** of the races, some closed to other races unless escorted. **CANON** (as a fact about the races).
  Source: World.
- **The battlefield:** "two lines facing each other across a field split into lanes; the Champion commands from
  behind their line, open to any enemy who finds a lane with nobody in the way." **CANON** (as the game's lore
  basis). Source: Rules. Earlier version (v0.10): "the Vanguard holds the line far ahead of the Rear, where the
  Champion commands" (`docs/rules/archive/GameRules_v0.10.md`), superseded by lanes.
- **A pass** (Thoren's concept). **DRAFT.** Source: Set1, CardList.
- **Modern-day Earth card shop** (the frame game; it has a shop counter for trading in cards). **CANON** (setting),
  **DRAFT** (details). Sources: `CLAUDE.md`, memory.
- **Terrain words in card names only** (no lore attached): marsh (Marsh Adder), caves (Cave Bear, Cave Troll),
  mountains (Mountain Axeman), borders (Border Scout), tollgates (Tollgate Keeper), caravans (Caravan Guard),
  camps (Camp Surgeon). **PLACEHOLDER.** Source: CardList.

## Magic/Systems (in-world explanation)

### The two energies
- **Magic is drawn from the environment.** Life generates it and releases it outward into the world, "like qi";
  a mage channels what the world around them produces. **CANON.** Sources: World, Rules ("draws its energy from
  the natural world around the caster"), `README.md` ("drawn from the natural world").
- **Magic is born:** without the innate gift, a person can never learn it. **CANON.** Source: World.
- **Martial energy comes from within**, "like jing"; anyone can develop it through discipline and training. At its
  height it is "almost supernatural" and comparable to Magic, but a different energy that behaves differently.
  **CANON.** Sources: World, Rules, `README.md` ("cultivated from within").
- **Both are arts beyond what untrained commoners can do.** **CANON.** Source: Rules (Lore basis).
- **Prejudice:** many see mages as an affront to nature, "taking what isn't theirs", while Martial power is
  earned. This brings disdain and suspicion, **not open war**. **CANON.** Source: World. The rules add that this
  is a viewpoint, not a truth, and both sides have prejudices (Rules, Design pillars).
- **Hybrid:** holding both energies is possible but very rare; they "oppose each other in the body", and it takes
  great discipline and specific circumstances. **CANON.** Source: World. Idea: a Hybrid's energies could pull
  against each other (spending one kind of charge costs or weakens the other). **DRAFT.** Source: World.
- **The words "Magic", "Martial", "Command"** are working names; original in-world names are wanted. **PLACEHOLDER.**
  Sources: World (Open questions), Rules (future: "Original names for Command and the two energies").

### Game mechanics with a stated in-world reason
- **Command** (the resource that pays for everything, growing each turn): "as the battle develops, the commander
  brings more forces to the front." **DRAFT.** Source: Rules (Resources).
- **XP and levels:** "a mage grows by channeling, a fighter by practice" (XP for each charge spent and each enemy
  unit that dies). **DRAFT.** Source: Rules (Champions).
- **Deck limits by spec:** a Champion's deck "holds only what their path has taught them". **CANON.** Source: Rules.
- **Gathering** (Binders, Level 2): "when a unit dies, its life is released into the world and mages can draw on
  it." Ties to "life generates Magic". **DRAFT.** Sources: World (Ideas), Rules, CardList.
- **Stalwart** (Bulwark, Level 2): "a defender who makes every blow cost the attacker; whoever strikes past the
  line at the commander is struck back." **DRAFT.** Source: World (Ideas). It replaced **Banking** ("inner reserves;
  unused Martial charges carry over"), whose lore line was removed in commit `7d94080`.
- **Martial healing:** "Lore supports Martial healing in its own ways (Second Wind)." How is not said. **DRAFT.**
  Source: Set1 (Decisions from review).
- **Cinder Zealot "blood magic":** its Arrival hurts both Champions ("yours too: blood magic"). The words "blood
  magic" appear only in the draft, not on the card. **DRAFT.** Sources: Set1; CardList (current text without it).

### Mechanics with flavor but no stated in-world reason
These are rules that carry a Magic/Martial identity; the repo explains them only as design, not as lore.
- **Casters vs Martial units:** Magic units are Casters (they "channel Spells"); Martial units "perform
  Techniques". **CANON** (rules). Source: Enums (`Discipline` comment).
- **Spells** (Magic), **Techniques** (Martial), **Orders** (paid with Command only, "usable by any Champion").
  **CANON** (rules). Sources: Rules, Enums.
- **Movement is a pillar:** Martial moves its own units, Magic only moves enemy units (Displace), Neutral has no
  movement. **CANON** (rules). Sources: `CLAUDE.md`, Expansion, Completion.
- **Casters' combat damage ignores 1 Armor; only Martial units Overrun.** **CANON** (rules). Source: `CLAUDE.md`.
- **Only Techniques can be played during combat** (Martial-only combat tricks). **CANON** (rules). Sources: Rules,
  `CLAUDE.md`, `HANDOFF.md`.
- **Rift** words: Rift Walk (attack through any lane), Rift Skirmisher, Rift Mage, Riftweaver, Ysolde the
  Unanchored; all Magic. What a "rift" is in the world is not stated. **PLACEHOLDER.** Sources: Expansion, CardList.
- **Runes:** Brunhal "the runesmith", Runic Binding, Runestone Golem, Rune Colossus, Rune Shard ("a rune-carved
  construct"). **DRAFT.** Sources: CardList, Generator.
- **Shield** (Champion-only absorbing pool) vs **Armor** (per-hit reduction on units): deliberately named
  differently. **CANON** (rules). Source: Rules.
- **Warded:** can't be targeted by enemy Spells. **CANON** (rules). Source: Enums.
- **Champion levels 1-3** and spec mechanics unlocked at Level 2: Overchanneling, Gathering, Stalwart, Bloodrush.
  Names **PLACEHOLDER**. Sources: Rules, CardList, Enums (`SpecMechanic`).

## Creatures

Non-people units are races in the code (`Race.Beast`, `Race.Construct`, `Race.Spirit`; Enums), but World.md lists
only the six peoples. All names **PLACEHOLDER**; none has lore beyond its name.

- **Beasts** (all Neutral): Carrion Crow, Hunting Hound, Marsh Adder, Den Mother and its Wolf Pup token, Pack Alpha,
  Ironhide Boar, Cave Bear, Hired Ogre, Ember Drake, Cave Troll, The Ashen Wyrm (Legendary). Sources: CardList,
  Generator.
- **Ridden beasts:** Griffon Rider (a human Martial unit), so griffons exist as mounts. **PLACEHOLDER.** Source:
  CardList.
- **Dragons / wyrms:** Ember Drake (Rare) and The Ashen Wyrm (Legendary). **PLACEHOLDER.**
- **Spirits:** Arcane Wisp (Neutral, Flying), Spark Imp (Tempest Caster). A **Cinder** spirit token existed
  (Set1) and was removed (Rules: "the Cinder token is gone"). **PLACEHOLDER.**
- **Constructs:**
  - Magic-made: Stone Sentinel ("a conjured construct"), Rune Shard ("a rune-carved construct"), Runestone Golem,
    Rune Colossus (Binders), and Brunhal's "stone guardians". **DRAFT.** Sources: CardList, Generator, Set1.
  - Mechanical or crafted (Neutral): Brass Automaton, Siege Ballista, Siege Golem, Powder Keg, Wooden Barricade,
    and the Decoy token (Reavers). **PLACEHOLDER.**
- **Undead:** not present; "may come later if the lore fits." **DRAFT.** Source: World.
- **Ogres and trolls:** appear only as Beasts (Hired Ogre, Cave Troll). See Open Questions.

## Items & Artifacts

**No named artifact exists.** Item-like cards, all **PLACEHOLDER** (names only, no lore):

- **Orders (Neutral gear and supplies):** Field Rations, War Banner, Call to Arms, Supply Run, Caltrops. Rules
  describe the Neutral tier as "commoners, hired swords, beasts, constructs, basic gear." Source: Rules, CardList.
- **Objects that are units:** Powder Keg, Wooden Barricade (both race Construct). Source: CardList.
- **Siege engines:** Siege Ballista, Siege Golem. Source: CardList.
- **The Unbroken Blade:** a Legendary Reavers unit (race Orc). The name could be a weapon or a warrior's title; the
  repo doesn't say. Source: CardList.
- **Runes / runestones:** a Binders and dwarf motif (see Magic/Systems). **DRAFT.**
- **The card game itself as an in-world object** (it may exist inside the world). **DRAFT.** Source: World.

## Glossary

Working terms that have in-world meaning. Status is for the term as a lore word.

| Term                 | Meaning in the repo                                                                        | Status                       | Source                       |
|----------------------|--------------------------------------------------------------------------------------------|------------------------------|------------------------------|
| Magic                | Energy drawn from the environment, generated by life; innate gift only                     | CANON idea, PLACEHOLDER word | World, Rules                 |
| Martial              | Energy cultivated from within through training; anyone can learn it                        | CANON idea, PLACEHOLDER word | World, Rules                 |
| Hybrid               | A rare person or spec holding both energies, which oppose each other in the body           | CANON                        | World, Rules                 |
| Discipline           | Magic or Martial (the energy a spec uses)                                                  | DRAFT                        | Rules, Enums                 |
| Spec                 | Combat specialization, joined through a quest after training                               | DRAFT (word is working)      | World, Rules                 |
| Sub-spec             | A possible secondary specialization at a higher rank                                       | DRAFT                        | World                        |
| Champion             | A named character of the world who commands one side of a match                            | CANON                        | World, Rules                 |
| Command              | The commander bringing more forces to the front as a battle develops                       | PLACEHOLDER                  | Rules                        |
| Caster               | A Magic unit; channels Spells                                                              | DRAFT                        | Enums, Rules                 |
| Spell                | A Magic card or effect                                                                     | DRAFT                        | Rules                        |
| Technique            | A Martial card or effect; the only kind usable mid-combat                                  | DRAFT                        | Rules                        |
| Order                | A one-shot effect any Champion can give, paid with Command only                            | DRAFT                        | Rules, Set1                  |
| Charge               | A unit of Magic or Martial energy available to a Champion each turn                        | PLACEHOLDER                  | Rules                        |
| Arrival              | Effect when a unit enters the battle                                                       | PLACEHOLDER                  | Rules                        |
| Last Echo            | Effect when a unit dies                                                                    | PLACEHOLDER                  | Rules                        |
| Token                | A summoned unit that isn't a card; a lore word (summons, conjurings...) is open            | PLACEHOLDER                  | Set1                         |
| Lane                 | One strip of the battlefield where two units face each other                               | DRAFT                        | Rules                        |
| Rift / Rift Walk     | Magic that attacks through any lane; "rift" undefined                                      | PLACEHOLDER                  | Expansion, CardList          |
| Gathering            | Mages drawing on the life a dying unit releases                                            | DRAFT                        | World, Rules                 |
| Stalwart             | A defender making every blow at the commander cost the attacker                            | DRAFT                        | World, Rules                 |
| Overchanneling       | Taking extra Magic now at the cost of the next turn                                        | PLACEHOLDER                  | Rules                        |
| Bloodrush            | Martial energy gained from kills in combat                                                 | PLACEHOLDER                  | Rules                        |
| Tempest              | Magic spec of destruction                                                                  | PLACEHOLDER                  | Rules                        |
| Binders              | Magic spec of constructs and control                                                       | PLACEHOLDER                  | Rules                        |
| Bulwark              | Martial spec of defense (also the old name of the Intercept keyword)                       | PLACEHOLDER                  | Rules, Set1                  |
| Reavers              | Martial spec of aggression                                                                 | PLACEHOLDER                  | Rules                        |
| Witch / Witch Hunter | "Witch" names a Magic user (Hedge Witch); the Witch Hunter is a Martial anti-magic fighter | DRAFT                        | World, CardList              |
| Vanguard / Rear      | The two rows of the old board (pre-lanes); the Champion commanded from the Rear            | PLACEHOLDER (retired)        | archived rules v0.10, README |

## Open Questions

Gaps the repo implies but doesn't answer. None are filled here.

**From World.md's own list** (Source: World, Open questions)
1. The world's main present-day conflicts, per race.
2. Who Champions are (legends of history, present-day leaders, adventurers) and what a match represents.
3. What the card game is called in the world.
4. Original names for Command, the two energies and the board rows (rows no longer exist; now lanes).

**Implied elsewhere**
5. The world, its continents, realms and capitals have no names. Which races are allied, and which are not?
6. Which races lean Magic and which lean Martial? World says some do; the cards spread every race across both
   (table under Factions), with dwarves mostly Martial and high and dark elves mostly Magic on the current cards.
7. How do the two framings fit: a TCG sold in a modern-day Earth shop, and a card game that may exist inside the
   fantasy world? (World, `CLAUDE.md`.)
8. Are specs also organizations? The plural group names (Binders, Reavers) and the old deck names (The Arcane
   Circle, The Iron Company) suggest groups, but World only describes specs as paths joined by quest.
9. What is a "rift" (Rift Walk, Rift Mage, Riftweaver, Ysolde "the Unanchored")?
10. Are constructs magical? Stone Sentinels are "conjured", Rune Shards "rune-carved", yet Brass Automaton, Siege
    Golem and Powder Keg are Neutral constructs that any Champion can field, and the Binders' Runestone Golem and
    Rune Colossus are listed as non-Caster ("Unit (Neutral)") units.
11. How does Martial healing work in-world (Second Wind)? Set1 says lore supports it "in its own ways".
12. Is blood magic a thing (Cinder Zealot, draft only), and how does it fit Magic being drawn from the
    environment?
13. Is there an in-world reason why Magic moves only enemies and Martial only its own units, why Casters pierce
    Armor, and why only Martial units Overrun?
14. What did Vaelith burn, and who exiled her? Is she connected to Ilvara, "the Last Flame" (also a high-elf
    Tempest fire mage)? Nothing links them.
15. Are Thoren Ashguard and Bram Ironvow, "the Unbreached" (both dwarf Bulwark defenders) connected?
16. Is "The Unbroken Blade" a person or a weapon? What is Hroth's "Red Harvest"?
17. Are ogres and trolls peoples or beasts? They are typed Beast (Hired Ogre, Cave Troll), but "Hired" implies
    someone who takes pay.
18. Are spirits (Arcane Wisp, Spark Imp) a form of Magic, of life released into the world, or something else?
19. The great threat that could unite the races, and the ancient escalations: what were they?
20. What are the in-world names of the races themselves? (Race is never part of a card's name, and invented
    race-flavored names are allowed, memory `world-and-races.md`.)
21. Who are the Archmage and the Warlord going to become? (Set1: "Both get named and reworked later.")
22. A lore word for tokens (summons, conjurings, reinforcements). (Set1, Open questions.)

### Inconsistencies noticed
- **Inquisitors' discipline:** World.md lists inquisitors as **Martial** anti-magic cards ("the Witch Hunter,
  inquisitors"), while the memory note `world-and-races.md` gives "Inquisitors -> Magic" as an example of a role
  leaning a discipline. They disagree; no Inquisitor card exists.
- **"Factions":** World.md rules out faction vs faction, but the Rules pillar says the stigma around Magic is
  "held by characters and factions". Probably groups within peoples rather than a faction system, but unstated.
- **Champion health:** 30 in Rules v0.33 and CardList; 20 in Set1, the archived rules and `ChampionData.health`'s
  default; the engine uses `Rules.PlaytestHealth` = 30 (`Core/State.cs`). Not lore, but a reader of older docs sees both.
- **Stale documents:** `README.md` still links rules v0.17 and describes 20-card decks, Vanguard and Rear rows and
  the two prototype decks; CardList's header says "Rules v0.30"; World.md's open question still mentions "the
  board rows", which became lanes in v0.23. World.md calls the four specs "Tempest, Binders, Bulwark, Reavers",
  which still matches.
- **"Bulwark" means two things across versions:** the Bulwark spec, and (in Set1 and older rules) a keyword now
  called Intercept. Commit `7d94080` still says Hold the Line gives "Bulwark".
- **Banking's lore** ("inner reserves", Martial) was removed from World.md when Stalwart replaced it, but Set1 still
  lists Banking as Thoren's Level 2 mechanic (Set1 is a design record of that time).
- **Placeholder vs named:** Champions are "named characters" (CANON), but every name is a placeholder (World,
  Rules). Both are true at once; the names just aren't final.
- **Arcane Wisp** carries "Arcane" in its name and the Spirit race, yet it is a Neutral non-Caster usable by Martial
  Champions. Ember Drake is likewise a Neutral fire creature. Not contradictory, but unexplained.
- **The Cinder token** appears in Set1 as a Spirit left by Cinder Zealot; the card no longer makes it (Rules,
  CardList), so Set1's token table is outdated.
- **Archived prototype perk:** Set1 says the Warlord's perk was "Vanguard units +1 attack"; Enums'
  `ChampionPerk.UnitsAttackPlusOne` says "Your units get +1 attack" (rows are gone). Mechanical only.
