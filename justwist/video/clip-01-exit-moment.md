# Clip 01 — "The Exit Moment" (قبل السيارة)

The chosen hero clip: hyper-realistic, human-led, built directly on the
customer journey in the business plan (§4.3): finish training → sight the
machine on the exit path → tap → twist, shake, drink before the car.
Inherits `../design-lock.md` — palette, geometry, cap colours, negatives.

## Why this clip

1. **It is the plan's own journey** — §4.3 word for word, turned into film.
2. **Trust is the product's stated problem** (60.7 % discover via social;
   counterfeit anxiety) — a real human face in a real Saudi gym is the trust
   carrier. No abstract product float.
3. **The ritual is self-explaining** (Rogers: observable, trialable — §4.1).
   Half of new gym joiners are first-timers; the ad must double as a demo.
4. **Realism sells the physics.** The fresh-vs-pre-mixed claim (survey Q12)
   lives or dies on the powder drop and vortex reading photoreal.

## Spec

- **Format:** 9:16 vertical (social-first — the plan's discovery channel).
  Later re-cuts: 16:9 web hero, 1:1.
- **Duration:** 10 s master. If beats rush, split into 2 × 5 s shots
  (A: corridor + machine; B: ritual + exit) and stitch.
- **Model:** Seedance 2.0 (PLUS unlocked), master still passed as
  `image_references` for identity lock.
- **Audio:** generate off for the master (plays muted on social); sound pass
  later if needed: gym hum, seal click, powder cascade, slosh, exhale. No
  dialogue.
- **SKU on camera:** MP-09 Milk protein Chocolate — brown dial, 25 g, milk
  reads opaque white in the clear bottle (strongest visual contrast).

## Beat sheet (10 s)

| Time | Beat |
|---|---|
| 0.0–2.0 | Modern Saudi gym exit corridor, cool neon. Saudi man late 20s, athletic, light beard, navy training tee dark with sweat, towel on shoulder — walking out tired, deep breath. |
| 2.0–3.5 | His face catches a navy-gold glow. The JUSTWIST machine: glass front, wall of colour-coded caps. He taps his watch on the reader. |
| 3.5–5.0 | Elevator tray lifts the bottle gently. He takes it — condensation beads, tall cocoa-brown dial printed **25g**. |
| 5.0–7.5 | Macro insert: right twist — soft click — a column of dry powder drops into the milk. Circular shake — visible vortex from the moulded base, powder blooming in turbulent tendrils to evenly mixed. |
| 7.5–10.0 | Left twist, long sip, satisfied exhale, half-smile. He walks on toward the car park, bottle in hand. End frame clean for logo + TWIST · SHAKE · DRINK. |

## Camera / grade

Cinematic handheld feel; ~35 mm for the walk, 100 mm macro for the
twist/vortex insert; shallow DOF. Cold gym neon against the machine's warm
gold-on-navy glow (#002454 / #A86000). Real skin texture, sweat sheen, no
beauty filter. Subtle 1.5× slow on the vortex only — otherwise real time.

## Generation prompt (EN, final draft)

> Hyper-photorealistic cinematic commercial footage, vertical 9:16. A Saudi
> man in his late twenties, athletic build, short dark hair, light beard,
> navy training t-shirt darkened with sweat, towel over one shoulder, walks
> exhausted down a modern gym exit corridor under cool neon light. His face
> catches a warm glow: a navy-and-gold JUSTWIST vending machine with a glass
> front full of chilled clear bottles topped by colour-coded caps. He taps
> his smartwatch on the payment reader; an elevator tray gently lifts one
> bottle. He takes it — fine condensation beading on the cold clear bottle,
> a tall cocoa-brown cap dial printed "25g", white milk inside. Macro
> close-up: his fingers twist the upper dial right with a soft click and a
> column of dry powder drops through the neck into the milk; he shakes the
> bottle in a fast circular motion and the moulded base drives a visible
> spiral vortex, the powder blooming in real turbulent tendrils until the
> drink runs evenly mixed. He twists the lower collar left, opens it, takes
> a long drink, exhales with quiet satisfaction and walks on toward the car
> park with the bottle in hand. True fluid simulation, real skin texture and
> sweat sheen, shallow cinematic depth of field, cold neon corridor against
> warm gold machine glow, photoreal only — no stylised motion, no cartoon
> physics, no extra hands, no on-screen text, no logos except on the machine
> and cap.

## Pipeline & cost discipline

1. **Master still** (nano_banana_pro): athlete at the machine — locks face,
   wardrobe, machine, bottle. ~2 credits.
2. **Proof cut** at 480–720p from the still — verify beats + fluid sim
   before real money. ~7–20 credits.
3. **Final** 1080p (social) or 4K: preflight the exact cost before firing
   (old ladder: 1080p/std/5s = 45; 4K/std/10s = 220 — confirm live).

## Generation log

| Take | Job ID | Spec | Cost | Status |
|---|---|---|---|---|
| Proof cut 1 | `51643118-d122-4636-a91f-b931b7c32227` | seedance_2_0 · 480×854 · 10 s · std · silent · text-to-video (no reference — master still was skipped) | 10 cr actual (30 held, 20 released) | Completed 2026-08-03, awaiting founder eye |
| Machine placement mock A | `618b52d5-1747-4cc8-a115-8b942a24309f` | nano_banana_pro→nb2 · 2K · 9:16 · text-only (uploads blocked by egress; machine + pool described from J8 render and founder's pool photos) | 2 cr | Completed, awaiting founder pick |
| Machine placement mock B | `a73e1dff-f7cf-4bc4-826e-4e0f223dfadf` | same prompt, variant 2 | 2 cr | The keeper — sole survivor of the founder's gallery cleanup |
| Placement mock A2 | `65350c3d-d08f-402a-ae99-d330c5a99bb8` | nano_banana_pro→nb2 · 2K · 9:16 · mock A as ref; no glass, lengthwise pool | 2 cr | Deleted by founder from gallery (with mock A) |
| Placement mock B2 | `f6534391-d92b-4219-bb09-07347b0a17bf` | nano_banana_pro→nb2 · 2K · 9:16 · surviving mock B passed as `image` ref; machine locked right-of-centre; glass partition + pool view moved to the LEFT of frame; pool rotated CROSSWISE — lane ropes running parallel to the glass, swimmer/wave murals on the far long wall | 2 cr | Superseded by B3 |
| Placement mock B3 (anchor candidate) | `9431704e-cfff-4754-b6ae-3e7e55028c92` | nano_banana_pro→nb2 · 2K · 9:16 · B2 as ref; four founder fixes: ~3 m tile walkway between glass and pool edge, racing starting block at the head of every lane, machine + logo corrected to the exact file design (athlete-in-gold-orbit, serif wordmark, TWIST·SHAKE·DRINK, 4×6 shelves, TAP TO PAY panel, PUSH flap), treadmills and bikes clearly visible on the mezzanine, overall realism pushed | 2 cr | Completed, awaiting founder eye |

**Location change (founder direction, 2026-08-03):** the scene moves from a
generic gym exit corridor to the founder's real club — the machine stands in
the lobby corridor at the glass-partition corner beside the grey stone column,
with the indoor turquoise lap pool, red-and-white sport murals, wood-slat
walls and mezzanine visible behind it through the glass. The chosen placement
mock becomes the anchor frame for the video re-shoot, and machine interaction
realism (scale, contact shadow, reflections, believable tap-pay and pick-up)
is the founder's top priority.

## Alternates (parked, not chosen)

- **B — "أول مرة":** first-timer tries it while friends watch — social proof
  angle, needs multi-character consistency (harder).
- **C — Women's cut:** same journey, female athlete, women's gym — the
  fastest-growing segment (13.05 % CAGR); strong second clip after the hero.
