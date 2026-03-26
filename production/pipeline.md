# Production Pipeline — The Football Brief

Every Short follows this exact five-step workflow. Do not skip steps. Do not change the order. Consistency is what keeps quality high at daily volume.

---

## Step 1: Script (Claude)

**Tool:** Claude (claude.ai or API)
**Time required:** 5–10 minutes
**Output:** Finished script file in `/scripts/`

### Process
1. Open the script template at `/production/script-template.md`
2. Choose the topic from the content calendar at `/content/content-calendar.md`
3. Prompt Claude with the template structure and topic context
4. Review output for: hook strength, stat accuracy, sentence rhythm, CTA
5. Save as `short-NNN-slug.md` in `/scripts/` with status `DONE`

### Script Specs
- **Duration target:** 25–45 seconds (optimal: 38–42 seconds for retention)
- **Word count:** 90–130 words (at 0.85 speed ElevenLabs, ~3 words/sec)
- **Hook:** Bold statement in first 3 seconds — first 8–12 words
- **No questions** as hooks — statements only
- **CTA:** Always "Follow The Football Brief" — last 3 seconds

### Claude Prompt Template
```
Write a 40-second YouTube Shorts script for The Football Brief.
Topic: [TOPIC]
Follow this structure:
- Hook (3 sec): bold statement, no question
- Body (30 sec): 2 surprising stats, short punchy sentences
- Re-engagement line at 50% mark
- CTA (3 sec): "Follow The Football Brief"
Total: 90-120 words. Tone: direct, confident, no fluff.
```

---

## Step 2: Voice (ElevenLabs)

**Tool:** ElevenLabs (elevenlabs.io)
**Time required:** 2–3 minutes
**Output:** `.mp3` audio file

### Voice Settings
| Setting | Value |
|---|---|
| Voice | Charlie **or** Daniel |
| Speed | 0.85 |
| Stability | 0.40 |
| Clarity / Similarity Boost | 0.80 |
| Style | 0 (keep neutral for sports commentary feel) |

### Voice Choice Guide
- **Charlie** — slightly warmer, works well for player profile pieces and human-interest angles
- **Daniel** — more authoritative, works well for tactical breakdowns and high-stakes match previews
- Both voices work at 0.85 speed — this slows delivery just enough to feel deliberate and premium

### Process
1. Paste the final script into ElevenLabs text box
2. Select voice (Charlie or Daniel)
3. Apply settings above
4. Generate and listen through once
5. If pacing feels off on a specific word, use SSML pauses: `<break time="0.3s"/>`
6. Download as `.mp3`
7. File naming: `short-NNN-audio.mp3`

### Common Fixes
- If a word is mispronounced, respell it phonetically (e.g., "Calhanoglu" → "Cal-han-oh-loo")
- If energy drops mid-script, split into two ElevenLabs generations and join in CapCut
- Keep all audio files in a local `audio/` folder outside this repo (file size)

---

## Step 3: Background Video (Kling AI)

**Tool:** Kling AI (klingai.com)
**Time required:** 5–15 minutes (generation time varies)
**Output:** Vertical MP4 video clip(s)

### Generation Settings
| Setting | Value |
|---|---|
| Aspect Ratio | 9:16 (vertical) |
| Duration | 5–10 seconds per clip (loop or extend in CapCut) |
| Mode | Standard or Pro (Pro for hero shots) |
| Style | Cinematic, photorealistic |

### Prompt Principles
- Always specify **9:16 vertical format** in the prompt
- Specify **cinematic** and **slow motion** or **dynamic** based on the mood
- Describe action without naming real players (AI licensing issue)
- Use atmospheric and environmental descriptions for better results

### Example Prompts by Content Type
**Player profile:**
`Cinematic slow-motion vertical 9:16 video, professional footballer in navy blue kit controlling ball with chest, stadium lights, shallow depth of field, golden hour lighting, ultra HD`

**Match preview:**
`Cinematic vertical 9:16, two football teams walking out of tunnel into packed stadium, dramatic low angle, floodlights, fog effect, slow motion, photorealistic`

**Stats/analysis:**
`Cinematic vertical 9:16, close-up of football hitting back of net in slow motion, crowd blurred in background, golden stadium lighting, dramatic, photorealistic`

### Process
1. Generate 2–3 clips per video (variety for cuts)
2. Download all clips
3. Review: check for AI artifacts, ensure correct orientation
4. File naming: `short-NNN-bg-01.mp4`, `short-NNN-bg-02.mp4`

---

## Step 4: Assembly (CapCut)

**Tool:** CapCut (desktop or mobile)
**Time required:** 15–25 minutes
**Output:** Exported `.mp4` ready for YouTube

### Assembly Order
1. **New project** — 1080x1920, 9:16
2. **Import** background video clips and audio `.mp3`
3. **Place audio** on timeline first as your guide track
4. **Cut and arrange** background clips to match audio length
5. **Add auto captions** — Bold style, center screen position
6. **Add text graphics** — player name (gold Impact/Oswald) and stat boxes per brand guide
7. **Add channel watermark** — small logo, top-right, 35% opacity
8. **Review full playback** — check caption sync, text timing, no dead air
9. **Export** (see settings below)

### Detailed CapCut Settings
See `/production/capcut-settings.md` for full settings reference.

### Timing Guide for Text Graphics
- Player name graphic: appears at 1.5 seconds, stays for 2–3 seconds
- Stat box 1: appears when first stat is spoken, stays 2–3 seconds
- Stat box 2: appears when second stat is spoken, stays 2–3 seconds
- All text: fade in 0.2s, fade out 0.2s — never hard cuts on text

---

## Step 5: Upload (YouTube)

**Tool:** YouTube Studio
**Time required:** 5 minutes upload + scheduling
**Upload time:** 18:00 Turkey time (UTC+3) daily

### Upload Checklist
- [ ] Title follows SEO formula (see `/seo/channel-seo.md`)
- [ ] Description uses template with timestamps, hashtags, and tags
- [ ] Tags added (default tags + video-specific tags)
- [ ] Category: Sports
- [ ] Made for kids: No
- [ ] Thumbnail: auto-selected or custom still from video
- [ ] Scheduled for 18:00 Turkey time
- [ ] Shorts label confirmed (YouTube auto-detects 9:16 under 60s)

### Why 18:00 Turkey Time?
- Covers peak engagement for Turkey/Middle East audience (early evening)
- Reaches Western Europe at 16:00 CET — early evening scroll time
- UK audience at 15:00 — post-work browsing window
- US East Coast: 10:00 AM — morning commute

---

## Quality Control Checklist

Before exporting, run through this checklist:

- [ ] Audio is clear, no clipping, no silence gaps
- [ ] Captions are accurate and synced (spot-check 5 random words)
- [ ] No text is obscured by video UI elements (like subscribe button area)
- [ ] Player name graphic appears at correct moment
- [ ] Stats are factually correct (cross-check with script)
- [ ] CTA at the end is audible and visible
- [ ] Video is exactly 9:16, under 60 seconds
- [ ] Export is 1080x1920, H.264, minimum 8 Mbps bitrate

---

## Estimated Total Production Time

| Step | Time |
|---|---|
| Script | 5–10 min |
| ElevenLabs audio | 2–3 min |
| Kling AI video | 10–15 min |
| CapCut assembly | 15–25 min |
| Upload + scheduling | 5 min |
| **Total** | **37–58 min** |

Target: under 45 minutes per video at full speed.
