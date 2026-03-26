# The Football Brief — YouTube Shorts Channel

A daily YouTube Shorts channel delivering punchy, stat-driven football analysis built around the 2026 FIFA World Cup. Every video is 25–45 seconds, AI-produced, and uploaded at 18:00 Turkey time.

---

## Channel Overview

| Field | Detail |
|---|---|
| Channel Name | The Football Brief |
| Handle | @FootballBrief |
| Format | YouTube Shorts (vertical, 9:16) |
| Length | 25–45 seconds per video |
| Upload Schedule | Daily at 18:00 Turkey time (UTC+3) |
| Language | English |
| Focus | World Cup 2026 players, squads, stats, match previews |

---

## Brand Identity

The Football Brief uses a premium newspaper-meets-stadium aesthetic. Breaking news urgency with Champions League production value. Every frame should feel like a headline worth stopping for.

- **Primary Black:** `#0a0a0a` — backgrounds, overlays, text boxes
- **Antique Gold:** `#c9a84c` — player names, borders, logo ring, emphasis elements
- **White:** `#ffffff` — body stats text, caption text, contrast elements
- **Title Font:** Playfair Display — editorial authority, serif, used in logo and series cards
- **Stats/Impact Font:** Impact or Oswald — condensed, maximum legibility at speed
- **Logo:** Black circle with antique gold ring border, newspaper masthead typography in Playfair Display

Full visual specifications and CapCut graphic settings in `/brand/brand-guide.md`.

---

## Production Pipeline

Every Short follows a five-step AI-powered workflow:

| Step | Tool | Output |
|---|---|---|
| 1. Script | Claude | Finished script file in `/scripts/` |
| 2. Voice | ElevenLabs (Charlie or Daniel, speed 0.85, stability 0.40, clarity 0.80) | MP3 voiceover |
| 3. Video | Kling AI (9:16 vertical, cinematic football visuals) | Background MP4 clips |
| 4. Assembly | CapCut (audio + video + Bold auto captions + text graphics) | Final 1080x1920 MP4 |
| 5. Upload | YouTube Studio | Scheduled at 18:00 Turkey time |

Full workflow details, prompts, and settings in `/production/pipeline.md`.

---

## Content Strategy

Content is organized into series. Each series runs 5–7 videos and follows a consistent arc — squad intro, player profiles, prediction. Series structure improves watch time and algorithm performance.

### Active Series (March 2026)

| Series | Videos | Status |
|---|---|---|
| Turkey Playoff Series | 5 | In Progress |
| France Full Series | 5 | In Progress |
| Brazil Squad Breakdown | 6 | Planned |

### Planned Series

England Breakdown, Argentina Series, Germany Analysis, Dark Horses, Bracket Predictions.

Full series status and planning in `/content/series-tracker.md`.
30-day upload schedule in `/content/content-calendar.md`.

---

## Folder Structure

```
worldcup2026/
├── README.md                         ← This file — project overview
│
├── brand/
│   └── brand-guide.md                ← Colors, fonts, logo, CapCut graphic specs
│
├── production/
│   ├── pipeline.md                   ← Full AI production workflow (5 steps)
│   ├── script-template.md            ← Script rules, structure, timing marks, examples
│   └── capcut-settings.md            ← CapCut project, text, caption, export settings
│
├── scripts/
│   ├── short-001-michael-olise.md    ← DONE — France WC2026
│   ├── short-002-neymar-last-dance.md ← DONE — Brazil/Neymar
│   ├── short-003-turkey-romania-playoff.md ← IN PROGRESS — Turkey playoff
│   └── short-NNN-slug.md             ← Future scripts numbered sequentially
│
├── content/
│   ├── content-calendar.md           ← 30-day upload calendar (Mar 26 – Apr 24)
│   └── series-tracker.md             ← All series: status, video list, notes
│
└── seo/
    └── channel-seo.md                ← Channel description, tags, title formula, templates
```

---

## Script Naming Convention

Scripts are numbered sequentially: `short-NNN-descriptive-slug.md`

Example: `short-014-griezmann-france-wc2026.md`

Status options: `DONE` | `IN PROGRESS` | `PLANNED`

---

## Key Principles

- **Hook in 3 seconds.** The first sentence is a bold statement, never a question. Never "Did you know...?"
- **One story per video.** No padding, no tangents, no trying to cover everything.
- **Stats make it shareable.** Every Short has at least 2 real, surprising numbers.
- **Re-engagement at 50%.** A pivot line halfway through resets the viewer's attention.
- **CTA is always the same.** "Follow The Football Brief." — exact wording, every video.
- **Upload daily without fail.** Consistency beats perfection on Shorts.

---

## Quick Start: Producing a New Short

1. Pick the next video from `/content/content-calendar.md`
2. Write script using `/production/script-template.md` — save in `/scripts/`
3. Paste script into ElevenLabs → export MP3 (Charlie or Daniel, speed 0.85)
4. Generate background clips in Kling AI (9:16 vertical, cinematic prompt)
5. Assemble in CapCut: audio + video cuts + Bold auto captions + text graphics
6. Export 1080x1920 H.264, minimum 8 Mbps
7. Upload to YouTube, use SEO template from `/seo/channel-seo.md`
8. Schedule for 18:00 Turkey time
9. Update script status to DONE and mark calendar entry accordingly
