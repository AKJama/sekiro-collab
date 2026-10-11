# Features

What each project has, as of 11 October 2026.
✅ done, 🟡 partial, ❌ not yet, ? not checked.
Keep your own column up to date.

| Area | Feature | sekiro-rs (Yama) | RustSekiro (FwLo) |
|---|---|---|---|
| Data | Archives, params, animation, TAE, behaviour graphs | ✅ | ✅ |
| Data | Player script | ✅ runs the real HKS bytecode | ✅ ported state machine |
| Data | Enemy Lua AI, EMEVD events | ✅ | ✅ |
| Data | Models and materials | ✅ | ✅ |
| Data | Cloth data | ❌ | ✅ |
| Movement | Walk, run, sprint, steps, jumps, air control, crouch | ✅ | ✅ |
| Movement | Lock-on strafing, kick-jump | ✅ | ✅ |
| Movement | Sheathed walk and run | 🟡 | ✅ |
| Movement | Grappling hook | ✅ arcs, air and chained | ✅ incl. enemy targets |
| Movement | Ledge hang and climb | 🟡 | ? |
| Movement | Wall hug | ✅ | ? |
| Movement | Swimming and diving | ✅ | ❌ |
| Movement | Fall death and respawn | ✅ | ? |
| Movement | Upper/lower body layering | ❌ | ✅ |
| Combat | Attacks, hit reactions, hit stop, guard, deflect, posture | ✅ | ✅ |
| Combat | Deflect spam penalty | ? | ✅ |
| Combat | Perilous attacks, Mikiri, sweep counter | ✅ | ✅ |
| Combat | Super armour | ✅ | ? |
| Combat | Status effects (poison, burn) | 🟡 | ✅ |
| Combat | Resurrection | ❌ | ✅ |
| Deathblows | Front, after posture break | ✅ | ✅ |
| Deathblows | From behind, stealth, plunging | ❌ | ✅ |
| Deathblows | Boss deathblow counts and phases | 🟡 Owl, Genichiro | ✅ |
| Skills | 19 combat arts, 10 prosthetic tools | ❌ | ✅ |
| Skills | Gourd, spirit emblems | ❌ | ✅ |
| Enemies | All 102 placed kinds load | ✅ | ✅ |
| Enemies | Fights verified | 🟡 soldier, Owl, Genichiro | ✅ most of the roster |
| Enemies | Great Shinobi Owl | ✅ | ✅ |
| Enemies | Genichiro rooftop, Tomoe, lightning reversal | ✅ | 🟡 arena and lightning |
| Enemies | Other bosses' events (Monk phantoms, summons, warps) | ❌ | ✅ |
| Enemies | Stealth and perception | ❌ | ✅ |
| Enemies | Several enemies at once | ❌ | ✅ |
| AI | Boss brain (learns the player, memory, coach) | ✅ Owl, Genichiro, soldier | ❌ |
| AI | AI debug modes | 🟡 | ✅ |
| World | Walkable maps | ✅ all 9 gameplay maps | 🟡 gate and boss arenas |
| World | Sandbox arena | ❌ | ✅ |
| World | Sky domes | ✅ | 🟡 |
| World | Time of day | ✅ | ✅ with blending |
| World | Water | 🟡 | 🟡 |
| Rendering | Fog, exposure, tone mapping, bloom from the game's shaders | ✅ | 🟡 Bevy built-ins |
| Rendering | Colour grading, layered materials, shadows | ✅ | ✅ |
| Rendering | GI probes and bounce light | ✅ | 🟡 |
| Rendering | Point lights | ✅ | ? |
| Rendering | Character materials | 🟡 | ✅ |
| Effects | FXR particle player | 🟡 | ✅ |
| Effects | Blood, hit stains, clash sparks | ❌ | ✅ |
| Audio | Game's FMOD, TAE sounds, footsteps | ✅ | ✅ |
| Audio | 3D placement, reverb | 🟡 | ✅ |
| Audio | Boss music | ❌ | ✅ |
| UI | HUD and boss bars | ✅ | ✅ |
| UI | Title, pause, death, victory screens | 🟡 start and pause menus | ✅ |
| UI | Boss and enemy picker | ✅ start menu | ✅ in game |
| UI | Options screen | ❌ | ✅ |
| Release | Packaged build | ❌ | ✅ |

## Biggest gaps

- **sekiro-rs:** combat arts and prosthetics, gourd, cloth, effects and blood, stealth, deathblows from behind and plunging, boss music, options and death screens, the wider roster.
- **RustSekiro:** boss brain, swimming, wall hug, shader-accurate rendering (fog, tone mapping, GI, point lights, sky), the rest of the maps, Genichiro's rooftop.

## Open questions

- One definition of "enemy works": loads, fights, or passes every phase.
