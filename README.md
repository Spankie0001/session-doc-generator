# session-doc-generator

**Live tool:** https://spankie0001.github.io/session-doc-generator

A prompt engineering tool for Suno AI that generates recording session 
documents — using real studios, engineers, and gear — to pattern-match 
against Suno's training data and produce dramatically more accurate, 
consistent, and genre-specific outputs than plain language prompting.

---

## What is Session Doc Prompting?

Session Doc Prompting is an advanced prompt engineering technique for 
Suno AI in which the style and lyrics fields are formatted as synthetic 
recording session documents rather than plain language genre descriptors 
or song lyrics.

Instead of writing "dark reggae with industrial textures," a Session Doc 
encodes the same intent as gear lists, studio names, engineer credits, 
signal routing maps, and disc/sample loadouts — mimicking the metadata 
format of a real analog recording session.

**How it works:** Suno's training data includes recorded music, production 
documentation, and text associated with specific studios, engineers, gear, 
and artists. When a prompt references real named entities — a specific 
mixing console, a real studio, a known engineer or producer — Suno 
pattern-matches against that training data and pulls the associated sonic 
characteristics rather than interpreting a generic description.

The result is more precise and consistent genre targeting than plain 
language prompting achieves.

**Validated:** An audio engineer listening blind to Suno output generated 
using this technique identified the SSL 4000G console by ear from the 
sound alone. The gear database is not cosmetic — it influences output at 
a level trained professionals can hear.

---

## The Tool

The Session Doc Generator is a single self-contained HTML file that runs 
in any browser with no install, no account, and no internet required at 
runtime.

### Features

- **32 genres** with fully filtered databases per genre
- **1,500+ database entries** covering real recording history
- Studios, engineers, producers — all genre-matched to real recording history
- Full signal chain: console, tape machine, preamp, amplifier, keys/synth, 
  drum machine, reverb, delay, modulation, drive, compression, bass
- **Disc Map** — 5-disc sample loadout system including 
  `Disc_A: In-Context_Vocal_Samples` vocal retrieval mechanism
- **Disc E** — configurable turntable/scratch layer with 6 vocabulary styles:
  Wu-Tang/Hip-Hop DJ, Industrial/Techno Cut, Jazz/Bebop, 
  Reggae/Dub Selector, IDM/Glitch, Golden Era Hip-Hop
- Hook & harmonic character — scale, interval, call/response, tension
- Texture and edit bed multi-select
- Arrangement structure — 16 sections individually toggleable
- Genre, mood, and instrument exclusion tags
- Generates two outputs: **Style prompt** (under 1000 chars) and 
  **Lyrics field routing map** (under 3000 chars)
- Live character counts with warnings
- One-click copy for both fields
- Dark studio aesthetic

### How to Use

1. Open the tool at https://spankie0001.github.io/session-doc-generator
2. Select your primary genre — all dropdowns filter to match
3. Work through the tabs: Session → Discs → Hook & Texture → Structure → Exclusions
4. Click **Generate Session Doc**
5. Copy both outputs directly into Suno's Style and Lyrics fields
6. *(Optional)* Run [AuralScript](https://github.com/Spankie0001/auralscript) 
   on the output to measure how close you landed against your reference 
   track — then adjust your Session Doc to close the gap
7. Iterate and refine

---

## Session Doc Format

A Session Doc typically contains:

```
[SESSION: studio_name_year]
[Engineer: name — producer: name]
[Gear: console, tape_machine, preamp, amp, drum_machine, keys,
reverb, delay, mod, drive, comp, bass]
[Disc_A: In-Context_Vocal_Samples]
[Disc_B: genre_sample_source — characteristics]
[Disc_C: genre_sample_source — characteristics]
[Disc_D: genre_sample_source — characteristics]
[Disc_E: scratch_vocabulary — techniques]
[Hook: scale, interval, call, response, tension]
[Bass: instrument_and_character]
[Texture: layered_sonic_descriptors]
[Edit_Bed: production_fx_continuous]
-exclusion -exclusion -exclusion
```

The lyrics field runs parallel — a pure routing map with 0% actual 
lyrics, using section tags to encode arrangement, transitions, and 
mix automation cues instead of words.

---

## Key Principles

- Name real studios, real engineers, real gear — specificity is the mechanism
- Append `-inspired` to artist/album references to avoid Suno's copyright filter
- `Disc_A: In-Context_Vocal_Samples` is the single most powerful tag — 
  it instructs Suno to pull vocal character from its training memory 
  without requiring lyrics
- Exclusion tags are load-bearing — use them aggressively to block genre drift
- Style prompt hard limit: 1000 characters
- Lyrics field limit: approximately 3000 characters
- Suno coherence typically holds for 2–2.5 minutes — front-load important sections

---

## Origin & Credit

The Session Doc Prompting technique was pioneered by **DJ Dogman**, a 
creator on the Suno platform, who demonstrated that encoding style prompts 
as DJ routing sheets and session metadata produced dramatically more 
accurate results than conventional prompting. The `Disc_A: In-Context_Vocal_Samples` 
tag in particular is his key contribution — it functions as a training 
memory retrieval instruction rather than a content descriptor.

This tool was developed by **Spankie0001** to systematize and extend the 
technique with a genre-filtered database of real recording history, making 
Session Doc Prompting accessible without requiring deep knowledge of studio 
gear and production history.

As of April 2026, this is the only publicly available tool built around 
Session Doc Prompting methodology.

---

## Roadmap

- [ ] Preset save/load — name and recall session configurations
- [ ] Multi-genre blending — hybrid filtered lists for fusion tracks
- [ ] AuralScript integration — paste acoustic analysis numbers, auto-select matching gear
- [ ] Export to .txt
- [ ] Polka / Weird Al mode
- [ ] Morrey/Smith Cure mode — 1987 UK post-punk shimmer pop

---

## Related Project

**AuralScript** — a Python tool that converts audio files into 
LLM-readable text schemas for AI music analysis. Use it to measure 
how close Suno's output landed against your reference track, then 
adjust your Session Doc to close the gap.

https://github.com/Spankie0001/auralscript

---

## License

MIT License — Copyright (c) 2026 Spankie0001

Permission is hereby granted, free of charge, to any person obtaining 
a copy of this software to use, copy, modify, merge, publish, distribute, 
sublicense, and/or sell copies of the Software, subject to the following 
conditions: The above copyright notice and this permission notice shall 
be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.
