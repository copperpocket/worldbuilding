# World Bible

The single source of truth for the world shared by all of my game projects. The long-term goal is a complete, polished RPG set in this world; smaller games are built along the way to develop the world and build an audience.

Game projects do not store lore. They point here.

## Projects using this world

| Project | Repo | Role |
|---|---|---|
| beautiful-tree | `beautiful-tree` | RPG framework prototype (Unity): movement, combat, abilities, quests |
| Magic vs Martial | `magic-vs-martial` (TCG) | Trading card game; the most developed lore so far |
| (third project) | TBD | New smaller game |

See `projects.md` for how each one uses the world.

## Status key

Every lore entry carries one of these:

- **CANON**: I decided it. Treat as true.
- **DRAFT**: intended or leaning, but not settled. Can change.
- **PLACEHOLDER**: a temporary name or test content.

**Naming rule (CANON):** every proper name in the world (characters, places, specs, abilities, the words "Magic", "Martial" and "Command") is a PLACEHOLDER as a name unless an entry says the name itself is final. A concept can be CANON while its name is still a placeholder.

## Files

| File | Contents |
|---|---|
| `overview.md` | The essentials: tone, pillars, core theme. Read at the start of every session |
| `peoples.md` | The races |
| `magic-and-martial.md` | The two energies and the in-world reasons behind mechanics |
| `specializations.md` | Specs: how they're earned, the four specs, Hybrids |
| `characters.md` | Champions, Legendaries, NPCs, role archetypes |
| `creatures.md` | Beasts, spirits, constructs, dragons |
| `locations.md` | Places (very few named yet) |
| `history.md` | The past (very little yet) |
| `items.md` | Gear, artifacts, objects |
| `glossary.md` | Terms across all projects |
| `projects.md` | How each game uses the world |
| `open-questions.md` | Unanswered questions and conflicts, with answer lines |
| `lore-inbox.md` | New lore captured by `/handoff`, waiting for review |
| `sources/` | Original extracts, kept unchanged. Do not edit |

## Workflow

1. During work on any project, `/handoff` appends new lore to `lore-inbox.md`.
2. I answer questions by writing under the **Answer:** lines in `open-questions.md`.
3. In a session in this repo, `/lore-review` moves answered questions and inbox items into the right files.

## Rules for Claude

- Never invent lore or fill gaps. Unknowns go in `open-questions.md`.
- Never promote DRAFT to CANON unless I clearly decide it.
- Contradictions are never resolved silently: add them to `open-questions.md` for me to rule on.
- Keep entries short and cite the source project when it helps.
- Never edit files in `sources/`.
- Keep `overview.md` short; it is loaded every session.
