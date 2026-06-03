# Prompt Templates

Fill only the bracketed fields needed for the request. Preserve exact text blocks.

## Front Prompt

```text
Use case: illustration-story
Asset type: cultural tourism postcard front
Primary request: Create a 3:2 horizontal illustrated travel postcard for [province] · [destination] · [month].
Input images:
- Image 1: authoritative IP character identity reference. Preserve its defining face, proportions, colors, and visual personality.
- Image 2, if supplied: approved front-side series style anchor. Match its composition language, paper texture, watercolor detail, and restraint.
Scene/backdrop: [destination landmark and seasonal landscape].
Botanical elements: [seasonal plants and destination-specific natural elements].
IP interaction: [one concrete physical action tied to the setting].
IP styling: [small prop or seasonal accessory, if useful].
Style/medium: refined hand-painted botanical specimen illustration, delicate watercolor and colored-pencil texture, vintage travel postcard warmth, milk-white paper base.
Composition/framing: full scenic composition; landmark in the central background; seasonal botanical branches framing foreground and edges; IP integrated near the right-side focal area without overwhelming the landscape.
Color palette: [season palette].
Text (verbatim): "[province] · [destination] · [Chinese month]"
Text placement: extremely small understated serif specimen-label text at bottom center, never title-sized.
Constraints: IP must visibly touch or manipulate a scene element; preserve IP identity; keep text minimal and exact; no watermark; no unrelated text.
```

## Back Prompt

```text
Use case: illustration-story
Asset type: cultural tourism postcard back
Primary request: Create the matching 3:2 horizontal back side of a vintage cultural tourism postcard for [destination].
Input images:
- Image 1: authoritative IP character identity reference.
- Image 2, if supplied: approved back-side series anchor. Keep its layout stable.
Style/medium: lightly aged warm off-white postcard paper, restrained vintage print texture, refined botanical watercolor ornament.
Composition/framing:
- Left area: four independent spacious lines of Chinese poem text, with generous vertical spacing and no ruled lines behind the poem.
- Upper-left corner: small [botanical element] illustration.
- Upper area: small widely spaced serif "POSTCARD" with a minimal ornament.
- Center: thin vertical divider with a tiny ornament at top and bottom.
- Upper-right: one vertical 3:4 decorative perforated-edge stamp with a miniature [IP interaction] scene.
- Right side below stamp: five thin horizontal address lines.
- Lower-right: small serif "POST CARD".
- Lower center crossing divider: one aged dark-red tilted seal, around 15 degrees.
Seal color: #8B1A1A.
Required text (verbatim):
POSTCARD
[poem line 1]
[poem line 2]
[poem line 3]
[poem line 4]
[destination]
中国邮政 CHINA
80分
[province]
[destination short name]
[PINYIN WITHOUT TONE MARKS]
POST CARD
Constraints: render every required character exactly; preserve spacious layout; keep the stamp as a decorative postcard design; no watermark; no unrelated text.
```

## Targeted Text Retry

```text
Regenerate only the postcard back. Preserve the existing composition, illustration, IP identity, stamp placement, seal position, and warm paper texture. Correct the rendered text exactly. Use only the following verbatim text and do not invent, replace, omit, or repeat any characters:
[exact text block]
```
