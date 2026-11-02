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
