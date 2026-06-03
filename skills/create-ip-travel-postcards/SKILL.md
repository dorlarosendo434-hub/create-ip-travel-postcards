---
name: create-ip-travel-postcards
description: Generate a coordinated front-and-back cultural tourism postcard series that combines any user-provided IP character with a destination and season. Use when users ask for IP travel postcards, destination postcards, cultural tourism postcard illustrations, 景点明信片, 文旅明信片, IP角色结合景点, 正反面明信片, or a multi-month postcard series rendered with GPT Image 2.
---

# Create IP Travel Postcards

Create a 3:2 landscape postcard pair: a scenic illustrated front and a traditional postcard back. Preserve the supplied IP character while making it physically interact with the destination.

Read [references/visual-rules.md](references/visual-rules.md) before generating. Read [references/prompt-templates.md](references/prompt-templates.md) when composing prompts.

## Collect Inputs

Require:

- IP character reference image
- destination name and location: province plus city or region
- recommended month
- 2-5 destination keywords

Optional:

- IP nickname
- user-written four-line poem
- existing approved front or back from the same series
- multiple destination-month entries for a later batch

Ask only for missing required inputs. Use simplified Chinese unless the user requests another script.

## Choose The Image Path

Target GPT Image 2 and a 3:2 landscape output. For direct API hosts, use `gpt-image-2`, `size: 1536x1024`, and `quality: high`.

For Codex:

1. Use the installed `imagegen` skill and the built-in `image_gen` tool for normal generation.
2. Load local input images with `view_image` before generating so they are visible in context.
3. If the user requires strict API-level model selection or explicit parameters, follow the `imagegen` skill's CLI fallback instructions for `gpt-image-2`. Do not silently switch models.

For another host:

1. Use its GPT Image 2 generation tool or API adapter.
2. Pass the original IP reference first.
3. Pass the approved front or back series anchor second when available.
4. If reference images, size, or quality are unsupported, state the limitation before generation.

Do not claim that a host supports a parameter unless its actual tool schema exposes it.

## Create The First Sample Pair

Generate one front and one back before any batch.

### Prepare The Poem

If the user supplies a poem, keep it unless it breaks the constraints. Otherwise write a four-line short poem:

- Prefer exactly 7 Chinese characters per line.
- Include destination imagery and a seasonal signal.
- Make line 3 an IP interaction or movement in the scene. Do not force a fixed character name.
- Prefer a restrained travel-afterglow ending such as `不思归`, `不知归`, or `不思迁`.
- Use common Chinese characters. Avoid rare characters, variant forms, and wording likely to render incorrectly.
- If a long destination name makes seven characters awkward, use a familiar short destination name and tell the user.

### Generate The Front

Use the original IP reference as the primary character anchor. Use the front prompt template.

The character must touch or manipulate a scene element: sit on a branch, hold a flower, touch snow, collect leaves, trail a hand in water, soak in a hot spring, run through grass, or perform another destination-specific action. Do not place the character beside the scenery as a detached sticker.

### Generate The Back

Use the original IP reference and the back prompt template. Render all text inside the image with GPT Image 2. Do not add deterministic SVG, Canvas, or HTML text overlays unless the user later asks for them.

Validate the rendered text visually. If the poem, label, stamp, seal, or postcard text has incorrect characters:

1. Retry once with a targeted prompt emphasizing the exact verbatim text.
2. If poem characters still fail, rewrite the poem with simpler common characters and regenerate the back.
3. Tell the user when the poem changed.

### Present For Approval

Show:

- front image
- back image
- final poem as plain text
- chosen IP interaction
- color palette
- any text retry or poem rewrite

Do not start a multi-entry batch until the user approves the first sample pair or explicitly asks to skip approval.

## Continue As A Series

After approval:

- Keep the original IP reference as the first reference for every image.
- Use the approved front as the front style anchor.
- Use the approved back as the back style anchor.
- Keep the back layout stable across the series.
- Keep the seal dark red `#8B1A1A`.
- Vary the interaction naturally by destination and avoid repeating an action when a good alternative exists.
- Keep the fourth-line emotional tone consistent across the series.

For a batch, generate fronts in bounded parallel and backs in bounded parallel only after the anchors exist. Use at most 10 concurrent jobs when the host supports concurrency; otherwise process sequentially.

Group results by destination and month.

## Validate Every Pair

Check:

- output is 3:2 landscape
- IP identity remains recognizable
- IP physically interacts with the destination
- front landmark, seasonal botany, and palette match the requested destination-month
- bottom front label is small and understated
- back follows the reference composition
- poem has four readable lines and uses common characters
- required postcard, stamp, and seal text is legible
- seal uses dark red rather than the seasonal palette
- no watermark or unrelated text appears

Retry only the failed side with a targeted correction.

## Reference Assets

The bundled reference images are layout and mood examples:

- `assets/reference-front-linzhi-march.png`
- `assets/reference-back-linzhi-march.png`

Inspect them when creating the first sample of a new series. Do not treat their frog character, Linzhi destination, peach blossoms, or poem as fixed content.
