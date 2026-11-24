# Workflow & Process Redesign — Vanderbilt Learning Series

Single-page interactive classroom experience (Learning on Demand). Live at
https://futureslearninghub.github.io/Workflow/ (GitHub Pages, `gh-pages` branch —
publish with `git branch -f gh-pages main && git push -f origin gh-pages`).

Sister programs: AI_Classroom (AI Basics), AI-Advanced (AI 201),
Difficult_Conversations, Coaching-for-Performance, Emotional-Intelligence;
catalog at FuturesLearningHub/FLH-Learning-Library-. Same engine, same standing principles.

## Standing design principles (do not regress these)

1. **Simulators, practice, and play throughout.** Every teaching section
   has an interaction; the Redesign Lab is the signature piece, Guess the
   Number is the skeptic-converter, and the private workflow mapper feeds
   every later section.
2. **A reason and facilitation behind every activity.** Learner-visible
   "Why this matters" lines; activities labeled As a group / On your own
   with steps, timings, and solo variants.
3. **Every section facilitatable, learning validatable.** ATD runbook in
   `facilitator/notes.json`. Kirkpatrick: L1 fist-to-five, L2 recap mapped
   to objectives, L3 redesign card + 7-day pulse + 30-day re-poll; the
   headline L3 metric is mapping sessions actually held.
4. **Facilitator edition is generated, never hand-edited** — run
   `python3 tools/build-facilitator.py` after ANY change to index.html or
   notes.json. Its QR encodes the LEARNER url.
5. **Privacy by design — this course runs on real team workflows.**
   Workflows and roles, never people's names; the mapper and redesign card
   are private (nothing saved or sent) and must SAY so in learner-visible
   copy. Never add telemetry, storage, or sharing to the personal
   exercises.
6. **The traffic light is shared with the AI courses and never
   contradicted:** green = public or generic, yellow = internal, approved
   VU tools only, red = private information about people, never. The light
   outranks the draft-verify-decide pattern in all copy.
7. **Stay tool-agnostic.** The course teaches the assignment pattern, not
   any product. No tool names, no vendor pitches; capability claims carry
   cited, linked sources (McKinsey State of AI; Metaintro for the
   manager's-core-job framing).
8. **Brand: Vanderbilt FLH system.** Black #1C1C1C / white / flat gold
   #CFAE70; Libre Caslon Display headlines (one italic word), Inter body,
   Antonio eyebrows; motion ≤400ms; real VU lockups (authorized use only).
9. **No frameworks.** One CSS file, one JS file, vendored QR lib,
   self-hosted fonts; the hero uses the gold particle canvas (no video).

## Layout (14 slides)

Welcome/QR (privacy norm) → Hero (5 objectives) → Agenda →
01 The case for redesign (Guess the Number) → manifesto ("AI doesn't fix a
broken process. It speeds it up.") → 02 See the work as a process (step
trainer + private mapper) → 03 Draft, verify, decide (assignment trainer +
traffic light) → 04 Design the verify (check trainer + rubric) → 05 The
Redesign Lab (graded 4-step rebuild) → 06 Bring the team along
(announcement trainer + pilot standard) → Recap quiz → Capstone Redesign
Card → Glossary → Closing (footer lives inside the closing slide).

## Editing map

- Copy: `index.html` · Recap: `QUESTIONS` in `assets/js/main.js`
- Trainers: `makeTrainer` configs (statGuess, stepSpot, assignStep,
  checkRate, sayJudge)
- Workflow mapper: `wfMap` block · Redesign Lab: `SLOTS` + reaction tiers
- Capstone maps: `PRACTICE` / `NOT` / `WHEN` in main.js
- Runbook: `facilitator/notes.json` (timing must sum: Full 90 / Core 60)
- Citations to keep honest: McKinsey State of AI survey (88% adoption,
  ~6% high performers, redesign = strongest EBIT factor, 2.8x more likely
  / 55% vs 20%, ~21% redesigned any workflow), Metaintro (manager's new
  core job), automation bias (framing only, no invented statistics).
