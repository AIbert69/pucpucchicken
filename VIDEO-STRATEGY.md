# PucPucChicken — Video Creation Prompts
### Prompts for generating video content (AI video tools: Runway, Sora, Kling, Pika, etc.)

---

## Video Strategy: The Hybrid Approach

The video is split into THREE layers that get edited together:

| Layer | What it shows | How it's made |
|-------|--------------|---------------|
| Layer 1: Real Environment | Production floor, conveyors, grading station | Real footage you've already shot |
| Layer 2: Concept Animation | Birds moving through inspection, data flowing, grades assigned | AI-generated or motion graphics |
| Layer 3: Data Readouts | A/B/C grades, throughput, timestamps on screens | Screen recordings or animated overlays |

---

## NDA RESTRICTIONS — APPLY TO ALL PROMPTS

```
NEVER INCLUDE IN ANY VIDEO:
- Camera box internals or hardware design
- Actual software UI or detection model
- Any footage from the duct factory deployment
- How cameras are positioned or triggered internally
- Deep learning model output screens
- Proprietary algorithm visualization
- Any identifiable client facility without permission

ALWAYS KEEP AMBIGUOUS:
- The exact mechanism of detection
- The number/arrangement of sensors
- The software stack
- Integration specifics
```

---

## Layer 1: Real Environment Footage (What You Film)

### Shot List — Film These Yourself

```
SHOT 1 — ESTABLISHING WIDE
Poultry processing facility exterior or interior wide shot.
Shows scale of operation. No proprietary equipment visible.
Duration: 3-5 seconds

SHOT 2 — CONVEYOR LINE
Overhead conveyor with birds moving through.
Focus on the SPEED and VOLUME — show how fast birds move.
No inspection hardware visible.
Duration: 3-5 seconds

SHOT 3 — GRADING STATION (HUMAN)
Human operators at a grading station making visual calls.
Shows the PROBLEM — humans squinting, fatigued, making quick decisions.
Duration: 3-5 seconds

SHOT 4 — SHIFT CHANGE / FATIGUE
Operators at end of shift. Tired. The accuracy problem is visual.
Duration: 2-3 seconds

SHOT 5 — CAMERA BOX EXTERIOR ONLY (OPTIONAL)
If you want to show the physical hardware — EXTERIOR ONLY.
Mounted on ceiling, clean industrial look. No internals.
Duration: 2-3 seconds

SHOT 6 — PLC / CONTROL PANEL
Generic shot of industrial control panel or PLC cabinet.
Shows this integrates with existing plant infrastructure.
Duration: 2-3 seconds
```

---

## Layer 2: Concept Animation Prompts

### For AI Video Tools (Runway Gen-3, Sora, Kling)

**Prompt 1 — Hero/Opening Animation**
```
Industrial poultry processing conveyor belt, birds moving rapidly 
on overhead shackle line, clean modern factory environment, 
soft cool lighting, shallow depth of field, slight slow motion, 
cinematic 4K, professional industrial documentary style, 
no text overlays, no people visible
```

**Prompt 2 — AI Scanning Concept (Abstract)**
```
Abstract visualization of light scanning across a surface, 
clean geometric lines sweeping left to right, data points 
appearing as the scan passes, dark background with teal and 
white accent lighting, futuristic but industrial feel, 
minimal and elegant, no text, smooth camera movement
```

**Prompt 3 — Grading Classification (Data Flow)**
```
Minimalist animation of objects moving along a conveyor line, 
each object gets tagged with a glowing label (A, B, or C) 
as it passes through a scanning zone, clean dark background, 
industrial color palette (dark gray, teal accent, white text), 
smooth motion, professional motion graphics style
```

**Prompt 4 — Diverter/Routing**
```
Industrial conveyor system with automated gates or diverters 
routing products into three separate lanes, mechanical precision, 
smooth robotic movement, factory automation aesthetic, 
overhead camera angle, clean lighting, no branding visible
```

**Prompt 5 — Speed/Throughput (185ms concept)**
```
Extreme close-up of a digital timer or counter rapidly 
incrementing, numbers changing in milliseconds, industrial 
digital display aesthetic, dark background with bright 
numerical readout, sense of speed and precision, 
data visualization style
```

**Prompt 6 — 24/7 Operation**
```
Time-lapse style animation of a factory production line running 
continuously, day turning to night and back to day through 
windows, conveyor never stopping, steady rhythm, 
industrial documentary feel, cinematic lighting transitions
```

---

## Layer 3: Data Overlay Prompts

### For Motion Graphics (After Effects, Canva, or AI tools)

**Overlay 1 — Live Grading Dashboard**
```
Create a minimal dashboard overlay showing:
- Bird count: rapidly incrementing number
- Current grade: "A" in green, cycling occasionally to "B" in yellow
- Throughput: "185ms avg"
- Accuracy: "99.2%"
- Uptime: "24/7"

Style: Dark semi-transparent background, monospace font, 
teal accent color (#00BFA5), minimal borders, 
positioned in lower-third or side panel
```

**Overlay 2 — Grade Distribution Bar**
```
Animated horizontal bar chart showing grade distribution:
- Grade A: 72% (teal/green bar)
- Grade B: 23% (yellow bar)  
- Grade C: 5% (red bar)

Bars animate in from left, numbers count up.
Clean, minimal, dark background.
```

**Overlay 3 — ROI Counter**
```
Animated counter showing:
"Revenue recovered: $___"
Number counts up from $0 to $1,300,000
with dollar formatting ($1.3M)
Subtitle: "Annual savings at 100K birds/day"

Style: Large bold number, small subtitle, 
dark background, white text, teal accent
```

**Overlay 4 — Before/After Split**
```
Split screen comparison:
LEFT: "Human Grading" — 87% accuracy, inconsistent, 
shifts in quality shown as fluctuating line graph
RIGHT: "AI Grading" — 99.2% accuracy, flat consistent line

Clean divider in center, labels at top.
Industrial color palette.
```

---

## Storyboard: Suggested Edit Sequence

```
[0:00 - 0:03]  FADE IN — Wide shot of poultry facility (Layer 1, Shot 1)
[0:03 - 0:06]  Conveyor line, birds moving fast (Layer 1, Shot 2)
[0:06 - 0:09]  Human operators grading — the problem (Layer 1, Shot 3)
[0:09 - 0:11]  Text overlay: "Human accuracy caps at 87%" (Layer 3)
[0:11 - 0:14]  AI scanning animation — light sweeping (Layer 2, Prompt 2)
[0:14 - 0:17]  Grading classification — A/B/C tags appearing (Layer 2, Prompt 3)
[0:17 - 0:19]  Speed counter — 185ms (Layer 2, Prompt 5)
[0:19 - 0:22]  Diverter routing birds to correct lanes (Layer 2, Prompt 4)
[0:22 - 0:25]  Dashboard overlay — live stats (Layer 3, Overlay 1)
[0:25 - 0:28]  Before/After accuracy comparison (Layer 3, Overlay 4)
[0:28 - 0:31]  ROI counter — $1.3M recovered (Layer 3, Overlay 3)
[0:31 - 0:34]  24/7 operation time-lapse (Layer 2, Prompt 6)
[0:34 - 0:37]  Camera box exterior on ceiling (Layer 1, Shot 5) — OPTIONAL
[0:37 - 0:40]  End card: PucPucChicken logo + "Request a Plant Walk"

TOTAL: ~40 seconds
```

---

## Video Specs for Web

```
Format: MP4 (H.264)
Resolution: 1920x1080 (16:9)
Frame rate: 30fps
Bitrate: 8-12 Mbps (quality) or 4-6 Mbps (web-optimized)
Audio: Optional — subtle industrial ambient or no audio
File size target: Under 15MB for fast web loading
Poster image: First frame or custom thumbnail (1920x1080 JPG)
```

---

## Tools You Can Use

| Tool | Best For | Cost |
|------|----------|------|
| Runway Gen-3 | Layer 2 animation prompts | $12-76/mo |
| Kling AI | Realistic industrial footage | Free tier available |
| Pika | Short animated clips | Free tier available |
| Sora (OpenAI) | High-quality cinematic clips | ChatGPT Plus |
| CapCut | Editing all layers together | Free |
| DaVinci Resolve | Professional editing + overlays | Free |
| Canva Video | Simple data overlays | Free/Pro |
| After Effects | Layer 3 motion graphics | Adobe CC |

---

## Quick Start Tonight

1. Gather your real footage clips (Layer 1)
2. Pick ONE AI video tool and generate Layer 2 clips using the prompts above
3. Edit them together in CapCut or DaVinci Resolve
4. Add data overlays (Layer 3) — even simple text overlays work
5. Export as MP4, under 15MB
6. Use the website workflow prompts to swap it into the site

---

*Remember: Show WHAT it does, not HOW it works. Ambiguity protects the IP.*
