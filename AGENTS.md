# AGENTS.md

Shared plan for two Sekiro rewrites in Rust and Bevy:

- [AKJama/sekiro-rs](https://github.com/AKJama/sekiro-rs) (Yama)
- [FFwLo/RustSekiro](https://github.com/FFwLo/RustSekiro) (FwLo)

No code here, just who does what and what's in progress.
If you are an agent working for either of us, read this first every session.

## Every session

1. Pull this repo, read `FEATURES.md` and `WORK.md`.
2. Pick anything not already claimed in `WORK.md`.
3. Check `FEATURES.md` and the other repo first; if it's already done there, reuse it.
4. Claim it in `WORK.md` (move it to Claimed with your owner's name and the date), commit and push straight away.

## Keep everything pushed

- Push your project often: small commits as you go, no releases or tags needed.
- When a task is done, move it to Done in `WORK.md` with a link to the commit.
- When a feature changes status, update your column in `FEATURES.md`.
- Push this repo whenever you change it, so the other side always sees the current state.

## Rendering rules (for upscaling and frame generation later)

Both projects will want DLSS and FSR, and frame generation most of all.
They only work if the renderer gives them correct inputs, so follow these now in any visual work:

- Every custom material and shader writes depth and motion vectors, including sky, fog, FX, decals, cloth and anything faded or alpha-tested.
- Anything moved on the CPU (cloth, particles) keeps its previous-frame position.
- Blended effects (smoke, sparks, fog, glass) are marked as transparent or reactive.
- The UI and HUD draw outside the scene pass, so a HUD-less image is always available.
- Keep a render scale separate from the window size, and do not hard-wire the MSAA sample count.
- Keep camera jitter, exposure and history resets in one place.

Details, sources and what Bevy 0.19 and wgpu 29 already offer: [sekiro-rs docs/UPSCALING.md](https://github.com/AKJama/sekiro-rs/blob/main/docs/UPSCALING.md).

## Rules

- No game files, extracted data or decompiled code in any repo.
- Both projects are MIT, so reuse each other's work and note it in your project.
- Short Markdown, plain dashes, one change per commit where possible.
