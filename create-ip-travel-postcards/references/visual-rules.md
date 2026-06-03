# Visual Rules

## Front

Use `../assets/reference-front-linzhi-march.png` as the baseline composition reference.

- Format: 3:2 landscape postcard, warm milk-white paper base.
- Build a complete scenic illustration rather than a rigid left-right split.
- Place the destination landmark in the central background.
- Frame the edges and foreground with detailed seasonal botanical illustration.
- Use watercolor, colored pencil, and vintage botanical specimen textures.
- Place the IP character near the right side or another balanced focal point.
- The IP must interact physically with the setting and remain clearly recognizable.
- Add a small seasonal prop only when it supports the scene.
- Keep the bottom-center label extremely small and restrained: `省份 · 景点名 · X月`.
- Keep the landscape dominant. The IP is an integrated story point, not a sticker or oversized mascot.

Season palette defaults:

| Season | Palette |
| --- | --- |
| Spring | soft pink, tender green, pale sky blue |
| Summer | leaf green, lake blue, warm sunlight |
| Autumn | ochre, gold, brick red, muted green |
| Winter | ice blue, snow white, pale gray, restrained warm accents |

## Back

Use `../assets/reference-back-linzhi-march.png` as the baseline layout reference.

- Format: 3:2 landscape postcard on lightly aged warm off-white paper.
- Left side: four spacious poem lines, no ruled writing lines behind them.
- Upper-left corner: a small seasonal botanical branch.
- Upper area: small widely spaced serif `POSTCARD` lettering with a minimal ornament.
- Center: thin vertical divider with small ornaments at both ends.
- Upper-right: vertical 3:4 perforated decorative stamp.
- Stamp image: miniature IP interaction scene based on the destination.
- Stamp text: destination name at top; `中国邮政 CHINA` and `80分` at bottom.
- Right side below stamp: five thin address lines.
- Lower-right: small serif `POST CARD`.
- Lower center crossing the divider: aged dark-red seal, around 15 degrees tilted.
- Seal text: province, destination short name, and pinyin without tone marks.
- Seal color: fixed `#8B1A1A`.

## Text Reliability

GPT Image 2 renders all text directly. Improve the odds of clean output:

- Put required text in a separate verbatim block in the prompt.
- Prefer common simplified Chinese characters.
- Keep labels short.
- Avoid uncommon place-name variants when a familiar short name is acceptable.
- Inspect the image after generation.
- Retry a failed side with only one focused correction.
- If poem text repeatedly fails, simplify the poem before regenerating.

## Series Anchors

The bundled images are only first-series visual references. After the user approves a new front and back:

- Replace the baseline references with the approved front and back as generation anchors.
- Keep the original IP reference first in the reference list.
- Keep front and back anchors separate.
