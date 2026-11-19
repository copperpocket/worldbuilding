# Lore Inbox

New lore captured by `/handoff` from any project, waiting for `/lore-review`. Entries are appended below; do not edit them by hand unless you want to.

### 2026-11-16 — still-blade
- **still-blade's playable world is five provinces of one human kingdom plus the unclaimed wilds behind them.** The capital's province, the misty province, an "upriver" province inland along the great river, a fourth province where those two branches meet, and a frontier province facing the wilds. No other kingdom is visited (possible DLC). The user leaned between 4 and 5 provinces; the sketch uses 5.
  - Status: DRAFT (count and sizes not final)
  - Source: still-blade `docs/design/world-layout.md`; sketch https://claude.ai/artifact/Co4v2uxUDh7Zyk6J75Lvxb
  - Conflicts: `locations.md` ("The game's playable world is the capital's province, the nearby province and the wilds") and `projects.md` (still-blade section) say only two provinces.
- **Province borders follow natural barriers:** the old forest between the capital's province and the misty province, low hills between the capital's province and the upriver province (the great river cuts a gorge through them), a marsh between the misty province and province 4, a tributary between the upriver province and province 4, a ridge before the frontier. Sketch orientation: sea to the south, the mountain range to the east.
  - Status: PLACEHOLDER (a first sketch; positions and barriers are proposals)
  - Source: still-blade `docs/design/world-layout.md`, the sketch
  - Conflicts: none known
- **The Warden's march:** a single Warden commands the whole chain of forts and watchtowers along the kingdom's edge with the wilds, across province lines, and patrols it with their soldiers. The provinces keep their own land; the march is a military duty strung across them. Its honour and its curse is that the patrol never ends. Fits the existing Warden rank ("a border region and its forts").
  - Status: DRAFT (the user liked it; not decided)
  - Source: still-blade `docs/design/world-layout.md` (section 5, as a layout note), the sketch
  - Conflicts: none; extends `human-kingdoms.md`, Military
- **The frontier province is the kingdom's newest claim,** still being pushed out into the wilds, so its edge shifts; forts more than farms. Other provinces also touch the wilds, but the frontier is mostly border.
  - Status: DRAFT
  - Source: the sketch
  - Conflicts: none known
- **The wild edge is a natural wall** (cliffs, deep forest, sinking marsh) watched from towers; the only road into the wilds runs through the frontier's last fort.
  - Status: DRAFT (a game-layout choice with a lore reading)
  - Source: still-blade `docs/design/world-layout.md`, the sketch
  - Conflicts: none known

### 2026-11-17 — still-blade
- **The planet is Earth-sized.** The user decided "Earth size is fine" when setting the game's scale.
  - Status: CANON
  - Source: still-blade `docs/design/world-layout.md` (section 1)
  - Conflicts: `overview.md` says the planet is "larger than average".
- **still-blade's playable world is one province at real scale (the capital's province), plus the wilds beyond it.** It's about 150 km from the coast to the wild border, about 15,000 km² (sketch figures), with roughly 1,500 villages and hamlets. It's made of exactly five counties, all of which the game shows. This replaces the five-province items from 2026-11-16 above.
  - Status: CANON (one province, five counties); DRAFT (sizes)
  - Source: still-blade `docs/design/world-layout.md`; `docs/design/province-scale-sketch.html`
  - Conflicts: `locations.md` lists the playable world as the capital's province, the nearby province and the wilds; the nearby (misty) province is now off the map. The 2026-11-16 inbox items about five provinces are superseded.
- **The five counties (placeholder names), each ruled by a Count or Countess:**
  - the capital's county: the capital, the chief port and the intro town;
  - the forest county, toward the old forest;
  - the hill county, up the great river through the low hills;
  - the seat county: the Duke's or Duchess's seat city, inland on the river;
  - the March county, the border country with the only gate into the wilds.
  - Status: DRAFT (layout); PLACEHOLDER (names)
  - Source: still-blade `docs/design/world-layout.md`, `province-scale-sketch.html`
  - Conflicts: none; uses the "county" rank kept in reserve in `human-kingdoms.md`.
- **The capital's province reaches the wilds.** It follows the great river from its mouth up to the wild border. The coast and lower valley are the heartland; the upper counties are border country.
  - Status: CANON (user: reasonable now that provinces are this large)
  - Source: still-blade `docs/design/world-layout.md` (section 2)
  - Conflicts: `locations.md` calls this province the sheltered heartland and puts the wilds inland, beyond the provinces.
- **"The wilds" is any land that isn't settled:** beyond the kingdom, possibly between provinces, and even pockets inside a province.
  - Status: DRAFT ("one could argue")
  - Source: still-blade `docs/design/world-layout.md` (section 2)
  - Conflicts: none known
- **Population:** the capital's county is the most densely populated land in the province, because of the capital and the royal family's residence there. The seat county is second. The other counties have no city, only a county town, towns and villages.
  - Status: DRAFT
  - Source: still-blade `docs/design/world-layout.md` (section 5)
  - Conflicts: none; consistent with one city per province (two in the capital's).
- **Three tiers of road:** kingdom roads, maintained by the crown, run from the capital out to the neighbouring counties and beyond. Lesser roads aren't maintained by the crown. Paths and tracks are the third tier.
  - Status: CANON
  - Source: still-blade `docs/design/world-layout.md` (section 6)
  - Conflicts: none known
- **New characters leave the threshold at level 2,** and their first quest leads to a trainer to learn their first skill.
  - Status: CANON
  - Source: still-blade `docs/design/world-layout.md` (section 3)
  - Conflicts: `locations.md` says the player quests around the intro town "from about level 3 to 10".

### 2026-11-17 — still-blade
- **The forest and hill counties, first layouts:** the forest county (west branch) has a county town, a crossroads town where the road from the capital forks, a north road town, a fort on the misty road and a fort on the seat road; the old forest walls its west side and the outer wilds its north. The hill county (east branch) has a county town, a river town by the gorge, an east hill town, a seat road fort and a fort facing the unsettled foothills; the great river runs up its west side with the kingdom road beside it.
  - Status: DRAFT (layout, agreed for the game build); PLACEHOLDER (every name)
  - Source: still-blade `docs/design/branch-counties-sketch.html`, `ForestCountyBuilder.cs`, `HillCountyBuilder.cs`
  - Conflicts: none known
- **The forest county reaches the coast** along its south edge.
  - Status: DRAFT (user accepted the proposal)
  - Source: still-blade `docs/design/branch-counties-sketch.html`
  - Conflicts: none known; `locations.md` doesn't place the old forest's coast.

### 2026-11-18 — still-blade
- **The seat county, first layout:** where the forest and hill branches rejoin. The walled seat city (the province's second-largest settlement, with the seat's keep and a big market on its plaza) stands on the great river near the east side, a few minutes up the road from the hill county's gate; four towns (on the west road, midway, the south vale, upriver), three forts (the marsh in the west, a north watch, the March road), villages and hamlets. A marsh on the west side, the March county beyond the north edge (its road closed for now), a ridge to the south against the capital's county with no way through.
  - Status: DRAFT (layout, agreed for the game build as a first pass); PLACEHOLDER (every name)
  - Source: still-blade `docs/design/seat-county-sketch.html`, `SeatCountyBuilder.cs`
  - Conflicts: none known
- **The March county, first layout:** border country, a wide, shallow strip under the wild wall (cliffs and dense woods along its north and west edges), with the unsettled foothills to the east and the seat county to the south. Sparsely settled: a county town just inside the road from the seat city, a town in the eastern foothills, a town on the western moor, a few villages and hamlets on poor farmland. Three forts stand on the wall (an east watch, a west watch, and the last fort, whose gate is the only way into the wilds), with watchtowers between them and a road along the inside of the wall linking them all. Moors, a fen under the west wall, pine slopes and scree in the foothills. The great river doesn't reach it. Who garrisons the wall is left open (see the Warden's march entry above).
  - Status: DRAFT (layout, agreed for the game build as a first pass); PLACEHOLDER (every name)
  - Source: still-blade `docs/design/march-county-sketch.html`, `MarchCountyBuilder.cs`
  - Conflicts: none known
