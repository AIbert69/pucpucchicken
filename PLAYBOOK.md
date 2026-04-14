# PucPucChicken — Prompts & Workflow
### Step-by-step prompts for editing the site in Claude Code

---

## Setup (Run Once)

### Prompt 1: Clone and baseline

```
Clone the repo at https://github.com/AIbert69/pucpucchicken
Review the full index.html and list every section with its ID.
Take a screenshot of the current live site at pucpucchicken.vercel.app.
Create a git branch called "baseline-backup" so we have a frozen copy.
```

---

## Video Section Workflow

### Prompt 2: Audit the current video section

```
Look at section "03 — See the System" in index.html.
Tell me:
1. What video file is referenced and where is it hosted?
2. Is it autoplay, click-to-play, or embedded?
3. What's the current fallback if the video doesn't load?
4. Screenshot this section so I can see the current state.
Do NOT change anything yet.
```

### Prompt 3: Replace/fix the video

```
Replace the video in section "03 — See the System" with this file: [YOUR VIDEO FILE PATH OR URL]

Requirements:
- Click-to-play with a poster/thumbnail image
- Show a play button overlay on the poster
- Responsive — 100% width, maintain 16:9 aspect ratio
- Fallback text if video can't load
- Do NOT change the section heading, numbering, or any other section
- Do NOT modify the nav, hero, footer, or any CSS outside this section

Show me the exact code change (before → after).
```

### Prompt 4: Verify the video change

```
Screenshot the full page after the video change.
Compare it to the baseline screenshot.
Confirm that ONLY the video section changed.
List any visual differences you see anywhere else on the page.
```

---

## Logo Swap Workflow

### Prompt 5: Swap the logo

```
Replace the logo image with this new file: [YOUR LOGO FILE PATH]

The logo appears in:
1. The header/nav
2. The footer (if present)

Replace it in ALL locations.
Keep the same dimensions, padding, and alignment.
Do NOT change nav links, font sizes, colors, or layout.

Show me the exact code change (before → after).
```

### Prompt 6: Verify the logo swap

```
Screenshot the header and footer after the logo change.
Compare to baseline.
Confirm nothing else shifted — same nav spacing, same footer layout.
```

---

## Asset Swap Workflow (Images)

### Prompt 7: Replace any illustration or image

```
Replace the image in section "[SECTION NAME]" with this new file: [FILE PATH OR URL]

Keep the same:
- Width and height constraints
- Border radius
- Shadow
- Alt text (update if the image content changed)
- Responsive behavior

Do NOT change text, spacing, or layout in this section.
Do NOT touch any other section.

Show me the exact code change.
```

---

## Copy Updates

### Prompt 8: Update text in a specific section

```
Update the copy in section "[SECTION NAME]" only.

New headline: [YOUR TEXT]
New subtext: [YOUR TEXT]
New CTA text: [YOUR TEXT] (if applicable)

Keep ALL styling, fonts, colors, spacing, and layout identical.
Do NOT touch any other section.
Show me the before → after.
```

### Prompt 9: Bulk copy update

```
Here is updated copy for the entire page. Update each section to match.
Do NOT change any styling, layout, colors, or component structure.
Only change text content.

---
HERO:
Headline: [YOUR TEXT]
Subtext: [YOUR TEXT]
CTA: [YOUR TEXT]

SECTION 01 — THE PROBLEM:
Headline: [YOUR TEXT]
Body: [YOUR TEXT]

SECTION 02 — HOW IT WORKS:
[etc.]
---

Show me a git diff after all changes.
```

---

## Adding a New Section

### Prompt 10: Add a section

```
Add a new section between "[PREVIOUS SECTION]" and "[NEXT SECTION]".

Section type: [testimonial / stats bar / partner logos / FAQ / etc.]
Content: [PROVIDE THE CONTENT]

Match the existing design language:
- Same fonts, colors, spacing as the rest of the page
- Same section numbering pattern (increment all following sections)
- Same animation/reveal style if the site uses scroll animations

Do NOT modify any existing sections except to update their numbering.
Show me the new section code AND the updated numbering.
```

---

## Video Strategy Restrictions

**IMPORTANT: Include these restrictions in any video-related prompt.**

```
VIDEO CONTENT RESTRICTIONS — NDA PROTECTED:

DO SHOW:
- Real production floor environment (conveyor, grading station, facility)
- Stylized/animated concept of birds moving through inspection
- Generic data readouts (A/B/C grades, throughput numbers, timestamps)
- Results and value (speed, accuracy, ROI numbers)
- The camera box EXTERIOR only (if showing hardware at all)

DO NOT SHOW:
- Camera box internals or hardware design
- Actual software UI or detection model interface
- Any footage from the duct factory deployment
- Specific system architecture or mounting details
- How the six cameras are positioned or synchronized
- The actual deep learning model output/inference screens
- Any proprietary algorithm visualization

TONE:
- Show WHAT it does and WHY it matters
- Never show HOW it works internally
- Ambiguous enough to protect IP
- Credible enough to prove it's real and deployed
```

---

## Testing & Polish

### Prompt 11: Responsive check

```
Screenshot this page at three breakpoints:
1. Mobile: 375px wide
2. Tablet: 768px wide
3. Desktop: 1440px wide

List any issues:
- Text overflow or truncation
- Images not scaling properly
- Sections that look broken on mobile
- Nav/menu behavior on small screens
- CTA buttons too small to tap on mobile
```

### Prompt 12: Full page review

```
Review the complete page for:
1. Visual consistency — do all sections look like they belong together?
2. Typography hierarchy — heading sizes consistent, body text readable?
3. Color consistency — same palette used everywhere?
4. Spacing rhythm — consistent padding between sections?
5. Broken links or missing assets
6. Accessibility: alt text, contrast, focus states

List each issue with its exact location and recommended fix.
Do NOT auto-fix anything — just report.
```

### Prompt 13: Performance check

```
Analyze index.html for performance issues:
1. Image file sizes — anything over 500KB?
2. Are images optimized (WebP vs PNG/JPG)?
3. Video loading strategy — lazy loaded or blocking?
4. Total page weight estimate
5. Any render-blocking resources?

Recommend fixes but do NOT implement yet.
```

---

## Deployment

### Prompt 14: Deploy to Vercel

```
Commit all changes with a descriptive message.
Push to the main branch on GitHub.
Verify the Vercel deployment triggered.
Once deployed, screenshot the live site and compare to local.
```

---

## Emergency: Something Broke

### Prompt 15: Rollback

```
Something broke. Compare the current code to the baseline-backup branch.
Show me every file that changed and what changed in each.
Ask me which changes to keep and which to revert.
Do NOT auto-revert anything without my confirmation.
```

### Prompt 16: Fix a specific broken element

```
The [DESCRIBE WHAT'S BROKEN] in the [SECTION NAME] section is broken.
It should look like [DESCRIBE EXPECTED BEHAVIOR].

Fix ONLY this issue.
Do NOT change anything else on the page.
Show me the exact code change.
Screenshot before and after the fix.
```

---

## Git Discipline

After EVERY successful change, run:

```
git add -A
git commit -m "[type]: [what changed]"
```

Commit types:
- `asset:` — logo swap, image replacement, video update
- `copy:` — text content changes
- `fix:` — bug fixes, layout repairs
- `add:` — new sections or features
- `style:` — visual polish, animation, spacing
- `perf:` — optimization (image compression, lazy loading)

---

## Prompt Cheat Sheet

| What you want to do | Use Prompt # |
|---------------------|-------------|
| Set up the project | 1 |
| Check what the video section looks like | 2 |
| Replace or fix the video | 3 → 4 |
| Swap the logo | 5 → 6 |
| Replace an image | 7 |
| Update text in one section | 8 |
| Update all copy at once | 9 |
| Add a new section | 10 |
| Test responsive | 11 |
| Full review | 12 |
| Performance check | 13 |
| Deploy | 14 |
| Something broke — investigate | 15 |
| Something broke — fix one thing | 16 |

---

*Use these prompts in Claude Code. One at a time. Verify after each. Commit after each success.*
*Never combine multiple changes in one prompt.*
