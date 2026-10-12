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
| boss | Lady Butterfly (c5090), both phases, in the Hirata main hall | sekiro-rs | Yama | 2026-10-12 |
| boss | Gyoubu Oniwa (c5080) on the castle gate | sekiro-rs | Yama | 2026-10-12 |
| boss | Folding Screen Monkeys (c1260), four monkeys with the screen illusions | sekiro-rs | Yama | 2026-10-12 |
| boss | Guardian Ape (c5100), both phases, in the watering hole | sekiro-rs | Yama | 2026-10-12 |
| boss | Headless Ape (c5100, c5001), both apes, in the burrow | sekiro-rs | Yama | 2026-10-12 |
| boss | Corrupted Monk ghost (c5000) on the Mibu bridge | sekiro-rs | Yama | 2026-10-12 |
| boss | True Corrupted Monk (c5000, c5005), all three phases, on the Fountainhead bridge | sekiro-rs | Yama | 2026-10-12 |
| boss | Emma, the Gentle Blade (c7400) in the Shura ending | sekiro-rs | Yama | 2026-10-12 |
| boss | Isshin Ashina (c5430) in the Shura ending | sekiro-rs | Yama | 2026-10-12 |
| boss | Demon of Hatred (c7020), all three phases | sekiro-rs | Yama | 2026-10-12 |
| boss | Great Shinobi Owl, Father (c5060, c5070), both phases, in the Hirata Estate | sekiro-rs | Yama | 2026-10-12 |
| boss | Divine Dragon and the Old Dragons (c5200, c5300, c5310, c5320), both phases | sekiro-rs | Yama | 2026-10-12 |
| boss | Isshin, the Sword Saint (c5400), all four phases including Genichiro, in the silvergrass field | sekiro-rs | Yama | 2026-10-12 |

## Done

<details>
<summary>Done (21)</summary>

| Area | Task | Repo | Who | Date | Commit |
|---|---|---|---|---|---|
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
