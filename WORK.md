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
| world | Boss arena: Ashina Castle, Shura ending |
| world | Boss arena: Ashina Reservoir, silvergrass field |
| world | Boss arena: Ashina Outskirts, castle gate |
| world | Boss arena: Ashina Outskirts, Demon of Hatred |
| world | Boss arena: Hirata Estate, main hall |
| world | Boss arena: Hirata Estate, Owl (Father) |
| world | Boss arena: Senpou Temple, illusion screens |
| world | Boss arena: Sunken Valley, watering hole |
| world | Boss arena: Sunken Valley, ape's burrow |
| world | Boss arena: Ashina Depths, Mibu bridge |
| world | Boss arena: Fountainhead Palace, bridge |
| world | Boss arena: Fountainhead Palace, sanctuary |

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

## Done

<details>
<summary>Done (6)</summary>

| Area | Task | Repo | Who | Date | Commit |
|---|---|---|---|---|---|
| tests | Test audit: one integration binary per crate, slow tier opt-in, full run about 90 s | sekiro-rs | Yama | 2026-10-12 | [6fe0ad5](https://github.com/AKJama/sekiro-rs/commit/6fe0ad5) |
| world | Castle top arena: fog walls from the event script and story time of day for Owl and Genichiro | sekiro-rs | Yama | 2026-10-12 | [5f6dc64](https://github.com/AKJama/sekiro-rs/commit/5f6dc64) |
| cloth | Port RustSekiro's Havok cloth: Wolf, Owl, Genichiro, Tomoe, soldier | sekiro-rs | Yama | 2026-10-12 | [85a8029](https://github.com/AKJama/sekiro-rs/commit/85a8029) |
| effects | Port RustSekiro's FXR player, blood and hit stains for the Owl and Genichiro fights | sekiro-rs | Yama | 2026-10-12 | [85a8029](https://github.com/AKJama/sekiro-rs/commit/85a8029) |
| rendering | Character materials: gloss and metal from the game's textures, fixed hair and fur cut-outs | sekiro-rs | Yama | 2026-10-12 | [85a8029](https://github.com/AKJama/sekiro-rs/commit/85a8029) |
| brain | Local checkpoint chooser so the boss brain needs no API key | sekiro-rs | Yama | 2026-10-12 | [43077c8](https://github.com/AKJama/sekiro-rs/commit/43077c8) |

</details>
