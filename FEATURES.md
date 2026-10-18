# Features

What each project has, and what's left to do.
This is the backlog: anything not ✅ is up for grabs, so claim it in `WORK.md` before starting.

- ✅ works and matches the real game, in behaviour and in look (the game's own data and art, not a stand-in).
- 🟡 works but differs from the game, or only part of it is done; say what's missing in the cell.
- ❌ not started.
- ? not checked.

Keep your own column up to date, and be strict: a feature that works but doesn't look or behave like the game is 🟡.

| Area | Feature | sekiro-rs (Yama) | RustSekiro (FwLo, Fireguy32) |
|---|---|---|---|
| Data | Archives, params, animation, TAE, behaviour graphs | ✅ | ✅ |
| Data | Player script | ✅ runs the real HKS bytecode | ✅ ported state machine |
| Data | Enemy Lua AI, EMEVD events | ✅ | ✅ |
| Data | Models and materials | ✅ | ✅ |
| Data | Cloth data | ✅ | ✅ |
| Movement | Walk, run, sprint, steps, jumps, air control, crouch | ✅ | ✅ |
| Movement | Lock-on strafing, kick-jump | ✅ | ✅ |
| Movement | Sheathed walk and run | 🟡 | ✅ |
| Movement | Grappling hook | ✅ arcs, air and chained | ✅ incl. enemy targets |
| Movement | Ledge hang and climb | 🟡 | 🟡 hang, shimmy, outside and inside corners, climb, drop, air catch and ledge deathblows with the game's clips; placement reconstructed, tried on the parkour test map only |
| Movement | Wall hug | ✅ | 🟡 hug, move, peek and hug deathblows with the game's clips; the peek camera is set by eye |
| Movement | Wall jumps | ? | 🟡 off a wall, out of a hug or a hang, once a flight as in the game; chained wall to wall only on the parkour test map |
| Movement | 180 quick turns (standing, walking, running) | ? | 🟡 the game's clips; the walk turns' swing is reconstructed |
| Movement | Swimming and diving | ✅ | 🟡 the game's swim, dive, jump, entry / exit, attack and item clips; no breath, swim deaths, underwater enemies or underwater look; the Construct's pool only |
| Movement | Fall death and respawn | ✅ | 🟡 a cut to black and back at the last safe ground for a third of max HP (our rule, the game's cost is not traced); the Construct's chasm |
| Movement | Upper/lower body layering | ❌ | ✅ |
| Combat | Attacks, hit reactions, hit stop, guard, deflect, posture | ✅ | ✅ |
| Combat | Deflect spam penalty | ? | ✅ |
| Combat | Perilous attacks, Mikiri, sweep counter | ✅ | ✅ |
| Combat | Super armour | ✅ | 🟡 flinch-free swings only, no toughness model |
| Combat | Status effects (poison, burn) | 🟡 | ✅ |
| Combat | Resurrection | ❌ | ✅ two nodes, locked after a resurrection until a deathblow; no Unseen Aid or Dragonrot |
| Deathblows | Front, after posture break | ✅ | ✅ |
| Deathblows | From behind, stealth, plunging | ❌ | ✅ |
| Deathblows | Boss deathblow counts and phases | 🟡 Owl, Genichiro | ✅ |
| Skills | 19 combat arts, 10 prosthetic tools | ❌ | ✅ |
| Skills | Gourd, spirit emblems | ❌ | ✅ |
| Items | Quick items (sugars, pellets, persimmon, Homeward Idol ...), inventory of every goods, pickups and the item dialog | ? | 🟡 the game's use states, effects, looks, texts and dialog for every quick item; held items shown by their effects' models (gourd, pellet, tanto ...); enemy drops and Resurrective Power, the Mibu Balloons, Five-color Rice and Divine Confetti's ghost barrier (gap: the exe's drop and luck formulas, a node's Power cost taken as 100) |
| Skills | Prosthetic tool upgrades (Sculptor's Workshop) | ? | 🟡 the game's tree and costs; reached from the idol menu (no Sculptor on the test map) |
| Enemies | All 102 placed kinds load | ✅ | ✅ |
| Enemies | Fights verified | 🟡 soldier, Owl, Genichiro | ✅ most of the roster |
| Enemies | Bosses, all phases (see [Bosses](#bosses)) | 🟡 15 of 15 in their arenas, 13 with every phase playable, none checked against the real game yet | ? |
| World | Boss arenas (see [Boss arenas](#boss-arenas)) | 🟡 13 of 13 staged with their bosses; weather and arena effects not drawn yet | ? |
| Enemies | Minibosses, all phases (see [Bosses](#bosses)) | ❌ 0 of 29 | ? |
| Enemies | Stealth and perception | ❌ | ✅ |
| Enemies | Several enemies at once | ❌ | ✅ |
| AI | Boss brain (learns the player, memory, coach) | ✅ Owl, Genichiro, soldier | ❌ |
| AI | AI debug modes | 🟡 | ✅ |
| World | Walkable maps | ✅ all 9 gameplay maps | 🟡 gate and boss arenas |
| World | Sandbox arena | ❌ | ✅ plus the Construct test map (`SHINOBI_MAP=construct`): a parkour course, a stealth outpost after the Ashina Outskirts one, a second section for the duel enemy, a pool and a chasm |
| World | Sculptor's Idols: pray, rest, checkpoint, Purchase Spirit Emblems, Travel | ? | 🟡 the game's model, flame, clips, menus and texts, Acquire Skills (skill points from kill experience) and Change Form; the Construct test map only |
| World | Sky domes | ✅ | 🟡 |
| World | Time of day | ✅ | ✅ with blending |
| World | Water | 🟡 | 🟡 |
| Rendering | Fog, exposure, tone mapping, bloom from the game's shaders | ✅ | 🟡 Bevy built-ins |
| Rendering | Colour grading, layered materials, shadows | ✅ | ✅ |
| Rendering | GI probes and bounce light | ✅ | 🟡 |
| Rendering | Point lights | ✅ | ❌ effect lights only |
| Rendering | Character materials | ✅ | ✅ |
| Effects | FXR particle player | 🟡 no model particles yet | ✅ |
| Effects | Blood, hit stains, clash sparks | ✅ | ✅ |
| Audio | Game's FMOD, TAE sounds, footsteps | ✅ | ✅ |
| Audio | 3D placement, reverb | 🟡 | ✅ |
| Audio | Boss music | ❌ | ✅ |
| UI | HUD and boss bars | 🟡 working bars, not the game's art | ✅ |
| UI | Title, pause, death, victory screens | 🟡 start and pause menus | ✅ incl. the game's 死 death screen with Die / Resurrect |
| UI | In-game menu: Equipment, Inventory, Skills, Options, Equipped Items | ? | 🟡 the game's art and layout from captures; Inventory and quick slots from the goods held |
| UI | Boss and enemy picker | ✅ start menu | ✅ in game |
| UI | Options screen | ❌ | ✅ |
| Release | Packaged build | ❌ | ✅ |

## Bosses

Done means every phase works, from the first bar to the final deathblow.
Phases are the deathblows needed (bars).
Codes are the character ids; variants share one code, so one working fight usually covers the rest.
Fill in your own column; claim a fight in `WORK.md` before starting it.

### Bosses (15)

| Boss | Code | Area | Phases | sekiro-rs | RustSekiro |
|---|---|---|---|---|---|
| Gyoubu Oniwa | c5080 | Ashina Outskirts | 2 | 🟡 every phase playable in its arena; not yet checked against the real game, gaps in docs/BOSSES-*.md | ? |
| Lady Butterfly | c5090 | Hirata Estate | 2 | 🟡 every phase playable in its arena; not yet checked against the real game, gaps in docs/BOSSES-*.md | ? |
| Genichiro Ashina (rooftop) | c7100, c7110 | Ashina Castle | 3 (2 + Way of Tomoe) | ✅ | ? |
| Great Shinobi Owl | c5060 | Ashina Castle | 2 | ✅ | ? |
| Folding Screen Monkeys | c1260 | Senpou Temple | 1 (four monkeys) | 🟡 partial: fights and shared health work; perception, navigation, natural victory missing | ? |
| Guardian Ape | c5100 | Sunken Valley | 2 (revives headless) | 🟡 every phase playable in its arena; not yet checked against the real game, gaps in docs/BOSSES-*.md | ? |
| Headless Ape | c5100 | Ashina Depths | 2 (two apes) | 🟡 every phase playable in its arena; not yet checked against the real game, gaps in docs/BOSSES-*.md | ? |
| Corrupted Monk (ghost) | c5000 | Ashina Depths | 1 | 🟡 every phase playable in its arena; not yet checked against the real game, gaps in docs/BOSSES-*.md | ? |
| True Corrupted Monk | c5000, c5005 | Fountainhead Palace | 3 | 🟡 every phase playable in its arena; not yet checked against the real game, gaps in docs/BOSSES-*.md | ? |
| Emma, the Gentle Blade | c7400 | Ashina Castle | 1 | 🟡 every phase playable in its arena; not yet checked against the real game, gaps in docs/BOSSES-*.md | ? |
| Isshin Ashina | c5430 | Ashina Castle | 1 | 🟡 every phase playable in its arena; not yet checked against the real game, gaps in docs/BOSSES-*.md | ? |
| Demon of Hatred | c7020 | Ashina Outskirts | 3 | 🟡 every phase playable in its arena; not yet checked against the real game, gaps in docs/BOSSES-*.md | ? |
| Great Shinobi Owl (Father) | c5060 | Hirata Estate | 2 | 🟡 every phase playable in its arena; not yet checked against the real game, gaps in docs/BOSSES-*.md | ? |
| Divine Dragon | c5200, c5300 | Fountainhead Palace | 2 | 🟡 partial: Old Dragons and Divine Dragon attacks work; grapple targets, lightning reversal missing | ? |
| Isshin, the Sword Saint | c7100, c5400 | Ashina Reservoir | 4 (Genichiro + 3) | 🟡 every phase playable in its arena; not yet checked against the real game, gaps in docs/BOSSES-*.md | ? |

### Minibosses (29)

| Miniboss | Code | Area | Phases | sekiro-rs | RustSekiro |
|---|---|---|---|---|---|
| General Naomori Kawarada | c1021 | Ashina Outskirts | 2 | ❌ | ? |
| General Tenzen Yamauchi | c1020 | Ashina Outskirts | 2 | ❌ | ? |
| General Kuranosuke Matsumoto | c1020 | Ashina Castle | 2 | ❌ | ? |
| Leader Shigenori Yamauchi | c1020 | Ashina Reservoir | 2 | ❌ | ? |
| Seven Ashina Spears - Shikibu Toshikatsu Yamauchi | c1021 | Ashina Reservoir | 2 | ❌ | ? |
| Seven Ashina Spears - Shume Masaji Oniwa | c1021 | Ashina Reservoir (invasion) | 2 | ❌ | ? |
| Ashina Elite - Jinsuke Saze | c1400 | Ashina Castle | 2 | 🟡 staged with its boss; arena effects not drawn yet | ? |
| Ashina Elite - Ujinari Mizuo | c1400 | Ashina Castle (invasion) | 2 | 🟡 staged with its boss; arena effects not drawn yet | ? |
| Chained Ogre (Outskirts) | c5020 | Ashina Outskirts | 2 | ❌ | ? |
| Chained Ogre (Castle) | c5020 | Ashina Castle (invasion) | 2 | ❌ | ? |
| Blazing Bull | c1370 | Ashina Outskirts | 1 | ❌ | ? |
| Shigekichi of the Red Guard | c1070 | Ashina Outskirts | 2 | ❌ | ? |
| Juzou the Drunkard | c1070 | Hirata Estate | 2 | ❌ | ? |
| Tokujiro the Glutton | c1070 | Ashina Depths (Mibu Village) | 2 | ❌ | ? |
| Shinobi Hunter Enshin of Misen | c1060 | Hirata Estate | 2 | ❌ | ? |
| Lone Shadow Masanaga the Spear-bearer | c1470 | Hirata Estate | 2 | ❌ | ? |
| Lone Shadow Vilehand | c1470 | Ashina Castle (invasion) | 2 | ❌ | ? |
| Lone Shadow Longswordsman | c1470 | Ashina Reservoir | 2 | ❌ | ? |
| Long-arm Centipede Sen'un | c1040 | Senpou Temple | 2 | ❌ | ? |
| Long-arm Centipede Giraffe | c1040 | Sunken Valley | 2 | ❌ | ? |
| Snake Eyes Shirafuji | c1191 | Sunken Valley | 2 | ❌ | ? |
| Snake Eyes Shirahagi | c1191 | Sunken Valley | 2 | ❌ | ? |
| Mist Noble | c1300 | Ashina Depths (Mibu Village) | 1 | ❌ | ? |
| O'Rin of the Water | c7000 | Ashina Depths (Mibu Village) | 2 | ❌ | ? |
| Okami Leader Shizu | c1310 | Fountainhead Palace | 1 | ❌ | ? |
| Sakura Bull of the Palace | c1380 | Fountainhead Palace | 2 | ❌ | ? |
| Armored Warrior | c1130 | Ashina Castle (invasion) | 1 | ❌ | ? |
| Headless (5 fights) | c1340, c1350 | Outskirts, Sunken Valley, Ashina Depths and more | 1 each | ❌ | ? |
| Shichimen Warrior (3 fights) | c1080 | Abandoned Dungeon, Sunken Valley, Fountainhead | 1 each | ❌ | ? |

Phase counts and codes are from the game data where we've read it; correct any that are wrong.

## Boss arenas

Done means the fight happens at its story spot in the full map: fog walls in and out, the story's time of day, and the arena's own events (illusions, screens, collapses).
Map ids are the game's; boss-bar entity ids are in brackets.

<details>
<summary>Boss arenas (13)</summary>

| Arena | Map | Fights there | sekiro-rs | RustSekiro |
|---|---|---|---|---|
| Ashina Castle, castle top | m11_01 | Genichiro and Tomoe (1110800, 1110801), Great Shinobi Owl (1110850) | 🟡 fog walls, story time of day; arena snow and lightning effects not drawn yet | ? |
| Ashina Castle, Shura ending | m11_01 | Emma (1110900), Isshin Ashina (1110920) | 🟡 staged with its boss; arena effects not drawn yet | ? |
| Ashina Reservoir, silvergrass field | m11_02 | Genichiro and Tomoe (1120800, 1120830), Isshin, the Sword Saint (1120860, 1120890) | 🟡 staged with its boss; arena effects not drawn yet | ? |
| Ashina Outskirts, castle gate | m11 | Gyoubu Oniwa (1100800) | 🟡 staged with its boss; arena effects not drawn yet | ? |
| Ashina Outskirts, Demon of Hatred | m11 | Demon of Hatred (1100900) | 🟡 staged with its boss; arena effects not drawn yet | ? |
| Hirata Estate, main hall | m10 | Lady Butterfly (1000800, 1000810) | 🟡 staged with its boss; arena effects not drawn yet | ? |
| Hirata Estate, Owl (Father) | m10 | Owl (Father) (1000900), Inner Father (1000990) | 🟡 staged with its boss; arena effects not drawn yet | ? |
| Senpou Temple, illusion screens | m20 | Folding Screen Monkeys (2000800) | 🟡 staged with its boss; arena effects not drawn yet | ? |
| Sunken Valley, watering hole | m17 | Guardian Ape (1700800) | 🟡 staged with its boss; arena effects not drawn yet | ? |
| Sunken Valley, ape's burrow | m17 | Headless Ape (1700850) | 🟡 staged with its boss; arena effects not drawn yet | ? |
| Ashina Depths, Mibu bridge | m15 | Corrupted Monk ghost (1500800) | 🟡 staged with its boss; arena effects not drawn yet | ? |
| Fountainhead Palace, bridge | m25 | True Corrupted Monk (2500850) | 🟡 staged with its boss; arena effects not drawn yet | ? |
| Fountainhead Palace, sanctuary | m25 | Divine Dragon and the Old Dragons (2500800, 2500810) | 🟡 staged with its boss; arena effects not drawn yet | ? |

</details>

Arena names are descriptive; the map and entity ids are from the game data.

## Biggest gaps

- **sekiro-rs:** the minibosses, boss gaps listed in `WORK.md`, combat arts and prosthetics, gourd, stealth, deathblows from behind and plunging, boss music, options and death screens, the wider roster.
- **RustSekiro:** boss brain, swimming, shader-accurate rendering (fog, tone mapping, GI, point lights, sky), the rest of the maps.

## Beyond the base game

Ideas that are new, not in the original game.
Not for now: the baseline comes first.
Claim one in `WORK.md` before starting it.

- **Fights that spill out of the arena.**
  A deathblow near an edge can push both fighters outside, and on the castle tower it felt cinematic.
  Allow it within limits: on the tower, at most one or two levels down, with a wall that stops the fall to the bottom, and the boss can follow you into the house below.
  If you still end up stuck, a start-menu option sends you back and restarts the fight.
- **Instant restart.**
  Press R after dying to restart the fight at once, like Hotline Miami, with no death screen or map reload; pick an equivalent controller button later.
  The test restart already does this in part; it needs to be fast enough to feel instant.
- **Upscaling and frame generation.**
  Add AMD FSR and NVIDIA DLSS (upscaling, then frame generation) so the game runs well on more PCs.
  The original game has neither, so there is nothing to decompile: both come as SDKs from AMD and NVIDIA (FSR is open source), and we plug them into our renderer.
  Research done: [sekiro-rs docs/UPSCALING.md](https://github.com/AKJama/sekiro-rs/blob/main/docs/UPSCALING.md); the rendering rules in `AGENTS.md` keep both projects ready for it.
