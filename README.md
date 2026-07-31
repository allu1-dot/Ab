# Visual assets

Generated with the Higgsfield MCP, all matched to the approved hero:
deep navy `#1B3A6B`, signal orange `#C4551A`, cold gym-fridge key light,
condensation on chilled glass.

| File | What it is |
|---|---|
| [`art-direction/hero-lock.md`](art-direction/hero-lock.md) | Palette, lighting, camera, product, global negatives. Source of truth. |
| [`prompts/prompt-book.md`](prompts/prompt-book.md) | All 19 prompts, final and ready to fire. |
| [`assets/manifest.json`](assets/manifest.json) | Machine-readable asset list — model, resolution, cost, dependency order, status. |

## Deliverables

1. **Bottle wrap texture** — flat seamless UV wrap, 4K, for the 3D bottle.
2. **Eight flavour-dial heroes** — DOM cards + social. Identical camera and
   lighting; dial colour is the only variable.
3. **Five particle plates** — powder burst, protein bloom, milk swirl, ice
   crystals, condensation. Background removed.
4. **Three section backgrounds** — brushed steel, navy gradient, frosted glass.
5. **One cinematic video** — Seedance 2.0, 4K, three beats, loop-friendly.

## The pipeline rule

`hero-00-master` is generated first and alone. All eight flavour dials are then
generated with the master passed as an `image` reference, changing only the
dial colour phrase. The same master goes to Seedance as `image_references`.

This matters: eight independently-rolled text prompts will not hold a locked
camera, and the drift is obvious the moment the cards sit in a row on the page.

## Budget

Live preflight figures from the MCP, not estimates.

| Group | Count | Credits |
|---|---|---|
| Bottle wrap texture (4K) | 1 | 4 |
| Flavour heroes (2K) — master + 8 | 9 | 18 |
| Particle plates (2K) | 5 | 10 |
| Section backgrounds (4K) | 3 | 12 |
| **Images subtotal** | **18** | **44** |
| Seedance 2.0, 4K std 10s | 1 | 220 |
| **Total** | **19** | **264** |

Particle background removal has no cost-preflight endpoint and is additional.

Video alternatives: 4K std 5s = 110 credits · 1080p std 5s = 45 credits.

**Status: blocked on credits.** Balance at planning time was 10 credits on the
free plan, with trial/unlimited generations unavailable — about 4% of the run,
and the video alone is 22× the balance. Everything above is complete and
costed; generation fires as soon as the account is funded.
