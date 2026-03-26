# CapCut Settings Reference — The Football Brief

This document is your settings reference for every production session. Open it before you open CapCut.

---

## Project Settings

| Setting | Value |
|---|---|
| Resolution | 1080 x 1920 (Full HD vertical) |
| Aspect ratio | 9:16 |
| Frame rate | 30fps (or match source video if 60fps) |
| Color space | SDR (not HDR — YouTube Shorts handles SDR better) |

**How to set:** New Project → select 9:16 → confirm 1080x1920 before importing media.

---

## Timeline Assembly Order

Import and layer in this order (bottom to top on timeline):

1. **Background video clips** (Kling AI exports) — bottom layer
2. **Audio track** (ElevenLabs MP3) — guide for all timing decisions
3. **Color grade / LUT** (optional, see below)
4. **Text graphics** — player name, stat boxes
5. **Auto captions** — always on top, center screen
6. **Channel watermark** — top layer, top-right corner

---

## Auto Captions Settings

| Setting | Value |
|---|---|
| Style | **Bold** preset |
| Position | Center screen — 45–55% from top |
| Max words per line | 3–4 |
| Font size | CapCut Bold default (do not reduce) |
| Animation | Fade or pop-in — avoid karaoke-style word highlight |
| Background | Off (stroke/shadow handles legibility) |

**How to add:** Select audio track → Auto Captions → Style: Bold → Position: drag to center screen.

**Critical:** After auto-generation, review captions for errors. Common misses:
- Player names (Calhanoglu, Arda, Rodrygo — fix manually)
- Numbers spoken as words ("fifteen" should match "15" on stat box)
- Fix timing drift if captions lag more than 0.2 seconds

---

## Player Name Text Graphic

| Setting | Value |
|---|---|
| Font | Impact (or Oswald Bold as fallback) |
| Color | Antique Gold `#c9a84c` |
| Size | ~80–100pt (fill about 60% of frame width) |
| Case | ALL CAPS |
| Letter spacing | 0 to -2 (tight) |
| Position | Lower-center of frame (avoid top 10%, bottom 20%) |
| Shadow | Black, X offset: 4, Y offset: 4, blur: 6, opacity: 60% |
| Stroke | Black stroke, 2–3px |
| Animation in | Fade 0.2s or slide-up 0.2s |
| Animation out | Fade 0.2s |
| Duration on screen | 2.0–3.0 seconds |
| Timing | Appears at 1.5 seconds into video |

**Example text:** `MICHAEL OLISE`

---

## Stats Box Graphic

Build stat boxes using the **Text + Background Shape** method in CapCut:

### Text Settings
| Setting | Value |
|---|---|
| Font | Oswald Bold or Impact |
| Primary number | Large — ~60–70pt, color: Deep Black `#0a0a0a` |
| Label text | Smaller — ~24–30pt below number, same color |
| Alignment | Center |

### Box/Background Shape Settings
| Setting | Value |
|---|---|
| Shape | Rectangle |
| Fill color | White `#ffffff` |
| Border/Stroke | Antique Gold `#c9a84c`, 3–4px |
| Corner radius | 6–8px |
| Padding | ~16px internal on all sides |

### Placement and Timing
| Setting | Value |
|---|---|
| Position | Center-left or center-right of frame, mid-height |
| Duration | 2.0–3.0 seconds |
| Animation in | Fade 0.2s or scale-in 0.2s |
| Animation out | Fade 0.2s |
| Timing | Appears exactly when stat is spoken in audio |

**Example stat box:**
```
┌────────────────────────┐  ← Gold border #c9a84c
│   15                   │
│   Goals — Bundesliga   │  ← Black text on white #ffffff
└────────────────────────┘
```

**Two stat boxes:** Never show both at once. Stat 1 appears, fades out, then Stat 2 appears.

---

## Channel Watermark

| Setting | Value |
|---|---|
| Image | Channel logo (PNG with transparent background) |
| Position | Top-right corner |
| Size | ~10–12% of frame width |
| Opacity | 30–35% |
| Duration | Full video, visible throughout |

---

## Color Grading (Optional but Recommended)

For consistency across all Kling AI clips:

| Setting | Value |
|---|---|
| Brightness | -5 to -10 (slightly darker, more cinematic) |
| Contrast | +10 to +15 |
| Saturation | -5 (slightly desaturated — less "AI generated" look) |
| Temperature | 0 to -5 (slightly cooler) |
| Vignette | Light vignette, 15–20% — focuses attention center |

Apply the same adjustment to all clips in a project for visual consistency.

---

## Transitions

| Use case | Transition |
|---|---|
| Standard clip-to-clip | **Cut** (no transition) — keep it clean |
| Section break (e.g., moving from player profile to stats) | **Fade to black**, 0.3s |
| Re-engagement line moment | **Flash cut** or **zoom cut** — adds energy at 50% mark |
| End of video → CTA | **Fade to black**, 0.5s |

**Rule:** Default to no transition (hard cut). Only add transitions where they serve the pacing.

---

## Pacing Notes

- Average shot length: 3–5 seconds per background clip
- Do not hold on one static clip for more than 6 seconds
- Cut clips on beats in the audio (pauses, emphasis words)
- The re-engagement line at ~50% is a natural cut point — match it with a new clip
- CTA ("Follow The Football Brief") should play over a clean, wide cinematic shot — not a close-up

---

## Export Settings

| Setting | Value |
|---|---|
| Resolution | 1080 x 1920 |
| Frame rate | 30fps (or match project) |
| Format | MP4 |
| Codec | H.264 |
| Bitrate | High — at least 8 Mbps (select "High quality" preset) |
| Audio | AAC, 192kbps minimum |
| HDR | Off |

**File size expectation:** 40-second Short at these settings ≈ 40–70 MB

**Export filename:** `short-NNN-final.mp4`

---

## Common Mistakes to Avoid

- Captions sitting at the very bottom (YouTube UI covers it) — always center screen
- Stats box overlapping the speaker's face in background video
- Text too small to read on mobile — test at 50% zoom to simulate phone screen
- Forgetting to review auto-caption accuracy for player names
- Exporting in portrait but wrong resolution (confirm 1080x1920, not 720x1280)
- Background clips being horizontal (landscape) — always verify Kling AI output is 9:16 before import
