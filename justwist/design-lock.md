# JUSTWIST — Design Lock (source of truth)

Distilled from the JUSTWIST business plan (v20, August 2026). Every future
visual asset — image, video, web, vending UI — is generated against this file.
If an asset disagrees with this file, the asset is wrong.

Fresh start: this file supersedes everything previously in this repo
(`art-direction/hero-lock.md`, `prompts/`, `assets/` describe an older,
unrelated concept and are retired).

---

## 1. The idea in one breath

**JUSTWIST** — Saudi-made fresh-mix sports nutrition. The bottle holds only
liquid (water or UHT milk). The cap's sealed dial holds the dry powder until
the moment of purchase. **Twist right** → frangible seal shears, powder drops.
**Shake** → the moulded two-ring vortex base mixes a fresh drink. **Twist
left** → open and drink. Zero loose parts, nothing pre-mixed, no cold chain.
Sold chilled (2–6 °C, taste only) from branded gym fridges, later 45-selection
IoT vending machines. Tagline ritual: **TWIST · SHAKE · DRINK**.
"Fresh at the point of need — made in Saudi."

## 2. Brand identity

- **Logo:** flexing athlete silhouette in navy inside a **gold twist orbit**
  (ellipse sweeping around him). Serif wordmark **JUSTWIST** in navy with gold
  bevel; on navy backgrounds the wordmark sets in solid off-white, orbit rule
  carries the gold. Sub-line: TWIST · SHAKE · DRINK (gold, letterspaced).
- **Core palette:**
  | Token | Hex | Use |
  |---|---|---|
  | Deep navy | `#002454` | Brand fields, hero backgrounds, wordmark |
  | Dark gold | `#A86000` | Twist orbit, CTAs, accents |
  | Light gold | `#DDA23F` | Gradients with dark gold, highlights |
  | Steel blue | `#8B9EC1` | Secondary UI, neutral collar grey-blue |
  | Off-white | `#FCFCFA` | Light backgrounds, reversed wordmark |
- **Application rule (hard):** navy carries the brand, gold carries the twist.
  Flavour colour lives **only on the cap dial** — never on the wordmark,
  never on the bottle.
- Clear space = height of the gold orbit on all sides; min print width 18 mm.

## 3. Product geometry (Appendix I values)

### Bottles — two widths, near-equal heights; width encodes dose family
Slim horizontally-ribbed Saudi water-bottle archetype, clear rPET, seven fine
body ribs, conical shoulder, 38 mm wide mouth, 13 mm neck.

| Family | Outer Ø | Height | Body/shoulder/neck | Capacity | Fill | Tallest assembly |
|---|---|---|---|---|---|---|
| Protein (16 SKUs) | 66 mm | 183 mm | 150/20/13 mm | 400 ml | 300 ml | ≈255 mm (combo cap) |
| Small-dose (6 SKUs) | 56 mm | 181 mm | 148/20/13 mm | 300 ml | 250 ml (creatine) / 240 ml (EAA) | ≈219 mm (EAA cap) |

### Vortex base (moulded in, no mixer ball, no loose parts)
Central dome ≈ Ø18 × 8 mm high · inner ring of **six radial petals** (11 mm
tapering to 5 mm) · outer ring of **eight conical pins** (Ø5 × 6 mm) offset
between the petals. No still corner; bottle walls above completely clean.

### Two-stage cap — one Ø48 mm body, one 38 mm thread
- **Lower OPEN collar, 10 mm, neutral steel-blue/grey:** twist LEFT ↺ unscrews
  the whole unit to drink.
- **Upper ACTIVATE dial, flavour-coloured, carries the sealed dry chamber:**
  twist RIGHT ↻ shears the frangible seal; powder drops through the collar's
  open bore. Dial is captive — turns in place, cannot lift off; parts are
  flush, permanently joined.
- **Dial height = dose signal.** Dose number prints LARGE on the dial.

| Cap | Payload | Chamber | Dial h | Total h |
|---|---|---|---|---|
| Combo (protein+creatine) | 25 g + 5 g | ≈63 ml | ≈60 mm | ≈72 mm |
| Protein | 25 g | ≈56 ml | ≈54 mm | ≈66 mm |
| EAA | 10 g | ≈18 ml | ≈26 mm | ≈38 mm |
| Creatine | 5 g | ≈8 ml | ≈20 mm | ≈32 mm |

Combo caps add a **"+C" marker ring** (checker band at dial top).

## 4. Flavour → dial colour key (identity lives on the cap)

| Flavour | Dial colour |
|---|---|
| Chocolate | Deep cocoa brown |
| Vanilla | Warm cream/tan |
| Citrus Twist | Green |
| Mixed Berry | Purple |
| Cookies & Cream | Black/white split |
| Salted Caramel | Gold/amber |
| Plain (unflavoured) | White |
| Still water (traffic SKU) | Blue |

## 5. The 22-SKU ladder — fixed prices, SAR 3 steps

| Family | Bottle | Liquid | Payload | Flavours | Price |
|---|---|---|---|---|---|
| Water protein (WP-01..04) | 66×183 | 300 ml water | 25 g | Choc, Vanilla, Citrus, Berry | SAR 12 |
| Water protein +C (WC-05..08) | 66×183 | 300 ml | 25+5 g | same 4, +C ring | SAR 15 |
| Milk protein (MP-09..12) | 66×183 | 300 ml UHT milk | 25 g | Choc, Vanilla, C&C, Caramel | SAR 15 |
| Milk protein +C (MC-13..16) | 66×183 | 300 ml | 25+5 g | same 4, +C ring | SAR 18 |
| Creatine water (CR-17..19) | 56×181 | 250 ml | 5 g | Citrus, Berry, Plain | SAR 9 |
| EAA water (EA-20..22) | 56×181 | 240 ml | 10 g | Citrus, Berry, Plain | SAR 9 |

Milk SKUs read as opaque white liquid in the clear bottle; water SKUs read as
clear liquid with navy environment tint.

## 6. Channel & machine (distribution imagery)

- **Phase 1:** dedicated branded coolers on the gym exit path (Leejam/Fitness
  Time, Armah, GymNation context). Zero capex, 15 % commission red line.
- **Phase 2:** 45-selection glass-front chilled vending machine, ≈400 bottles,
  **elevator (gentle-lift) delivery mandatory** (protects the frangible seal),
  single shelf pitch ≈260 mm, cabinet 2–6 °C, cashless only (mada + Apple
  Pay), IoT telemetry. Cream/off-white cabinet shell, navy glass interior,
  JUSTWIST wordmark + athlete-orbit logo on the header.
- **Planogram (both channels):** 24 stocked lanes across 4 shelves × 6 deep =
  144 bottles. Lane 01 far right → lane 24 far left. Shelf 1: Chocolate
  family + Citrus small-dose; Shelf 2: Vanilla family + Berry small-dose;
  Shelf 3: C&C family + Plain small-dose; Shelf 4: Caramel family + Berry
  water SKUs + 2 blue still-water lanes (SAR 2). Lane rail shows code,
  flavour, dose, price.
- **Purchase journey:** SELECT (or lane code) → TAP TO PAY → PICK UP (elevator,
  PUSH flap) → twist right → shake → twist left → drink before the car.

## 7. Landing page reference (justwist.sa draft)

Navy hero with reversed logo + wordmark, gold tagline "Fresh at the point of
need — made in Saudi", TWIST·SHAKE·DRINK, gold CTA **Find a machine**, product
render right. Below: 3 ritual cards (01 Twist right / 02 Shake / 03 Twist
left), flavour chip row (dial colour = flavour), navy price-ladder band, footer
"Zero cold chain · zero loose parts · SFDA-registered · 22 SKUs".

## 8. Voice & claims (safe copy pool)

- Fresh at the point of need · Made in Saudi · TWIST · SHAKE · DRINK
- Zero cold chain · zero loose parts · nothing pre-mixed
- The bottle holds the liquid. The cap holds everything else.
- Dial colour = flavour · dial height = dose · number printed large
- SFDA-registered, halal-certified inputs
- Price ladder: 9 / 12 / 15 / 18 SAR
- Audience: Saudi gym members at the post-workout exit moment; three
  segments — cutting (water line), bulking (milk line), lactose-intolerant
  (isolate water line). 59.1 % of Saudi adults train ≥150 min/week.

## 9. Video-relevant physics (for prompt writing)

- Right twist: cam shears frangible seal → dry powder column drops through
  the 38 mm bore into the liquid.
- Circular shake: dome + petals + offset pins drive a visible spiral vortex;
  powder blooms in turbulent tendrils until evenly mixed and opaque; whey
  never settles, creatine re-suspends.
- Left twist: whole cap unit unscrews as one piece (dial stays captive on the
  collar). Exactly one clean hand may appear for twists; chilled-glass
  condensation is on-brand (fridge at 2–6 °C).
- Loop-friendly: start and end on the same still bottle.

## 10. Global negatives

No loose scoops/shaker balls, no powder tubs, no cold-chain trucks, no
cartoon/stylised rendering, no flavour colour on bottle or wordmark, no
competitor trade dress (Barebells/Quest/Ensure), no Arabic-English mixed
lettering errors — English wordmark JUSTWIST only, no invented certification
marks, no visible brand text unless the asset spec asks for the wordmark.
