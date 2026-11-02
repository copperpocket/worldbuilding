# Lore Extract — beautiful-tree

Extracted 2026-10-20 from the working tree at commit `ad18b72` (plus untracked files).

## Summary

**This project has almost no written world-building yet.** It is a Unity action RPG prototype (in the style of WoW) with one test zone, one quest, five abilities, two enemy types and one NPC. All the world content below comes from data asset fields, UI strings and object names. None of it comes from design docs.

**Sources searched:**
- **Docs:** none exist. There is no `CLAUDE.md`, `HANDOFF.md`, README or design doc in the repo. The linked `worldbuilding` folder is empty.
- **Data:** `Assets/_Project/ScriptableObjects/` (abilities, quests), `Prefabs/Characters/`, and the scenes `AlphaIsland.unity` and `SampleScene.unity`.
- **Code:** every `.cs` file under `Assets/_Project/Scripts/` (string literals, enums, comments, tooltips).
- **Art:** file names under `ArtSource/` and `Assets/_Project/`, and the reference images in `ArtSource/Reference/` and `ArtSource/Blender/_Archive/Reference/`. These are plain T-pose base meshes with no costume, faction or setting detail.
- **Other:** `ProjectSettings` (`productName: beautiful-tree`, `companyName: DefaultCompany`) and the git log messages.

**Status key:**
- **CANON:** clearly intended content.
- **DRAFT:** seems intended but is undeveloped.
- **PLACEHOLDER:** likely a temporary name or test content.

---

## Overview & Tone

| Entry | Status | Source |
|---|---|---|
| **Project name "beautiful-tree".** This is the repo and Unity `productName`. Nothing in the content uses it or explains it. | PLACEHOLDER (project codename?) | `ProjectSettings/ProjectSettings.asset`, repo name |
| **Genre conventions are taken openly from WoW-style MMOs.** These include `!`/`?` quest markers, a quartermaster quest giver, evade/leash behaviour on enemies, the global cooldown, the power types Mana/Energy/Rage/Focus, and a level cap of 60. Code comments name WoW directly ("like WoW", "WoW-style evade"). | DRAFT (mechanical, not in-world) | `Scripts/Abilities/DamageAbility.cs:56`, `Scripts/World/EnemyAI.cs:279`, `Scripts/Quests/QuestMarker.cs`, `Scripts/Stats/PlayerStats.cs:39` |
| **Tone from the only NPC dialogue: dry and gruff, like a drill sergeant.** "Those dummies won't break themselves." "Not bad. You might survive out there after all." The second line hints at a dangerous world "out there" beyond the training area. | DRAFT | `ScriptableObjects/Quests/QD_TrainingDay.asset` |
| **Visual palette for magic:** fire is orange (`1, 0.55, 0.15`), frost is light blue, healing is green, and melee is red-brown. The level-up text uses "softer, pastel" colours. | DRAFT (art direction only) | `ScriptableObjects/Abilities/*.asset` (`iconTint`), `Scripts/UI/CombatTextSpawner.cs` tooltip |

## History/Timeline

Nothing found. No dates, eras, events or backstory appear anywhere in the project.

## Factions

Nothing found. There are no faction names, reputations or allegiances. Enemies and NPCs have no affiliation field.

## Characters

| Entry | Status | Source | Notes |
|---|---|---|---|
| **Quartermaster.** The only NPC and the quest giver. Their lines are "I have nothing more for you." and "Come back when you've finished "<quest>"." In the dialog window: "You haven't finished yet. Come back when it's done." | DRAFT | `Scripts/Quests/QuestGiver.cs:13,76,81`, `Scripts/Quests/QuestDialogUI.cs:72`, `Scenes/AlphaIsland/AlphaIsland.unity` (object `NPC_Quartermaster`, `npcName: Quartermaster`) | "Quartermaster" is a job title, not a personal name. No faction, appearance or backstory. The word implies a military or garrison setting (see Open Questions). |
| **The Player.** Starts at level 1 with 100 health and 100 Mana, and gains +10 Health and +5 power per level up to a cap of 60. It is human. The male model is used now, and a female model is in progress. | DRAFT | `AlphaIsland.unity` (Player `PlayerStats`), `ArtSource/Blender/HumanMale_UAL_v04.blend`, untracked `HumanFemale_v01–v09.blend`, `ArtSource/Tripo/HumanFemale.fbx` | No name, class, origin or race lore. |

## Locations

| Entry | Status | Source | Notes |
|---|---|---|---|
| **Alpha Island.** The main (and only real) scene, with terrain, a NavMesh, the Quartermaster, a Training Dummy spawner and a Wolf spawner. | PLACEHOLDER | `Scenes/AlphaIsland/AlphaIsland.unity`, `Art/Terrain/TD_AlphaIsland.asset` | "Alpha" reads like a milestone label (alpha build), not an in-world name. Being an island may or may not be intended. |
| **SampleScene.** A Unity default test scene with a cube, camera and HUD only. | PLACEHOLDER | `Scenes/SampleScene.unity` | |
| **"Out there."** The Quartermaster refers to somewhere dangerous beyond the training area. | DRAFT (implied only) | `QD_TrainingDay.asset` (`completionText`) | No location is named. |

Terrain layers are unnamed (`NewLayer`, `NewLayer 1–3.terrainlayer`), so they say nothing about the setting.

## Magic/Systems (in-world explanation)

There is no in-world explanation for any system. The entries below are what the data implies.

| Entry | Status | Source | Notes |
|---|---|---|---|
| **Fireball.** "Hurl a slow but heavy ball of flame." 2 s cast, 25 power, 35 damage, range 30. | CANON (as game content) | `ScriptableObjects/Abilities/AB_Fireball.asset`, `Scripts/Editor/HudBuilder.cs:180` | |
| **Frost Bolt.** "A fast shard of ice. Can be cast on the move." Instant cast, 12 power, 6 s cooldown, 14 damage. | CANON (as game content) | `AB_Frostbolt.asset`, `HudBuilder.cs:193` | **Inconsistent spelling:** the display name is "Frost Bolt", but the asset is `AB_Frostbolt` and the prefabs are `PF_Frostbolt`/`PF_FrostImpact`. |
| **Mend.** "Restore your own health. Cannot be cast while moving." 1.5 s cast, heals 35. | CANON (as game content) | `AB_Mend.asset`, `HudBuilder.cs:205` | It is self-only, and its source of power (divine, nature or arcane) is not stated. |
| **Strike.** "A quick melee blow." 18 damage and starts auto-attack. | CANON (as game content) | `AB_Strike.asset` | |
| **Auto Attack.** "Toggle melee swings against your target." | CANON (as game content) | `AB_AutoAttack.asset` | |
| **Power types: Mana, Energy, Rage, Focus.** Rage starts empty and builds from swinging. Mana and Focus regenerate. The player uses Mana. | DRAFT | `Scripts/Stats/PowerType.cs`, `Scripts/Combat/PlayerCombat.cs:145`, `Scripts/Combat/PlayerCombatTracker.cs:93` | These imply multiple classes, but no class is defined. |
| **Classes.** Code comments say "Every class has this" (auto-attack) and "Rage classes build power by swinging." | DRAFT (implied only) | `Scripts/Abilities/AutoAttackAbility.cs:4`, `PlayerCombat.cs:145` | No class names exist. **Inconsistency:** the one player character has both melee (Strike) and spells (Fireball, Frost Bolt, Mend) on one Mana bar, so it fits no single class. |
| **Death and respawn.** "You are dead". The player respawns at a spawn point, and enemies respawn after 10 s. | DRAFT (mechanical) | `Scripts/Abilities/Ability.cs:61`, `Scripts/Player/Respawn.cs`, `Scripts/World/EnemySpawner.cs` | There is no in-world reason for resurrection. |
| **Evade.** An enemy pulled too far from home (30 m leash) returns home fully healed and immune to damage. | DRAFT (mechanical) | `Scripts/World/EnemyAI.cs:16,279`, `Scripts/Combat/Health.cs:48` | |

## Creatures

| Entry | Status | Source | Notes |
|---|---|---|---|
| **Wolf.** Level 1, 50 HP, 25 XP. It bites, has walk, gallop and idle animations, plays a hit flinch, dies on its side, and its corpse lasts 5 s. | DRAFT | `Prefabs/Characters/Wolf.prefab`, `ArtSource/Blender/Wolf_anim_v08.blend`, `Scripts/Editor/WolfAssetBuilder.cs`, git log (`1899407`, `610e6e3`) | It is an ordinary animal with no special or corrupted variant. It is the first real enemy. |
| **Training Dummy.** Level 1, 50 HP, 25 XP. It is a target object (it tips over on death), and it is the target of the only quest. | PLACEHOLDER / tutorial content | `Prefabs/Characters/Dummy.prefab`, `Scripts/Combat/Health.cs:11` (default `displayName`) | **Inconsistent:** the prefab is named `Dummy`, but its display name is "Training Dummy". It is also the hard-coded default name for every `Health` component. |

## Items & Artifacts

Nothing found. There is no inventory, loot, item, equipment or currency data. The only reward in the game is XP (100 for the quest, 25 per kill).

## Quests (supporting section)

| Entry | Status | Source | Notes |
|---|---|---|---|
| **Training Day.** "Those dummies won't break themselves. Destroy five of them." Objective: Training Dummy ×5, level 1 required, 100 XP reward. On completion: "Not bad. You might survive out there after all." | DRAFT (tutorial) | `ScriptableObjects/Quests/QD_TrainingDay.asset`; also hard-coded preview text in `Scripts/Editor/QuestUIBuilder.cs:41,84` and `QuestLogBuilder.cs:64` | `questId` is empty. The quest giver is not linked in the quest data; it is set on the NPC. |
| UI preview strings: "Quest description goes here.", "Quest description.", "QD_NewQuest" | PLACEHOLDER | `QuestUIBuilder.cs:45`, `QuestLogBuilder.cs:67`, `Scripts/Quests/QuestDefinition.cs` | |

## Glossary

| Term | Meaning (as used) | Status | Source |
|---|---|---|---|
| Alpha Island | The test zone | PLACEHOLDER | `Scenes/AlphaIsland/` |
| Quartermaster | Quest-giver NPC | DRAFT | `QuestGiver.cs` |
| Training Dummy | Practice target / tutorial enemy | PLACEHOLDER | `Dummy.prefab` |
| Mend | Self-heal spell | CANON | `AB_Mend.asset` |
| Fireball / Frost Bolt | Fire and frost projectile spells | CANON | `AB_Fireball.asset`, `AB_Frostbolt.asset` |
| Strike | Melee ability | CANON | `AB_Strike.asset` |
| Mana / Energy / Rage / Focus | Power resources | DRAFT | `PowerType.cs` |
| Evade | Enemy resets to its home point | DRAFT | `EnemyAI.cs` |

## Open Questions

1. **What does "beautiful-tree" mean?** Is it a working title, or does a tree feature in the world?
2. **Is "Alpha Island" a real place name** or a build label? Is the starting area really an island?
3. **Who does the Quartermaster serve?** The title implies a garrison, army or camp. What is the organisation, and why is the player being trained?
4. **What is "out there"** in "You might survive out there after all"? What is the threat beyond the training grounds?
5. **What classes exist?** The code expects classes that use Rage, Energy and Focus, but none are defined. Is the current mixed melee-and-caster kit a test setup or a hybrid class?
6. **Where does magic come from?** Fire, frost and healing exist with no source or explanation.
7. **Why do the dead come back?** The player and enemies respawn; is there an in-world reason, or is it purely a game mechanic?
8. **Is the player always human?** Male and female human models exist. Are there other races?
9. **Are wolves just wildlife,** or tied to some larger threat?
10. **Why level 60?** Is the cap intended, or a default copied from the genre?
