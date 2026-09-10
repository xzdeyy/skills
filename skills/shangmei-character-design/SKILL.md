---
name: shangmei-character-design
description: >
  Design original characters in the visual language of classic Chinese hand-drawn
  animation, with strong identity consistency, believable age, occupation-driven
  wardrobe, anti-same-face rules, turnaround sheets, expression sheets, outfit
  variants, reference-image refinement, and production-ready character prompts.
---

# Shangmei-style Character Design

Use this skill when the user wants to create, refine, or preserve an original
character inspired by classic Chinese hand-drawn animation aesthetics, especially
ancient Chinese townspeople, merchants, farmers, scholars, constables, magistrates,
women, girls, elders, innkeepers, gamblers, servants, wealthy households, and folk-
tale or zhiguai characters.

The goal is NOT to copy a specific existing film character. The goal is to inherit
traditional Chinese 2D animation design language while creating a new, independent
character identity.

Load these reference files when needed:

- `references/anchor-system.md`
- `references/prompt-patterns.md`
- `references/age-and-face.md`
- `references/occupation-wardrobe.md`
- `references/examples.md`

## Core objective

The highest priority is CHARACTER CONSISTENCY plus BELIEVABLE IDENTITY.

A good result must look like a real person of this age, social class, occupation,
and life history who happens to be designed as a classic Chinese 2D animation
character.

Do not default to young, beautiful, fashionable, idol-like characters. Avoid modern
idol-drama faces, influencer faces, Korean-style pointed jaws, generic anime youth
faces, modern makeup, xianxia costume excess, game-character armor language, and
luxurious studio costumes for ordinary people.

## Default visual target

Unless the user asks otherwise, use:

- classic Chinese hand-drawn animation aesthetics
- 1980s Chinese 2D cel-animation feeling
- traditional Chinese animation character design
- clean hand-drawn black outlines
- rounded, natural contour lines
- cel-style flat colors
- low-saturation traditional palette
- restrained gongbi / light-color-painting influence
- slight paper texture and vintage animation grain
- readable silhouette and grounded human proportions
- non-photorealistic, non-3D, non-modern-anime look

Describe the visual language rather than demanding an exact copy of any specific
existing film or copyrighted character.

## Inputs

Only ask for missing information when it materially changes identity. If the user
provides only one sentence, infer sensible defaults instead of blocking progress.
Useful inputs: name/codename, gender, exact age or range, region/period, occupation,
social class, economic condition, personality, physical condition, story role,
must-keep traits, reference images, and requested output.

## Design reasoning order

identity / occupation
→ age
→ living environment
→ economic condition
→ personality
→ physical state
→ face shape
→ facial features
→ age markers
→ hair
→ headwear / accessories
→ clothing structure
→ fabric quality
→ palette
→ footwear
→ body build
→ posture / habitual gesture
→ unique identifiers
→ anti-same-face comparison
→ final anchor
→ requested output prompt

Do not jump directly from “merchant” to a random robe color.

## Character Anchor

Create an immutable anchor before generating any reusable character prompt.

```text
CHARACTER ANCHOR:
[name/codename], [age], [gender presentation], [historical/social identity],
[economic condition], [face shape], [brow shape], [eye shape/spacing], [nose],
[mouth], [skin/age details], [hair silhouette], [headwear], [body build],
[posture], [signature clothing silhouette], [fabric/material], [main palette],
[signature accessory/prop if any], [classic Chinese hand-drawn animation target]
```

Then separate variables:

```text
OUTPUT VARIABLE:
[expression], [pose/action], [allowed outfit changes], [camera/framing],
[background], [layout], [lighting if needed], [output format]
```

Never casually rewrite the anchor.

## Hard identity locks

Unless the user explicitly requests a redesign, keep stable: face silhouette, eye
spacing and shape, brow architecture, nose, mouth, hair silhouette, age band, body
proportions, signature headwear, costume silhouette, main palette, and style target.
Allowed to vary: expression, gesture, small pose variation, camera angle, requested
outfit variant, background, and scene lighting.

## Age engine

Use `references/age-and-face.md`. Do not represent age only by gray hair. Age must
affect face volume, eyelids/eye bags, nasolabial area, cheek firmness, jaw definition,
skin texture, hairline/graying when appropriate, hands, posture, and movement
impression. If exact age is supplied, respect it. A 45-year-old must not read as 25.

## Anti-same-face system

When multiple characters exist in one project, compare at minimum: face shape,
eyebrows, eyes/spacing, nose, mouth, chin/jaw, hair silhouette, facial hair, body
build, posture, clothing silhouette, and palette. For major recurring characters,
ensure at least five meaningful differences from the closest existing character.
Do not solve difference only by changing clothing color.

## Occupation-driven wardrobe

Use `references/occupation-wardrobe.md`. Wardrobe must communicate occupation +
class + age + climate + daily activity. Prefer coarse cloth, cotton-linen, plain
cotton, worn but serviceable cloth, and restrained silk only when status supports it.
Avoid unnecessary gold trim, giant embroidery, fantasy belts, shoulder armor,
floating ribbons, court dress for commoners, and decorative overload.

## Palette system

Default toward low-saturation traditional colors: gray blue, indigo, earth yellow,
rice white, gray brown, tea brown, brick red, dark green, bean green, smoke blue,
muted ochre, old red. Separate major characters by palette without making the cast
rainbow-like.

## Standard production sheet

When the user does not specify layout, default to:

- 16:9 horizontal canvas
- pure white background
- LEFT: large front-facing head-and-shoulders detail portrait
- RIGHT: same character in three full-body views: front, side, back

All four depictions must be the SAME PERSON: same age, face structure, hairstyle,
headwear, clothing, palette, and body proportions. Right-side poses may be slightly
natural instead of rigid mannequin poses but must not hide costume construction.
Suggested gestures: front lightly folded arms; side touching chin/adjusting sleeve;
back relaxed.

## Reference-image workflow

If the user uploads a character image, preserve only what the user wants preserved.
For an original redesign, intentionally rework several facial dimensions: face
proportions, brows, eyes, nose, mouth, chin/jaw. Do not mechanically copy a famous
character. If the user asks to edit the same original user-provided character,
preserve identity and change only the requested feature.

## Output modes

### Quick mode

Trigger for requests such as “直接给提示词”, “画一下”, “直接生成”, or “按这个做人物设定图”. Do the design reasoning internally and output only the production prompt, or perform the image generation/edit if available.

### Full design mode

Return:

```text
【人物定位】
姓名：
性别：
年龄：
身份：
经济状况：
性格关键词：

【外貌】
脸型：
眉毛：
眼睛：
鼻子：
嘴：
肤色/皮肤状态：
年龄特征：

【头部】
发型：
头饰：

【身体】
身高感觉：
体型：
姿态：

【服装】
上衣：
下装：
腰部：
鞋：
材质：
主色：
辅色：

【人物辨识点】
1.
2.
3.

【CHARACTER ANCHOR】
...

【人物设定图生成提示词】
...
```

## Supported user commands / intents

Interpret naturally; slash syntax is optional.

- `/character` — create a new character from a short description
- `/sheet` — default left portrait + right turnaround sheet
- `/turnaround` — front / side / back full-body turnaround
- `/expressions` — expression sheet while preserving identity
- `/older [age]` — age the same character without redesigning identity
- `/younger [age]` — younger variant while preserving recognizability
- `/outfit [description]` — change clothing only
- `/hat [description]` — change/add headwear only
- `/variant` — new face for the same occupation/archetype; do not clone identity
- `/lock` — return a compact reusable Character Anchor
- `/compare` — compare two characters for same-face risk
- `/video-anchor` — return a compact continuity block for image-to-video workflows

## Quality bar

Reject or retry when: age reads wrong; sheet panels look like different people;
face or body drifts; occupation is not visually readable; ordinary people look like
xianxia/game characters; clothing changes without request; three-view costume
construction disagrees; main cast shares the same face architecture; or the result
copies a recognizable existing animation character too closely.