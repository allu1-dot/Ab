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
| Seedance 2.0, 4K std 5s | 1 | 110 |
| **Total** | **19** | **154** |

Particle background removal has no cost-preflight endpoint and is additional.

Video alternatives: 1080p std 5s = 45 credits · 4K std 10s = 220 credits.

## Status

**Blocked on credits.** 6 credits remain on the free plan against a 154-credit
run. One-time credit packs are not purchasable on this workspace; only
PLUS/ULTRA plan upgrades are offered. The video is now specced at 5s (110)
rather than 10s (220).

Generated so far (5.2 credits spent, 4.8 remaining):

| Asset | Job ID | Result |
|---|---|---|
| `hero-00-master` | `42ff1343…5ce5` | 1856×2304 |
| `hero-01-chocolate` | `aaa0d6b8…6c58` | 1856×2304, master accepted as `image` reference |
| `video-02-proof-cut` | `f820c525…95aa` | 854×480, 4s, silent, seed 429144 |

The two stills validate the pipeline: the master's job ID is accepted as a
reference and the derived dial comes back at identical framing.

The proof cut is a **substitute for `video-01-hero`, not a replacement** —
480p instead of 4K, 4s instead of 5s, `seedance1_5` instead of `seedance_2_0`.
It exists because `seedance_2_0` is tier-locked and this was the cheapest model
that clears the gate. Its job is to show the three beats and prove the fluid
simulation reads photoreal before 110 credits go into the real render.

Remaining: 16 images, 5 cutouts, and the 4K hero video.

## Three things that need you

1. **Plan tier — the hard blocker on the video.** Seedance 2.0 returns
   `job_minimum_basic_plan_required` (403) on the free plan, independent of
   credits. A 480p/fast/4s test costing exactly the 6 available credits was
   rejected on tier, not funds, and nothing was charged. **Credits alone will
   not unblock the video** — PLUS or ULTRA is required; both list Seedance 2.0
   as full access.
2. **Credits** — 148 short of the 154-credit run. One-time credit packs are not
   purchasable on this workspace, only plan upgrades.
3. **Egress** — this session's policy returns 403 on CONNECT to the Higgsfield
   CDN (`d8j0ntlcm91z4.cloudfront.net`), so generated files cannot be pulled
   into the repo and cannot be visually checked from here. The assets live in
   the Higgsfield gallery; `manifest.json` tracks each by job ID and URL.
   Allowlisting that host lets the binaries be committed alongside the specs.

Neither render above has been approved by eye — see `delivery` in the manifest.

The image half of the run is not plan-gated: the two heroes generated fine on
the free plan. Only Seedance is tier-locked.
