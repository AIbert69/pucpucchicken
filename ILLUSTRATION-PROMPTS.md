# PucPucChicken — Illustration Prompt System

Prompt workflow for generating consistent illustrations for the PucPucChicken site. Built to match the existing `hero_illustration.png` style: isometric, flat vector, editorial, industrial documentary.

**Recommended tools:** Recraft (best for consistent vector sets), Midjourney (with `--sref` to hero_illustration), Nano Banana image-to-image mode.

---

## Style Lock (paste before every prompt)

```
Isometric technical illustration, clean flat vector line art, editorial 
industrial documentary style. Limited palette: cream background #F5EFE0, 
dark forest green #3D5A3E, charcoal ink #2A2A25, muted bone white #FAF8F2. 
Flat shading only — no photorealism, no gradients beyond subtle flat tone, 
no text, no logos, no UI, no people. Generous negative space. 
Composition: single focal subject, 3:4 portrait aspect. 
Matches an isometric ceiling-mounted poultry inspection system aesthetic.
```

---

## NDA Restrictions (ALWAYS APPLY)

```
NEVER show:
- Camera box internals or hardware schematics
- Any UI, software screens, or detection model output
- Proprietary algorithm visualization
- Identifiable facility or branding

KEEP AMBIGUOUS:
- Exact sensor arrangement
- Software stack
- Integration details
```

---

## Block Structure

Every illustration prompt = `Style Lock` + `Scene Block` + `Realism Tail`.

### Realism Tail (paste after every scene block)

```
High detail, crisp linework, subtle paper grain, clean composition with 
ample whitespace. No text anywhere. Portrait 3:4. Renders that look 
like a single frame from a printed technical manual — not a photograph.
```

---

## The Four Cards (How It Works section)

### Step 01 — Capture

```
Scene: Six ceiling-mounted industrial cameras arranged in a hexagonal 
array above a single shackle on an overhead poultry conveyor line. Six 
thin green light cones converge on one point — the bird. Emphasis on 
the geometry of synchronized multi-angle capture. Isometric 3/4 view. 
Subtle scan grid on the floor below. No bird is distressing or graphic.
```

### Step 02 — Detect

```
Scene: Close isometric view of one bird silhouette on a shackle with a 
soft green detection overlay — abstract keypoint dots and faint bounding 
brackets on the surface, hinting at AI inspection without showing any 
screen or UI. Faint neural lattice lines in the background. Focus on 
the moment of analysis.
```

### Step 03 — Grade

```
Scene: Three glowing labeled tags — A, B, C — floating above a conveyor 
as birds pass a checkpoint. Each letter rendered in the same editorial 
flat style as the rest of the scene. One tag is active (solid green), 
the other two muted. Emphasis on the decision moment / classification.
```

### Step 04 — Route

```
Scene: Isometric conveyor system with a mechanical diverter gate splitting 
one lane into three parallel lanes (A, B, C channels). A small PLC cabinet 
on the side with a single green status LED. An EtherNet cable runs from 
the cabinet to the gate. Focus on precision industrial routing.
```

---

## Variation Workflow

Once a card is approved, iterate on the **render**, not a new scene. Change **one axis at a time**.

### Change only color palette
```
Keep the scene composition, linework, and subject identical. Keep every 
element in place. Change only the accent color from dark forest green 
#3D5A3E to [NEW HEX]. All other colors and shading stay the same.
```

### Change only camera angle
```
Keep every element of the scene, materials, and palette identical. 
Change only the camera angle to [top-down / straight elevation / 
low-angle isometric]. No other changes.
```

### Tighten composition
```
Keep the scene and style identical. Remove peripheral detail and tighten 
composition around the primary subject. Increase negative space. No new 
elements.
```

---

## File Naming Convention

Save approved renders as:
```
assets/step_01_capture.png
assets/step_02_detect.png
assets/step_03_grade.png
assets/step_04_route.png
```

Tell Claude "wire them in" and the HTML update will happen.

---

## Additional Site Imagery (future)

| Slot | Prompt seed |
|------|-------------|
| Problem section hero | "Operator silhouette at grading station, fatigued posture, blurred conveyor, muted palette, editorial" |
| ROI background | "Abstract flowing data lines suggesting value recovery, dark green on cream, no numbers" |
| Advantages icons | Use Heroicons or Lucide instead — consistent icon set beats AI for small marks |

---

## Tips

1. Always test one card first. If it matches the hero style, lock the seed and run the others.
2. Recraft's "Vector Illustration" mode gives the cleanest, most print-ready output.
3. Midjourney: add `--sref [hero_illustration url] --sw 400` to pull the style strongly.
4. Keep prompts short. Long prompts produce busy images. If it's too busy, ask for "more negative space, minimal composition."
5. Export at 2x the display size (e.g. 1200x1600 for cards shown at 600x800).
