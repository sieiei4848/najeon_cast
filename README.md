# NAJEON — Model Casting (mockup round 1)

> Brainstorming / look-development pass. **Not final talent.** Generated with Higgsfield Soul 2.0 (stills) + Seedance 2.0 (video) from `najeon-model-casting-spec.md`.

**For Danny:** open **`casting-board.html`** in any browser — it lays out all four faces with motion clips, in the NAJEON brand styling. Everything is local; no login needed.

## What's here
```
casting/
├─ casting-board.html      ← start here (visual board)
├─ README.md               ← this file
├─ stills/                 ← 16 PNGs (2048px, 3:4)
│   └─ <MODEL>-front-A/-front-B/-34/-profile.png
└─ videos/                 ← 4 MP4s (720p, ~5s, silent, slow)
    └─ PEARL / ONYX / BRASS / NACRE .mp4
```

## The four faces
| Model | Role | Look | Recommended keeper |
|---|---|---|---|
| **PEARL** | classic cover | long ash-platinum, glacial, 178cm | front **B** |
| **ONYX** | lookbook (sharp) | jet blue-black bob + baby fringe, berry lip, 163cm | front **B** |
| **BRASS** | lookbook (warm) | honey-bronde wavy bob, freckles, 167cm | front **B** |
| **NACRE** | lead muse / hero | raven black, ultra-high cheekbones, nacre shimmer, 180cm | front **B** |

## Reproducibility log (Higgsfield job IDs + seeds)
Keepers are the references all later shots + videos were locked to.

| Model | Keeper job ID | Seed | Front-A seed |
|---|---|---|---|
| PEARL | `30881861-30f2-4477-a616-1f806ec93f6f` | 97114 | 140210 |
| ONYX  | `4f7c68fc-5414-4a9d-9649-24c5413c4d05` | 165100 | 883563 |
| BRASS | `79107cac-fab2-45c4-9f7d-ec1c71c546d1` | 185606 | 135937 |
| NACRE | `54ba594f-50e6-4601-bed6-2c740aad92a8` | 493403 | 609390 |

Model: `soul_2` (Higgsfield Soul 2.0), 2k, 3:4. Video: `seedance_2_0`, 720p, 5s, `generate_audio:false`. Prompts = the spec's `SOUL PROMPT` / `SEEDANCE PROMPT` verbatim.

## Consistency findings (the real point of this round)
1. **Archetype lock = strong.** Same prompt reliably reproduces the casting *type*.
2. **Identity lock ≠ text alone.** Two runs of one prompt = two different women of the same type.
3. **Soul 2.0 auto-rewrites the prompt** (`enhance_prompt`), which drifts features (nudged Onyx toward "Mediterranean/olive") and **ignored the 3/4 + profile pose requests** (rendered near-frontal).
4. **Seedance video holds the face** much better when driven from the locked front portrait.

## Recommended next step → true identity lock
To get the *same person* across a full campaign:
1. Pick one keeper per model (defaults above).
2. **Train a reusable Soul character** per model (5–20 generated images of that one face, ~10 min each). This is the spec's "lock the Soul ID" step.
3. Then every still + Seedance clip is the identical individual — swap only pose / wardrobe / crop.

## Credits
Round 1 spend ≈ **92 credits** (16 stills ≈ 2 + 4 videos × 22.5). Balance after: ~838.
