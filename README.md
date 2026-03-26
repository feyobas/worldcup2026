# The Football Brief — YouTube Shorts Channel

A daily YouTube Shorts channel delivering sharp, stat-driven football content built around the 2026 FIFA World Cup cycle. Every video is 25–45 seconds, AI-produced, and uploaded at 18:00 Turkey time.

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
| Focus | World Cup 2026 players, squads, stats, previews |

---

## Brand Identity

The Football Brief uses a premium newspaper-meets-stadium aesthetic. Think breaking news urgency with Champions League production value.

- **Primary Black:** `#0a0a0a`
- **Antique Gold:** `#c9a84c`
- **White:** `#ffffff`
- **Title Font:** Playfair Display (editorial authority)
- **Stats/Impact Font:** Impact or Oswald (punchy, readable)
- **Logo:** Black circle, antique gold ring border, newspaper masthead typography

Full details in `/brand/brand-guide.md`.

---

## Production Pipeline

Every Short is produced using the following AI-assisted workflow:

1. **Script** — Claude writes a 25–45 sec script following the template
2. **Voice** — ElevenLabs TTS (Charlie or Daniel voice, speed 0.85)
3. **Video** — Kling AI generates cinematic 9:16 football background footage
4. **Assembly** — CapCut: audio + video + auto captions + text graphics
5. **Upload** — YouTube Shorts, daily at 18:00 Turkey time

Full details in `/production/pipeline.md`.

---

## Content Strategy

- **Series-based content** groups related videos for watch time and algorithm performance
- **Topical hooks** tied to current fixtures, transfers, and World Cup qualification
- **30-day rolling calendar** maintained in `/content/content-calendar.md`
- **Active series** tracked in `/content/series-tracker.md`

### Active Series (as of March 2026)
| Series | Videos | Status |
|---|---|---|
| Turkey Playoff Series | 5 | In Progress |
| Brazil Squad Breakdown | 5 | Planned |
| France Full Series | 5 | In Progress |

---

## Folder Structure

```
worldcup2026/
├── README.md                    ← This file
├── brand/
│   └── brand-guide.md           ← Colors, fonts, logo, CapCut text style
├── production/
│   ├── pipeline.md              ← Full AI production workflow
│   ├── script-template.md       ← Script writing guide and format
│   └── capcut-settings.md       ← CapCut project and export settings
├── scripts/
│   ├── short-001-michael-olise.md
│   ├── short-002-neymar-last-dance.md
│   ├── short-003-turkey-romania-playoff.md
│   └── ...                      ← All future scripts numbered sequentially
├── content/
│   ├── content-calendar.md      ← 30-day rolling upload schedule
│   └── series-tracker.md        ← Series status and planning
└── seo/
    └── channel-seo.md           ← Channel description, tags, SEO templates
```

---

## Script Naming Convention

Scripts are numbered sequentially: `short-NNN-descriptive-slug.md`

Example: `short-007-griezmann-france-wc2026.md`

Status options: `DONE` | `IN PROGRESS` | `PLANNED`

---

## Key Principles

- **Hook in 3 seconds.** The first sentence is a bold statement, never a question.
- **One story per video.** No padding, no tangents.
- **Stats make it shareable.** Every Short has at least one surprising number.
- **CTA is always the same.** "Follow The Football Brief." — consistent brand recall.
- **Upload daily without fail.** Consistency beats perfection on Shorts.
