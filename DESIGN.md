---
name: Gia Bảo · 206
description: A race bib and its course, worn on asphalt.
colors:
  race-orange: "#ff4d12"
  course-blue: "#4a66ff"
  asphalt: "#18191b"
  asphalt-raised: "#222326"
  tyvek: "#f4f4f0"
  carbon-ink: "#111111"
  ink-soft: "#3a3a38"
  road-paint: "rgba(244, 244, 240, .92)"
  road-paint-dim: "rgba(244, 244, 240, .74)"
typography:
  display:
    fontFamily: "Barlow Condensed, Arial Narrow, sans-serif"
    fontSize: "clamp(8rem, 54vw, 28rem)"
    fontWeight: 900
    lineHeight: 0.8
    letterSpacing: "-0.035em"
    fontFeature: "tnum"
  headline:
    fontFamily: "Barlow Condensed, Arial Narrow, sans-serif"
    fontSize: "clamp(3rem, 9vw, 6rem)"
    fontWeight: 900
    lineHeight: 1.02
    letterSpacing: "-0.01em"
  title:
    fontFamily: "Barlow Condensed, Arial Narrow, sans-serif"
    fontSize: "clamp(2rem, 5vw, 3rem)"
    fontWeight: 900
    lineHeight: 1.05
  lead:
    fontFamily: "Barlow, system-ui, sans-serif"
    fontSize: "clamp(1.25rem, 2.4vw, 1.5rem)"
    fontWeight: 600
    lineHeight: 1.4
  body:
    fontFamily: "Barlow, system-ui, sans-serif"
    fontSize: "1.125rem"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "Barlow Condensed, Arial Narrow, sans-serif"
    fontSize: "0.95rem"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "0.12em"
rounded:
  flag: "3px"
  card: "10px"
  tab: "12px"
  bib: "14px"
  pill: "999px"
spacing:
  gutter: "clamp(16px, 4vw, 48px)"
  leg: "clamp(56px, 10vh, 112px)"
components:
  tear-tab:
    backgroundColor: "{colors.tyvek}"
    textColor: "{colors.carbon-ink}"
    rounded: "{rounded.tab}"
    padding: "18px 28px 22px"
  tear-tab-hover:
    backgroundColor: "{colors.carbon-ink}"
    textColor: "{colors.tyvek}"
  km-flag:
    backgroundColor: "{colors.tyvek}"
    textColor: "{colors.carbon-ink}"
    rounded: "{rounded.flag}"
    padding: "10px 14px 9px"
  km-flag-current:
    backgroundColor: "{colors.race-orange}"
    textColor: "{colors.carbon-ink}"
  skill-chip:
    textColor: "{colors.tyvek}"
    rounded: "{rounded.pill}"
    padding: "12px 16px 11px"
  podium-card:
    backgroundColor: "{colors.tyvek}"
    textColor: "{colors.carbon-ink}"
    rounded: "{rounded.card}"
    padding: "16px 22px 14px"
---

# Design System: Gia Bảo · 206

## Overview

**Creative North Star: "The Race Bib"**

The page is a runner's bib pinned on, then the course run in it. Two materials carry everything: dark, grainy asphalt as the ground, and Tyvek-white bib stock for the objects that sit on it (the bib, km flags, podium cards, the torn-off finish tab). Text on the road is painted on: big, white, condensed, uppercase. Text on Tyvek is printed in carbon ink.

Density is low and the rhythm is vertical. One scroll is one race: a cobalt-blue course line runs down the left edge, an orange runner dot moves along it as you scroll, and each section is a leg marked by a km flag. Hierarchy comes from size, weight and case inside one superfamily (Barlow Condensed for display and labels, Barlow for reading copy), never from extra decoration.

Race-world devices are the native vocabulary and are meant to be reused: pin holes, perforated tear lines with bitten corners, a timing-chip barcode strip, km marker flags, a painted start line, a checkered finish band. The world rejects the dark dev-portfolio look: no avatar hero, no typing effect, no card grid.

**Key Characteristics:**
- Asphalt ground with fine noise; Tyvek objects with a faint fibre texture.
- One condensed sports superfamily; uppercase 900 weight for every heading.
- Orange means "you are here"; blue means "the course".
- Objects sit slightly tilted (-2.2deg to +1deg), as if pinned or dropped by hand.
- Interaction has real physical travel: tabs tug down at the perforation.

## Colors

A near-monochrome road-and-paper palette with two signal colors, each with exactly one job.

### Primary
- **Race Orange** (race-orange): The name band on the bib, the current km flag, the runner dot, focus rings, text selection and the scrollbar thumb. Always marks identity or present position.

### Secondary
- **Course Blue** (course-blue): The course line only. A lighter cobalt chosen so the line holds against asphalt.

### Neutral
- **Asphalt** (asphalt): Page ground, with a 7% white fractal-noise grain. Also the fill of the punched pin holes, so the road shows through the bib.
- **Raised Asphalt** (asphalt-raised): Fill for task boxes in diagrams painted on the road.
- **Tyvek** (tyvek): Bib stock and every object on the road; also the color of headings and solid rules painted on the road.
- **Carbon Ink** (carbon-ink): All text printed on Tyvek; the dark state of tear tabs on hover.
- **Ink Soft** (ink-soft): Secondary labels printed on Tyvek (podium captions).
- **Road Paint** (road-paint): Default text and lead copy on asphalt.
- **Road Paint Dim** (road-paint-dim): Body paragraphs, captions, legends, footer and secondary labels on asphalt.

### Named Rules
**The You-Are-Here Rule.** Orange marks only the name band and the present position (current km flag, runner, focus, selection, scroll thumb). A km flag that is not current stays Tyvek. Never use orange as a general accent, link color or decoration.

**The One Course Rule.** Blue is the course line and nothing else.

## Typography

**Display Font:** Barlow Condensed (with Arial Narrow, sans-serif), weights 500 / 700 / 900
**Body Font:** Barlow (with system-ui, sans-serif), weights 400 / 600
Both self-hosted from `fonts/` with Latin and Vietnamese subsets; the 900 Latin cut is preloaded.

**Character:** A race-number condensed grotesk at every display size, with its non-condensed sibling for long Vietnamese paragraphs so diacritics stay readable.

### Hierarchy
- **Display** (900, clamp(8rem, 54vw, 28rem), 0.8, tabular numerals): The bib number only.
- **Headline** (900, clamp(3rem, 9vw, 6rem), 1.02, uppercase, balanced wrap): Leg titles painted on the road. The bib name band and the finish title use the same 900 uppercase voice at their own clamp sizes.
- **Title** (900, clamp(2rem, 5vw, 3rem), 1.05, uppercase): Entries inside a leg (one row per thing done). Big painted words (Gym, Chạy bộ, podium results) use the same voice up to ~4.8rem.
- **Lead** (Barlow 600, clamp(1.25rem, 2.4vw, 1.5rem), 1.4, max 34ch): The one-sentence summary under each leg title.
- **Body** (Barlow 400, 1.125rem, 1.6, max 62ch): Reading copy, in Road Paint Dim with Tyvek 600 for emphasis.
- **Label** (Condensed 700, 0.95rem, 0.12em tracking, uppercase): Roles, legends, captions on podium cards, footer. Bib tags and meta use the same voice at 0.14em / 0.12em.

### Named Rules
**The One Family Rule.** Every word is Barlow or Barlow Condensed. Condensed for anything shouted, labelled or numbered; Barlow only for sentences.

**The Uppercase Shout Rule.** Headings are 900 uppercase; tracking goes negative only at display sizes (-0.01em to -0.035em) and positive (0.04em to 0.3em) for small labels.

## Layout

A single vertical column that is one race from start to finish. The first viewport is the start corral: the bib centered on asphalt (max 760px wide, tilted -2.2deg) above a 10px painted start line and the word START tracked at 0.3em.

Below it the course: a 6px blue line at `clamp(22px, 9vw, 150px)` from the left edge, content offset to its right, legs up to 1000px wide with leg padding (spacing.leg) top and bottom. Each leg's km flag sits centered on the line, level with the leg title. The page ends with a 36px checkered band, a centered finish title, the torn-off tab, and a footer split left/right.

Horizontal padding uses the shared gutter (spacing.gutter). At 560px and below: the bib band stacks, pin holes shrink to 16px, the chip strip hides, the line moves to 22px, km flags rotate -90deg to run along the line, two-column grids collapse to one, and the horizontal diagram swaps for a vertical one.

## Elevation & Depth

Depth is physical: Tyvek objects lie on the road and cast soft, real shadows; nothing on the asphalt itself is elevated. Pin holes are punched through, with an inset shadow. There are no hard offset shadows.

### Shadow Vocabulary
- **Pinned bib** (`box-shadow: 0 2px 3px rgba(0,0,0,.35), 0 30px 60px -18px rgba(0,0,0,.7)`): The bib.
- **Stamped card** (`box-shadow: 0 2px 3px rgba(0,0,0,.3), 0 18px 34px -16px rgba(0,0,0,.7)`): Podium cards.
- **Flag** (`box-shadow: 0 3px 8px rgba(0,0,0,.4)`): Km flags.
- **Torn tab** (`filter: drop-shadow(0 2px 2px rgba(0,0,0,.35)) drop-shadow(0 16px 18px rgba(0,0,0,.45))`): Masked shapes, where box-shadow would fill the bites.
- **Punched hole** (`box-shadow: inset 0 2px 3px rgba(0,0,0,.6), 0 0 0 1.5px rgba(17,17,17,.18)`): Pin holes.

### Named Rules
**The Paper-On-Road Rule.** Only Tyvek objects cast shadows; every shadow pairs a tight contact shadow with a long soft one.

## Shapes

Soft-cornered paper (bib 14px, tab 12px, card 10px, flag 3px) against hard road paint (straight 10px rules, square line caps). Perforations are 3px dashed borders; tear edges are bitten with 12px radial masks at both corners. Skills are full pills (999px). Solid outlines mean "done"; dashed outlines mean "still in progress". Objects carry a small hand-placed tilt, never more than about 2.2deg at rest.

## Components

### Tear Tab (primary action)
Physical, tug-able, the only button shape in the system.
- **Shape:** Tyvek strip under a 3px dashed perforation, bitten top corners, rounded bottom (tab).
- **Content:** Condensed 900 uppercase label at clamp(1.4rem, 3.4vw, 2rem) with a square-capped 3px SVG arrow; a timing-chip barcode strip on the left (hidden on mobile).
- **Hover:** Inverts to Carbon Ink with Tyvek text; the arrow nudges 3px in its direction.
- **Active:** Gives at the perforation, `translateY(4px) rotate(.8deg)` over .25s on the shared ease-out.
- **Focus:** 3px Race Orange outline, 4px offset (8px when the tab is detached).
- Appears attached to the bib (start) and torn off with drop shadow (finish).

### Km Flag
- **Style:** Tyvek, flag radius, Condensed 900 at clamp(1.1rem, 2vw, 1.5rem), 0.08em tracking, flag shadow, centered on the course line.
- **Current:** Turns Race Orange and scales 1.12 over .35s. On mobile it is rotated -90deg along the line.

### Skill Chips
- **Style:** Pill, 3px Tyvek border, transparent fill, Condensed 700 uppercase at clamp(1.15rem, 2.4vw, 1.45rem).
- **State:** Solid border = used; dashed border = still exploring (with screen-reader text saying so). A legend with matching solid/dashed strokes sits above.

### Cards / Containers (Podium Card)
- **Corner Style:** card radius.
- **Background:** Tyvek with Carbon Ink 900 result and Ink Soft label beneath.
- **Shadow Strategy:** Stamped card (see Elevation).
- **Tilt:** Alternating -1.5deg / +1deg.

### Splits List
Rows separated by 2px rules at 22% Road Paint; the first row opens with a 10px Tyvek rule. Each row: Title, then a Label role line, then body.

### Course Line and Runner (signature)
A 6px Course Blue line; a 26px Race Orange dot with a 6px 22%-orange halo, positioned by scroll on one requestAnimationFrame timeline. The leg whose top has passed mid-viewport is current.

## Do's and Don'ts

### Do:
- **Do** put new content on the course as a leg with a km flag, a 900 uppercase headline and a lead sentence.
- **Do** print on Tyvek in Carbon Ink and paint on asphalt in Tyvek / Road Paint; keep body copy in Road Paint Dim at max 62ch.
- **Do** reuse the race devices (pin holes, perforations, bitten tear edges, chip strip, painted rules, checkered band) for new surfaces.
- **Do** mark honest skill level with solid vs dashed outlines.
- **Do** give every press real travel and honor reduced motion (animations off, diagrams fully drawn).

### Don't:
- **Don't** use Race Orange for anything other than the name band, present position, focus and selection.
- **Don't** introduce a third typeface or system display fonts.
- **Don't** add hard offset shadows or shadows on road-painted elements.
- **Don't** build an avatar hero, typing effect or card grid.
- **Don't** use icon glyphs or emoji; arrows are inline square-capped SVG.
