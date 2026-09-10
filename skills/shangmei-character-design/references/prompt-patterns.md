# Prompt Patterns

## Default character sheet

```text
CHARACTER ANCHOR:
[anchor]

OUTPUT VARIABLE:
16:9 horizontal character design sheet, pure white background. On the left, one
large front-facing head-and-shoulders portrait showing facial construction, age
markers, hairstyle and headwear clearly. On the right, three full-body views of the
same character arranged front, side, back. Same face, same age, same hair, same
headwear, same clothing, same colors and same body proportions across all views.
Front pose may lightly fold arms; side pose may touch chin or adjust sleeve; back
pose relaxed. Costume structure must remain readable. No extra characters, no text,
no watermark.
```

## Turnaround only

```text
CHARACTER ANCHOR:
[anchor]

OUTPUT VARIABLE:
clean front / side / back full-body turnaround, pure white background, same person in
all three views, stable proportions, stable clothing construction, neutral readable
pose, no cropped feet, no extra props unless requested.
```

## Expression sheet

```text
CHARACTER ANCHOR:
[anchor]

OUTPUT VARIABLE:
head-and-shoulders expression sheet: neutral, slight smile, angry, suspicious,
worried, frightened, sad, surprised, determined. Preserve exact face construction,
age, hair and headwear. No identity drift.
```

## Older version

```text
Preserve the approved character's fundamental face identity, eye spacing, nose,
mouth, hair family, body identity and costume family. Change age only to [target
age]. Update eyelids, eye bags, cheek firmness, nasolabial area, jaw definition,
skin texture, hair graying/hairline when appropriate, hands and posture. Do not make
a completely different person.
```

## Outfit-only edit

```text
Keep the approved character's face, age, hairstyle, headwear unless specifically
changed, body proportions and drawing style exactly consistent. Change only the
outfit to [outfit], using [materials] and [palette]. No face changes, no age changes.
```

## Headwear-only edit

```text
Keep the same character identity, age, face, hairstyle beneath the headwear, body,
clothing and palette. Add/replace only the headwear with [headwear]. It must fit the
historical occupation and not alter the character's face.
```

## Video continuity block

```text
CHARACTER CONTINUITY:
[compact anchor]

LOCK:
same face, same age, same hairstyle, same headwear, same body proportions, same
costume silhouette and same colors. Only expression, gesture and requested action
may change. No identity drift, no costume morphing.
```

## Useful negative components

```text
different person, face drift, age drift, different hairstyle, different headwear,
inconsistent costume, modern fashion, modern makeup, idol-drama face, generic anime
face, 3D render, photorealistic skin, fantasy armor, excessive embroidery, duplicate
character, cropped feet, text, watermark
```