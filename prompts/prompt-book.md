# Prompt Book

Every prompt below is final and ready to fire. They all inherit
[`../art-direction/hero-lock.md`](../art-direction/hero-lock.md).

**Pipeline rule that matters:** asset `hero-00-master` is generated *first* and
alone. Every one of the eight flavour dials is then generated with the master
passed as an `image` reference, changing **only the dial colour phrase**. That
is what makes the camera and lighting genuinely identical rather than
approximately similar — re-rolling eight independent text prompts will not hold
a locked camera, and any drift shows up instantly when the cards sit in a row.

The same master is passed to Seedance as `image_references` so the video is the
same bottle as the cards.

---

## Block A — shared invariant

Prepended verbatim to all eight flavour prompts.

> Photoreal commercial product photography. Clear rPET protein bottle, seven
> fine horizontal ribs, conical shoulder, 38 mm collar, moulded two-ring vortex
> base. Shot on a 100 mm macro lens at f/5.6, camera locked at bottle-label
> height, 1.2 m subject distance, three-quarter front view, bottle centred,
> dead-level horizon, no tilt. Single cold gym-fridge key light from upper left
> at 5600K raking across the ribs, narrow deep-navy #1B3A6B bounce card at
> right, deep falloff to near-black #0A0F1A. Fine condensation beading on the
> chilled glass with a few droplets tracking down the shoulder. Left face label
> zone completely clean and empty. No text, no logo, no lettering, no hands.

---

## 1. Bottle wrap texture — `texture-01-bottle-wrap`

Flat seamless UV wrap for the 3D bottle. Not a photograph of a bottle.

- Model `nano_banana_pro` · resolution `4k` · aspect `21:9`

> Flat orthographic UV unwrap texture map of a clear rPET bottle wrap, laid out
> perfectly flat with zero perspective and zero curvature. Seamless tiling: the
> left and right edges match exactly so the wrap closes with no visible seam.
> Seven fine horizontal ribs running edge to edge as evenly spaced parallel
> bands, conical shoulder gradient toward the top, 38 mm collar band across the
> top edge. The left third is a completely clean empty label zone with no
> detail. Deep navy #1B3A6B tinted transparency with cold white #E8F1F7
> specular edges, fine condensation micro-droplets scattered across the
> surface, one signal orange #C4551A accent band at the collar. Even flat
> lighting across the whole map, no hotspots, no vignette, no baked directional
> shadow. No text, no logo, no lettering.

---

## 2. Flavour dials — `hero-00-master` + eight

Master first, then eight with the master as `image` reference.

- Model `nano_banana_pro` · resolution `2k` · aspect `4:5` (DOM card crop)

**`hero-00-master`** — Block A, then:

> The flavour dial at the collar is bare matte signal orange #C4551A.

**The eight.** For each, pass `hero-00-master` as an `image` reference and use
the single line below. Nothing else changes — not the camera, not the light,
not the bottle.

> Keep the camera, lighting, bottle, condensation and framing pixel-identical
> to the reference image. Change one thing only: the flavour dial at the collar
> is now **{DIAL}**.

| # | Flavour | `{DIAL}` |
|---|---|---|
| 1 | Chocolate | deep cocoa-brown matte |
| 2 | Vanilla | warm ivory-cream matte |
| 3 | Citrus | bright citrus yellow-orange matte |
| 4 | Mixed berry | deep magenta-violet matte |
| 5 | Cookies & cream | off-white matte with fine dark speckle |
| 6 | Salted caramel | burnt amber-caramel matte |
| 7 | Plain | bare matte signal orange `#C4551A` |
| 8 | +C creatine | cold clinical white-blue matte |

Flavour 7 is the master look — generate it as a straight copy of the master so
the set stays a clean eight without a re-roll.

---

## 3. Particles — `particle-01…05`

Generated on a pure void background so the cutout is clean, then run through
`remove_background`.

- Model `nano_banana_pro` · resolution `2k` · aspect `1:1`

Shared tail, appended to each:

> Isolated dead-centre on a pure flat black #0A0F1A void background, subject
> fully separated from the background with clean edges, no environment, no
> surface, no horizon, no props. Cold 5600K lighting, deep navy #1B3A6B shadow
> tint, cold white #E8F1F7 speculars. Macro, high shutter, razor sharp. No
> text, no logo, no hands.

| Asset | Head of prompt |
|---|---|
| `particle-01-powder-burst` | A dry protein powder burst frozen mid-air, a fine dense cloud of loose particulate expanding outward with individual grains visible at the edges. |
| `particle-02-protein-bloom` | A protein bloom unfurling through water, dense opaque tendrils curling and billowing outward into clear liquid, true fluid dynamics. |
| `particle-03-milk-swirl` | A milk swirl folding through liquid in a slow spiral, thick opaque ribbons wrapping over each other, true fluid dynamics. |
| `particle-04-ice-crystals` | A scatter of sharp clear ice crystals suspended in mid-air, faceted and refracting, cold blue-white cores. |
| `particle-05-condensation` | A cluster of condensation droplets on chilled glass, beading tight and beginning to track downward, each bead refracting the light behind it. |

---

## 4. Section backgrounds — `bg-01…03`

- Model `nano_banana_pro` · resolution `4k` · aspect `16:9`

| Asset | Prompt |
|---|---|
| `bg-01-brushed-steel` | Brushed steel gym-fridge interior wall, fine horizontal brush grain running edge to edge, cold 5600K light raking from upper left, deep navy #1B3A6B tint in the shadows, falloff to near-black #0A0F1A at the edges, faint condensation haze. Empty, no products, no shelves in focus, no text, no logo. Clean plate for a web section background. |
| `bg-02-navy-gradient` | Soft deep navy #1B3A6B gradient field, smooth and completely even, falling off to near-black #0A0F1A toward the edges, a single cold 5600K light bloom in the upper left, gentle film grain, no banding. Abstract, empty, no subject, no text, no logo. Clean plate for a web section background. |
| `bg-03-frosted-glass` | Frosted glass surface seen straight on, fine even frost texture with cold 5600K light diffusing through from behind, deep navy #1B3A6B tint, scattered condensation beads catching cold white #E8F1F7 speculars, falloff to near-black at the edges. Empty, no subject, no text, no logo. Clean plate for a web section background. |

---

## 5. Cinematic video — `video-01-hero`

- Model `seedance_2_0` · resolution `4k` · mode `std` · duration `5s` ·
  aspect `16:9` · `generate_audio: false`
- `hero-00-master` passed as `image_references` to lock the bottle

`generate_audio` is off because this is a loop-friendly web hero — it plays
muted. Flip it to `true` only if the cut is going somewhere with sound.

**Why this prompt is not the 10s prompt with a smaller number.** At 5s the
three beats get ~1.6s each. The long per-beat descriptions written for 10s make
the model try to stage setup, action and settle inside each beat, and at 1.6s
it either rushes all three or drops the third. So the beats are cut to one
action verb each, the hand exit is removed, and the vortex — the beat that
actually sells the product — is the one given room. Everything else is
compressed to a clause.

> Photoreal macro cinematography of a clear rPET protein bottle, physically
> accurate, true fluid simulation, slow motion, shallow macro depth of field.
> Cold gym-fridge key light from upper left at 5600K, deep navy #1B3A6B
> environment, near-black falloff, condensation on the chilled glass.
>
> Three continuous beats, no dead frames, no pauses between them:
>
> One — a single clean hand twists the collar dial right and the sealed chamber
> drops a dose of dry powder into the water.
>
> Two — the bottle shakes and the moulded two-ring vortex base drives a visible
> spiral, the powder blooming through the water in real turbulent tendrils
> until it runs evenly mixed and opaque. Hold on this.
>
> Three — the collar twists left and opens.
>
> The shot begins and ends on the same still bottle in the same position so the
> clip loops seamlessly. Photoreal only — no stylised motion, no cartoon
> physics, no speed ramps, no extra hands, no text, no logo.

If the cut comes back with beat three clipped, the fix is to drop beat one to a
half-second dial-twist and let the powder already be falling on frame one —
not to lengthen the clip.
