# PucPucChicken — Project Brief

## What This Is
An interactive online presentation deck for PucPucChicken, an AI-powered poultry grading system built by Singh Automation, LLC (Portage, MI). This is NOT a traditional website — it's a sales tool disguised as a landing page.

## Live URL
https://pucpucchicken.vercel.app

## GitHub Repo
https://github.com/AIbert69/pucpucchicken

## Tech Stack
- Plain HTML (single index.html file)
- Tailwind CSS via CDN
- Deployed on Vercel (auto-deploys from GitHub main branch)
- No framework, no build step

## Target Audience
- Plant managers and QA directors at poultry processing facilities
- Decision-makers evaluating automation for grading lines
- These are industrial buyers, not consumers — they want ROI numbers, not flashy design

## Primary CTA
"Request a Plant Walk" — a free, no-pitch facility visit

## Brand Identity
- **Tone:** Industrial, serious, confident. Not startup flashy.
- **Colors:** Cream (#F5EFE0), Ink (#2A2A25), Green (#3D5A3E)
- **Fonts:** Playfair Display (headings) + DM Sans (body)
- **Feel:** Editorial, premium, like a high-end industrial catalog

## Current Page Structure
1. **Navbar** — Text-based logo + nav links + CTA button
2. **Hero** — "Every bird graded in 185 milliseconds" + illustration
3. **Stat Cards** — 185ms, 6 cameras, 87-94% accuracy, 24/7
4. **Background Text** — YIELD · COMPLIANCE · LABOR SAVINGS
5. **The Problem (Section 01)** — "Your operators are defaulting to B" + loss stats
6. **How It Works (Section 02)** — 4 cards: Capture → Detect → Grade → Route
7. **Compatibility Strip** — EtherNet/IP, Marel, Meyn, BAADER, Gainco
8. **ROI Section** — "Pays for itself in 3-5 months"
9. **Video Section (Section 03)** — "The 87% Ceiling" video (currently broken — no video file in repo)
10. **Advantages (Section 04)** — 6 feature cards
11. **Conveyor Illustration** — Full-width technical illustration
12. **CTA (Section 05)** — "Let us walk your line" + 4-step process
13. **Trust Strip** — Singh Automation credit
14. **Footer** — Contact, links, CTA

## What Needs Work
- [ ] Logo swap — replace text-based nav logo with new PNG logo image
- [ ] Video — create and embed the hybrid video (see VIDEO-STRATEGY.md)
- [ ] Video file missing — The_87__Ceiling.mp4 is referenced but not in the repo
- [ ] All nav links go to # anchors — working correctly for single-page
- [ ] Mobile responsiveness check needed
- [ ] Performance audit (image sizes, loading)

## NDA / IP Restrictions
- System was first deployed in a duct factory under NDA
- CANNOT show: camera internals, software UI, detection model, duct factory footage
- CAN show: concept animations, production floor environment, data readouts, exterior hardware
- See VIDEO-STRATEGY.md for full restrictions

## Assets in This Folder
- `assets/logo.png` — New PucPucChicken logo (400px, transparent PNG)
- `assets/logo_large.png` — Large version (800px)
- `assets/hero_illustration.png` — Isometric camera box illustration
- `assets/conveyor_illustration.png` — Technical conveyor illustration
- Video file: TBD (needs to be created per VIDEO-STRATEGY.md)

## How to Deploy
```bash
git add -A
git commit -m "description of change"
git push origin main
# Vercel auto-deploys from main branch
```

## Rules
1. One change at a time
2. Screenshot before and after every change
3. Commit after every successful change
4. Always specify what NOT to change in prompts
5. Read this brief at the start of every session
