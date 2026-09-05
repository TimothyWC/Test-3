# GTA Web Works: design plan

Written before any code, per the distinctive-web-design skill.

## Subject
A two-person web studio in Vaughan, Ontario (Tim: design and code; Daniel: outreach and client contact), building custom sites for local businesses that have great reviews and no website. Audience: owners of auto shops, trades, clinics and landscapers in York Region and Toronto, usually on a phone, skeptical of agency quotes. Primary job: make them trust the studio enough to call.

## Real inventory
- Names: Tim, Daniel. Phone (647) 636-1859. Email team.gtawebworks@gmail.com. Vaughan.
- Prices: $400 / $750 / $1,200 CAD, paid once. Optional $25/month maintenance.
- Process: reply within a day, free 20-minute call, quote, 50% to start, first draft in 3 to 5 days, revisions, balance before launch, handoff.
- Work: two live concept builds (Cornerstone Interlock & Landscape Design, Vaughan; Good Guys Computer, Richmond Hill). Labelled "concept build" everywhere; neither was commissioned.
- Photos: six real Cornerstone project photos (granite steps, interlock walkway, pergola).
- Gaps: no screenshots of the two builds yet (live-screenshot fallback plus an honest empty state), no founder photos, no client-written reviews, no logo mark. None of these are faked. There is no reviews section.

## World list
Google Maps listings with the "Add website" button; 4.8 stars and dozens of reviews; the client's old Facebook page; strip plazas along Highway 7 with backlit sign boxes at night, some lit, some dark; work trucks with vinyl lettering; hand-lettered price boards; black granite steps and wet interlock in daylight; a pergola at golden hour; a chandelier lit in a foyer; business cards on a corkboard; two students at a kitchen table at 11pm, a phone glowing; e-transfer, a quote on a clipboard; the 407 at night, headlights, sodium lights; brick subdivisions; the oldest storefronts with gold-leaf lettering on glass, the look of a business that has been there thirty years; "an agency quoted me $5,000."

## The one idea
The site is a strip plaza at night. The businesses with a website are the lit sign boxes; the ones without are dark. The hero is a before-and-after slider where you drag the light across: on the left, the unlit listing ("Your business. 4.8 stars. Website: none."); on the right, the lit site. Everything after the hero is either night (the studio, the work, lit like sign boxes) or day (pricing and process, on the limestone of the client's own stonework).

Competitor swap: a rival could not use the lit/unlit plaza without the concept becoming theirs; the copy carries the price and the place. Owner pride: yes. Free tokens: hero (the slider), dominant colour (night), accent (sign-box amber), display type (established-storefront lettering), motion (the light comes on once).

Warmth check: colour field (night, then limestone) yes; human presence (first-person copy, names, a real stone photo) yes; scale (the hero headline and the Didone prices) yes; texture (only the real photo) yes; play (the slider) yes. Five of five.

## Tokens

Colour (provenance in comments):
- --night #0e1620, dominant: the sky over Highway 7 at 11pm, blue-black with warmth from the plaza lights
- --night-2 #16212e: the inside of a lit sign box, one step up
- --glow #fff2dc: backlit sign white, text on night
- --glow-muted #a6b0bd: unlit lettering, secondary text on night
- --amber #ffb54a, accent: sodium light, sign-box amber; the slider's light; buttons; focus
- --day #ede7db, secondary field: limestone in daylight, the client's stone steps
- --day-2 #e3dccd: limestone, shadow side
- --ink #171a1f: wet asphalt, text on day
- --ink-muted #6b665d: secondary text on day

Ratio: night about 60%, limestone about 30%, amber under 10% (handle, buttons, links). No pure black, no pure white, no purple, no cream-plus-terracotta, no decorative gradients. The only gradients are light: the glow around the slider handle, and the dusk fade between the night sections and the daylight photo.

Type:
- Display: Bodoni Moda (variable, optical sizes 6 to 96, weights 400 to 900). Reason: the high-contrast lettering on the oldest storefronts, jewellers and bank branches, gold leaf on glass; the look of having been there thirty years, which is what the studio sells. Counter-expectation move: fashion-house type, plumber's copy.
- Text: Radio Canada (variable width 75 to 100, weights 300 to 700). Reason: the Canadian broadcaster's typeface; local, plain, public, clearly different in kind from a Didone. Condensed width for captions, the way sign lettering condenses.
- Scale: 14, 16, 18, 20, 24, 32, 44, 60, hero clamp(44px, 7.2vw, 100px). Display at opsz 96 for the hero and prices, 48 for section heads, 24 for the wordmark.
- Not used: Inter, Instrument Serif, DM Sans, JetBrains Mono, Space Grotesk, Playfair, Fraunces or anything else on the tell list. No mono anywhere. No italic accent words. No caps eyebrows.

Layout:
Night header (sticky, solid). Hero: headline and one paragraph left (5 columns), the slider right (7 columns) bleeding past the container edge; on mobile the slider goes full-bleed under the headline. Then the work: two lit panels, the first image-left, the second image-right, so the page does not read as a template. Then a quiet six-item list of what every site includes, two columns, no boxes. Then a full-bleed daylight photo of the client's stone with a dusk fade at the top and a fade into limestone at the bottom, one line over it: "Their work. Our website." Then the day: pricing as a price list with Didone prices at scale, the process as a real numbered sequence. Then night again: who is building it, with one line at display size. Footer.

Grid breaks: the slider bleeds right; the daylight photo is full-bleed; the pull line in the "who" section sits in the right column at display size. Nothing rotated, nothing overlapping for effect.

```
+------------------------------------------------------------+
| GTA Web Works        Work Pricing About Contact  (647) ...  |  night
+------------------------------------------------------------+
| Great reviews.        | [ dark listing | LIT SITE ]->bleed  |
| No website.           |   Your business|  screenshot        |
| We fix the second     |   4.8 stars    |                    |
| part.                 |   Website: none|                    |
| $400 to $1,200...     |  Before   (o)  After               |
| [Call] [See the work] |  Drag the light across.            |
+------------------------------------------------------------+
| Two builds so far.                                          |
| [ lit panel: Cornerstone ]   text                           |
| text                          [ lit panel: Good Guys ]      |
+------------------------------------------------------------+
| What every site comes with      (six items, two columns)    |
+------------------------------------------------------------+
| [ full-bleed daylight stone photo ]  "Their work. Our..."   |  dusk -> day
+------------------------------------------------------------+
| Pricing            Basic ......................... $400     |  limestone
|                    Standard ...................... $750     |
|                    Premium ..................... $1,200     |
| How it works       1. 2. 3. 4. 5.                           |
+------------------------------------------------------------+
| Who's building it  "Tim builds it. Daniel picks up."        |  night
| footer                                                      |
+------------------------------------------------------------+
```

Motion:
- The one moment: on first load the headline settles in (three elements, 80ms stagger, transform and opacity), then the slider's light sweeps from fully dark to about 42% over 1.2s with a weighted ease-out. Once. After that the slider is the visitor's to drag.
- Feedback: links underline in amber, buttons swap fill in 200ms, the slider knob scales while held, details open with a height transition, form fields glow on focus.
- Reduced motion: no sweep, no stagger; the slider starts at 42%; everything else instant.

Imagery and texture:
- Real screenshots of the two builds at images/work/cornerstone.jpg and images/work/goodguys.jpg when Tim adds them; until then a live-screenshot fallback, and if that fails, an honest lit panel with the site's name and link. Never a broken icon.
- One real Cornerstone photo as the full-bleed daylight break, captioned as the client's work. A second Cornerstone photo on the work page.
- No texture overlays. The only texture is in the photos.

Copy voice:
Two founders talking. Plain, specific, a bit of attitude, no sales language, no em dashes, straight quotes, sentence case. Age stays on the About page. Concept builds are labelled. Sample: "Great reviews. No website. We fix the second part." / "Tim builds it. Daniel picks up." / "You pay once. It's yours after."

## Default check
- Dark plus warm accent plus serif could be any luxury restaurant template. What makes it this site: the lit/unlit plaza concept, the slider as an interface object rather than decoration, the limestone day section motivated by the client's stone, the Canadian text face, the plain copy with prices in it, honest concept labels, a real photo as the bridge between night and day. Removed from an earlier draft: gold as the accent (reads as cheap luxury; amber reads as light), hairline rules everywhere (broadsheet tell), centred hero (template), pill "Available" status, any eyebrow labels.
- Bodoni Moda: would not be chosen for any brief; chosen here for the storefront-lettering reason and the counter-expectation of luxury type over trades copy.
- Slider: requested by the owner, and it is the argument of the business, not an effect.
- All five pages share the system: night intros, limestone for anything that is paperwork (pricing, the contact form), night for the studio and the work.
