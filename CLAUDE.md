# World Bible

The lore shared by all my game projects. `README.md` holds the file list, the workflow and the rules for Claude; read it before changing lore.

## Git
- Commit messages: `type: short summary`, as in `git log`. Stage exact files.
- Commit lore changes once they're done. Ask before pushing.
- `HANDOFF.md` and `.handoff/` are never committed.

## Session hooks
- Pickup: read `overview.md`. Use one line to say how many entries in `lore-inbox.md` and how many answered questions in `open-questions.md` are waiting for `/lore-review`, but don't process them.
- Handoff: make sure every lore change from this session is committed. Anything left undecided goes in `open-questions.md`, not `HANDOFF.md`.
