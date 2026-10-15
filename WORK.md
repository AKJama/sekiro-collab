# Work

Who's working on what right now, and what's done.
`FEATURES.md` is the full backlog; Open below lists specific tasks someone has broken out but nobody has started yet; either of us can take one.

- One row per specific task you're actually starting (one arena, one boss, one screen), not a whole area.
- Before starting, add the row to Claimed with your name and the date, then commit and push straight away.
- When it's done, move the row to Done with the commit as a short link: `[abc1234](https://github.com/<owner>/<repo>/commit/<sha>)`.
- Anything not in Claimed is open to either of us.
- Pull before you edit; `main` is protected, so a push that's behind is rejected rather than overwriting.
- Tip: add one line to your own repo's `AGENTS.md` (or `CLAUDE.md`) pointing here, so every new session checks this board.

## Open

| Area | Task |
|---|---|
| world | Boss arena: Ashina Castle castle top, the arena's snow, lightning and dense-fog effects |
| rendering | Scene brightness calibrated against a real-game screenshot of the castle rooftop |
| ui | Debug text off by default |
| boss | Divine Dragon: the authored grapple targets, so lightning charging and reversal work |
| boss | Folding Screen Monkeys: darkness, hearing history, roof navigation, footprints, natural victory |
| boss | Lady Butterfly: illusion homing, navigation and summon recreation; two illusions fall below the floor |
| boss | Guardian Ape: grabs do not connect |
| combat | TAE 705 facing correction for enemies (20 Demon of Hatred events use it) |

## Claimed

| Area | Task | Repo | Who | Since |
|---|---|---|---|---|
| combat | Hit-shape reach and first-hit frames checked against real-game clips: Wolf's swings, Ichimonji, Mortal Draw, regular enemies | RustSekiro | FwLo | 2026-10-12 |
| combat | Hit-shape priority, knockback facing, armoured enemies' damage cut | RustSekiro | FwLo | 2026-10-12 |
| cloth | Wolf's cape against a real-game clip, coat detail texture layer | RustSekiro | FwLo | 2026-10-12 |
| camera | Lock-on camera offsets, target smoothing, look limits, lock-on switch | RustSekiro | FwLo | 2026-10-12 |
| rendering | The game's tone curve and auto exposure, night snow brightness, light probe blend between hours | RustSekiro | FwLo | 2026-10-12 |
| rendering | Layered map materials: each layer's own mask, UV sets, blend data | RustSekiro | FwLo | 2026-10-12 |
| effects | Hand-made effects moved to the game's FXR files: deflect, guard sparks, hit blood, floor dust, blood decals, lit particles | RustSekiro | FwLo | 2026-10-12 |
| effects | Regular enemies' attack effects from their TAE events, checked per enemy | RustSekiro | FwLo | 2026-10-12 |
| ui | HUD art: stealth meter, deathblow mark | RustSekiro | FwLo | 2026-10-12 |
| audio | Remaining mixer events and sound occlusion | RustSekiro | FwLo | 2026-10-12 |
| enemies | Regular enemies: AI pacing against a recorded fight, armoured servant's armour part | RustSekiro | FwLo | 2026-10-12 |
| stealth | Shadow hiding, forced crouch, patrol routes | RustSekiro | FwLo | 2026-10-12 |
| rendering | Single-sample TAA at native resolution, to prove our motion vectors, depth and jitter before DLSS or FSR (see docs/UPSCALING.md) | sekiro-rs | Yama | 2026-10-13 |
| rendering | Map lights applied from the game data: lanterns, fires and braziers (BTL), all four light-set lights, probe installed once (visual parity L1, E1) | sekiro-rs | Yama | 2026-10-15 |

## Done

<details>
<summary>Done (52)</summary>

| Area | Task | Repo | Who | Date | Commit |
|---|---|---|---|---|---|
| rendering | Shared fix: GI volume lookup per pixel scans every volume (Hirata 142); filter spatially | sekiro-rs | Yama | 2026-10-14 | [7b36fc6](https://github.com/AKJama/sekiro-rs/commit/7b36fc6) |
| rendering | Shared fix: sky dome mapping overwritten by cloud models | sekiro-rs | Yama | 2026-10-14 | [7b36fc6](https://github.com/AKJama/sekiro-rs/commit/7b36fc6) |
| tools | Shared fix: captures wait for finished pipelines; --uncapped partly (sustained rate still open) | sekiro-rs | Yama | 2026-10-14 | [7b36fc6](https://github.com/AKJama/sekiro-rs/commit/7b36fc6) |
| world | Ashina Outskirts and Castle: grass and weed clumps from the game's grass data (visual parity G1) | sekiro-rs | Yama | 2026-10-15 | [7b36fc6](https://github.com/AKJama/sekiro-rs/commit/7b36fc6) |
| world | Visual parity, Ashina Outskirts and Castle: camera matched to real-game shots, every difference sorted by cause | sekiro-rs | Yama | 2026-10-15 | [8a09abf](https://github.com/AKJama/sekiro-rs/commit/8a09abf) |
| rendering | Shared fix resumed: fog switched off by a wrong-name lookup; fog banks use the sun; sky continuation | sekiro-rs | Yama | 2026-10-15 | [8a09abf](https://github.com/AKJama/sekiro-rs/commit/8a09abf) |
| world | Map test gates (fast data checks over all maps, a few render views per area) and the Ashina Outskirts regression | sekiro-rs | Yama | 2026-10-14 | [d229d6c](https://github.com/AKJama/sekiro-rs/commit/d229d6c) |
| tools | Real-game reference screenshots of Ashina Outskirts and Castle indexed by position (tool only; the images stay local) | sekiro-rs | Yama | 2026-10-14 | [d229d6c](https://github.com/AKJama/sekiro-rs/commit/d229d6c) |
| world | Map completeness research: how map blocks connect, draw groups and detail levels, from Smithbox, DSMapStudio, SoulsFormats and RustSekiro | sekiro-rs | Yama | 2026-10-14 | [d76523f](https://github.com/AKJama/sekiro-rs/commit/d76523f) |
| world | Automated hole sweep for one map area (Ashina Castle first): holes, void below the horizon, pop-in | sekiro-rs | Yama | 2026-10-14 | [d76523f](https://github.com/AKJama/sekiro-rs/commit/d76523f) |
| ui | Menu: Explore map option first, no hour row (story state from the data) | sekiro-rs | Yama | 2026-10-14 | [d76523f](https://github.com/AKJama/sekiro-rs/commit/d76523f) |
| world | Castle top snow during the Genichiro fight checked against the game data | sekiro-rs | Yama | 2026-10-14 | [d76523f](https://github.com/AKJama/sekiro-rs/commit/d76523f) |
| tools | Game data found from the cache folder at runtime, not the build folder | sekiro-rs | Yama | 2026-10-14 | [d76523f](https://github.com/AKJama/sekiro-rs/commit/d76523f) |
| world | Map layout reader keeps every visibility, loading and connection field (map completeness job A) | sekiro-rs | Yama | 2026-10-14 | [d76523f](https://github.com/AKJama/sekiro-rs/commit/d76523f) |
| world | Missing map textures, grey stand-ins and missing object models accounted for (map completeness job G) | sekiro-rs | Yama | 2026-10-14 | [d76523f](https://github.com/AKJama/sekiro-rs/commit/d76523f) |
| world | Map streaming, detail level and visibility rules from the exe (map completeness research) | sekiro-rs | Yama | 2026-10-14 | [d76523f](https://github.com/AKJama/sekiro-rs/commit/d76523f) |
| world | Exported map layout keeps every part, connection and the reason anything is not drawn (map completeness job B) | sekiro-rs | Yama | 2026-10-14 | [d76523f](https://github.com/AKJama/sekiro-rs/commit/d76523f) |
| world | Ashina Outskirts and Castle: story state at the first visit from the event scripts (map completeness job C) | sekiro-rs | Yama | 2026-10-14 | [d76523f](https://github.com/AKJama/sekiro-rs/commit/d76523f) |
| world | Ashina Outskirts and Castle: neighbouring map blocks loaded, map objects on (map completeness job D) | sekiro-rs | Yama | 2026-10-14 | [d76523f](https://github.com/AKJama/sekiro-rs/commit/d76523f) |
| world | Ashina Outskirts and Castle: one visibility decision per map part, by the exe's rules (map completeness job E) | sekiro-rs | Yama | 2026-10-14 | [d76523f](https://github.com/AKJama/sekiro-rs/commit/d76523f) |
| world | Ashina Outskirts and Castle: every detail level exported and picked by distance (map completeness job F) | sekiro-rs | Yama | 2026-10-14 | [d76523f](https://github.com/AKJama/sekiro-rs/commit/d76523f) |
| world | Ashina Outskirts and Castle: ground fog and cloud surfaces below the cliffs (map completeness) | sekiro-rs | Yama | 2026-10-14 | [d76523f](https://github.com/AKJama/sekiro-rs/commit/d76523f) |
| rendering | Map lighting check and fix, Hirata Estate (m10_00): every story state against the game data, real frame time | sekiro-rs | Yama | 2026-10-13 | [24bc46d](https://github.com/AKJama/sekiro-rs/commit/24bc46d) |
| rendering | Map lighting check and fix, Ashina Outskirts (m11_00): every story state against the game data, real frame time | sekiro-rs | Yama | 2026-10-13 | [24bc46d](https://github.com/AKJama/sekiro-rs/commit/24bc46d) |
| rendering | Map lighting check and fix, Ashina Castle (m11_01): every story state against the game data, real frame time | sekiro-rs | Yama | 2026-10-13 | [24bc46d](https://github.com/AKJama/sekiro-rs/commit/24bc46d) |
| rendering | Map lighting check and fix, Ashina Reservoir (m11_02): every story state against the game data, real frame time | sekiro-rs | Yama | 2026-10-13 | [24bc46d](https://github.com/AKJama/sekiro-rs/commit/24bc46d) |
| rendering | Map lighting check and fix, Abandoned Dungeon (m13_00): every story state against the game data, real frame time | sekiro-rs | Yama | 2026-10-13 | [24bc46d](https://github.com/AKJama/sekiro-rs/commit/24bc46d) |
| rendering | Map lighting check and fix, Ashina Depths (m15_00): every story state against the game data, real frame time | sekiro-rs | Yama | 2026-10-13 | [24bc46d](https://github.com/AKJama/sekiro-rs/commit/24bc46d) |
| rendering | Map lighting check and fix, Sunken Valley (m17_00): every story state against the game data, real frame time | sekiro-rs | Yama | 2026-10-13 | [24bc46d](https://github.com/AKJama/sekiro-rs/commit/24bc46d) |
| rendering | Map lighting check and fix, Senpou Temple (m20_00): every story state against the game data, real frame time | sekiro-rs | Yama | 2026-10-13 | [24bc46d](https://github.com/AKJama/sekiro-rs/commit/24bc46d) |
| rendering | Map lighting check and fix, Fountainhead Palace (m25_00): every story state against the game data, real frame time | sekiro-rs | Yama | 2026-10-13 | [24bc46d](https://github.com/AKJama/sekiro-rs/commit/24bc46d) |
| rendering | Map material layers (multi-material ground, masks, tint, detail normals, wetness, snow), adapted from RustSekiro | sekiro-rs | Yama | 2026-10-13 | [24bc46d](https://github.com/AKJama/sekiro-rs/commit/24bc46d) |
| performance | GPU frame-time regression: camera fade only on fading materials; material cache, decal and FX hold leaks; Tomoe storm resets on restart | sekiro-rs | Yama | 2026-10-13 | [f99e8b7](https://github.com/AKJama/sekiro-rs/commit/f99e8b7) |
| rendering | Story lighting per map selected from the game data: time-of-day flags, area gparam sub-ids from map events, collision-part light, fog and env-map ids (selection only; tone curve and exposure stay with RustSekiro) | sekiro-rs | Yama | 2026-10-13 | [f99e8b7](https://github.com/AKJama/sekiro-rs/commit/f99e8b7) |
| brain | Move sheet as a gate: attacks only when reach and first-hit time fit, fastest break punish, idle penalties | sekiro-rs | Yama | 2026-10-13 | [f99e8b7](https://github.com/AKJama/sekiro-rs/commit/f99e8b7) |
| brain | Wolf wins against multi-phase bosses not recorded in the brain memory (Genichiro win around fight 18 counted as 0) | sekiro-rs | Yama | 2026-10-13 | [f99e8b7](https://github.com/AKJama/sekiro-rs/commit/f99e8b7) |
| combat | Deathblow near an edge pushes Wolf through doors or off the castle tower, out of the arena | sekiro-rs | Yama | 2026-10-13 | [f99e8b7](https://github.com/AKJama/sekiro-rs/commit/f99e8b7) |
| brain | Break punish: code lists the viable punishes (lands before the stun ends, incl. ranged) with their damage and follow-ups; the coach picks | sekiro-rs | Yama | 2026-10-13 | [f99e8b7](https://github.com/AKJama/sekiro-rs/commit/f99e8b7) |
| rendering | Research: what FSR and DLSS (upscaling, frame generation) need from the renderer, what Bevy 0.19 and wgpu 29 offer, and what to start doing now ([docs/UPSCALING.md](https://github.com/AKJama/sekiro-rs/blob/main/docs/UPSCALING.md)) | sekiro-rs | Yama | 2026-10-13 | [56c4f57](https://github.com/AKJama/sekiro-rs/commit/56c4f57) |
| boss | Lady Butterfly (c5090), both phases, in the Hirata main hall: every phase playable in its arena (gaps in that boss's docs/BOSSES-*.md) | sekiro-rs | Yama | 2026-10-12 | [e964560](https://github.com/AKJama/sekiro-rs/commit/e964560) |
| boss | Gyoubu Oniwa (c5080) on the castle gate: every phase playable in its arena (gaps in that boss's docs/BOSSES-*.md) | sekiro-rs | Yama | 2026-10-12 | [e964560](https://github.com/AKJama/sekiro-rs/commit/e964560) |
| boss | Guardian Ape (c5100), both phases, in the watering hole: every phase playable in its arena (gaps in that boss's docs/BOSSES-*.md) | sekiro-rs | Yama | 2026-10-12 | [e964560](https://github.com/AKJama/sekiro-rs/commit/e964560) |
| boss | Headless Ape (c5100, c5001), both apes, in the burrow: every phase playable in its arena (gaps in that boss's docs/BOSSES-*.md) | sekiro-rs | Yama | 2026-10-12 | [e964560](https://github.com/AKJama/sekiro-rs/commit/e964560) |
| boss | Corrupted Monk ghost (c5000) on the Mibu bridge: every phase playable in its arena (gaps in that boss's docs/BOSSES-*.md) | sekiro-rs | Yama | 2026-10-12 | [e964560](https://github.com/AKJama/sekiro-rs/commit/e964560) |
| boss | True Corrupted Monk (c5000, c5005), all three phases, on the Fountainhead bridge: every phase playable in its arena (gaps in that boss's docs/BOSSES-*.md) | sekiro-rs | Yama | 2026-10-12 | [e964560](https://github.com/AKJama/sekiro-rs/commit/e964560) |
| boss | Emma, the Gentle Blade (c7400) in the Shura ending: every phase playable in its arena (gaps in that boss's docs/BOSSES-*.md) | sekiro-rs | Yama | 2026-10-12 | [e964560](https://github.com/AKJama/sekiro-rs/commit/e964560) |
| boss | Isshin Ashina (c5430) in the Shura ending: every phase playable in its arena (gaps in that boss's docs/BOSSES-*.md) | sekiro-rs | Yama | 2026-10-12 | [e964560](https://github.com/AKJama/sekiro-rs/commit/e964560) |
| boss | Demon of Hatred (c7020), all three phases: every phase playable in its arena (gaps in that boss's docs/BOSSES-*.md) | sekiro-rs | Yama | 2026-10-12 | [e964560](https://github.com/AKJama/sekiro-rs/commit/e964560) |
| boss | Great Shinobi Owl, Father (c5060, c5070), both phases, in the Hirata Estate: every phase playable in its arena (gaps in that boss's docs/BOSSES-*.md) | sekiro-rs | Yama | 2026-10-12 | [e964560](https://github.com/AKJama/sekiro-rs/commit/e964560) |
| boss | Isshin, the Sword Saint (c5400), all four phases including Genichiro, in the silvergrass field: every phase playable in its arena (gaps in that boss's docs/BOSSES-*.md) | sekiro-rs | Yama | 2026-10-12 | [e964560](https://github.com/AKJama/sekiro-rs/commit/e964560) |
| combat | A deathblow right after a Mikiri counter now works (Genichiro, Owl, soldier) | sekiro-rs | Yama | 2026-10-12 | [e964560](https://github.com/AKJama/sekiro-rs/commit/e964560) |
| camera | Hanging blinds in the castle-top tower dither out near the camera, from the game's material fade flags | sekiro-rs | Yama | 2026-10-12 | [e964560](https://github.com/AKJama/sekiro-rs/commit/e964560) |
| brain | Every bad outcome counts as failure; per-move bandit every two attacks; moves table, ten-fight digest and coach review mode | sekiro-rs | Yama | 2026-10-12 | [e964560](https://github.com/AKJama/sekiro-rs/commit/e964560) |
| tests | Bug hunt rounds 10-20: finder plus skeptic per area, each confirmed defect fixed with a test that fails without it (combat, deflect, plunges, grapple, respawn and reset, AI queries, status, menus, camera, extractor export) | RustSekiro | FwLo | 2026-10-12 | [265e142](https://github.com/FFwLo/RustSekiro/commit/265e142) |
| rendering | Fog density over GameScale, the game's metering and adaptation, height fog pass, sky domes by story hour, bloom level weights (after sekiro-rs, credited) | RustSekiro | FwLo | 2026-10-12 | [265e142](https://github.com/FFwLo/RustSekiro/commit/265e142) |
| world | Fog walls from common events 20005820 / 20005825, data-driven (after sekiro-rs fogwall.rs, credited) | RustSekiro | FwLo | 2026-10-12 | [265e142](https://github.com/FFwLo/RustSekiro/commit/265e142) |
| world | Boss arena staged (story spot, collision, fog walls, story time, map events): Ashina Castle, Shura ending | sekiro-rs | Yama | 2026-10-12 | [b082d8a](https://github.com/AKJama/sekiro-rs/commit/b082d8a) |
| world | Boss arena staged (story spot, collision, fog walls, story time, map events): Ashina Reservoir, silvergrass field | sekiro-rs | Yama | 2026-10-12 | [b082d8a](https://github.com/AKJama/sekiro-rs/commit/b082d8a) |
| world | Boss arena staged (story spot, collision, fog walls, story time, map events): Ashina Outskirts, castle gate | sekiro-rs | Yama | 2026-10-12 | [b082d8a](https://github.com/AKJama/sekiro-rs/commit/b082d8a) |
| world | Boss arena staged (story spot, collision, fog walls, story time, map events): Ashina Outskirts, Demon of Hatred | sekiro-rs | Yama | 2026-10-12 | [b082d8a](https://github.com/AKJama/sekiro-rs/commit/b082d8a) |
| world | Boss arena staged (story spot, collision, fog walls, story time, map events): Hirata Estate, main hall | sekiro-rs | Yama | 2026-10-12 | [b082d8a](https://github.com/AKJama/sekiro-rs/commit/b082d8a) |
| world | Boss arena staged (story spot, collision, fog walls, story time, map events): Hirata Estate, Owl (Father) | sekiro-rs | Yama | 2026-10-12 | [b082d8a](https://github.com/AKJama/sekiro-rs/commit/b082d8a) |
| world | Boss arena staged (story spot, collision, fog walls, story time, map events): Senpou Temple, illusion screens | sekiro-rs | Yama | 2026-10-12 | [b082d8a](https://github.com/AKJama/sekiro-rs/commit/b082d8a) |
| world | Boss arena staged (story spot, collision, fog walls, story time, map events): Sunken Valley, watering hole | sekiro-rs | Yama | 2026-10-12 | [b082d8a](https://github.com/AKJama/sekiro-rs/commit/b082d8a) |
| world | Boss arena staged (story spot, collision, fog walls, story time, map events): Sunken Valley, ape's burrow | sekiro-rs | Yama | 2026-10-12 | [b082d8a](https://github.com/AKJama/sekiro-rs/commit/b082d8a) |
| world | Boss arena staged (story spot, collision, fog walls, story time, map events): Ashina Depths, Mibu bridge | sekiro-rs | Yama | 2026-10-12 | [b082d8a](https://github.com/AKJama/sekiro-rs/commit/b082d8a) |
| world | Boss arena staged (story spot, collision, fog walls, story time, map events): Fountainhead Palace, bridge | sekiro-rs | Yama | 2026-10-12 | [b082d8a](https://github.com/AKJama/sekiro-rs/commit/b082d8a) |
| world | Boss arena staged (story spot, collision, fog walls, story time, map events): Fountainhead Palace, sanctuary | sekiro-rs | Yama | 2026-10-12 | [b082d8a](https://github.com/AKJama/sekiro-rs/commit/b082d8a) |
| tests | Test audit: one integration binary per crate, slow tier opt-in, full run about 90 s | sekiro-rs | Yama | 2026-10-12 | [6fe0ad5](https://github.com/AKJama/sekiro-rs/commit/6fe0ad5) |
| world | Castle top arena: fog walls from the event script and story time of day for Owl and Genichiro | sekiro-rs | Yama | 2026-10-12 | [5f6dc64](https://github.com/AKJama/sekiro-rs/commit/5f6dc64) |
| cloth | Port RustSekiro's Havok cloth: Wolf, Owl, Genichiro, Tomoe, soldier | sekiro-rs | Yama | 2026-10-12 | [85a8029](https://github.com/AKJama/sekiro-rs/commit/85a8029) |
| effects | Port RustSekiro's FXR player, blood and hit stains for the Owl and Genichiro fights | sekiro-rs | Yama | 2026-10-12 | [85a8029](https://github.com/AKJama/sekiro-rs/commit/85a8029) |
| rendering | Character materials: gloss and metal from the game's textures, fixed hair and fur cut-outs | sekiro-rs | Yama | 2026-10-12 | [85a8029](https://github.com/AKJama/sekiro-rs/commit/85a8029) |
| brain | Local checkpoint chooser so the boss brain needs no API key | sekiro-rs | Yama | 2026-10-12 | [43077c8](https://github.com/AKJama/sekiro-rs/commit/43077c8) |

</details>
