# Workflow & Process Redesign · Redesign the Work, Then Add the AI

An interactive, single-page teaching site on the highest-impact managerial
AI skill the research keeps pointing at: mapping how a team's work actually
flows and deciding, step by step, where AI drafts, where a human verifies,
and where a human decides (the draft-verify-decide pattern). A **Learning
on Demand** program: the facilitator projects it while learners scan a QR
code and work every exercise on their own devices, or share the link for
self-paced review. Private by design: every exercise runs on workflows and
roles (never names) and nothing typed is saved or sent anywhere.

Part of the Vanderbilt Learning Series. Catalog:
[Course Library](https://flh-learning-library.vercel.app/) ·
Sister programs: [AI Basics](https://futureslearninghub.github.io/AI_Classroom/),
[Emotional Intelligence](https://futureslearninghub.github.io/Emotional-Intelligence/)

- **Learner edition:** https://futureslearninghub.github.io/Workflow/
- **Facilitator edition:** https://futureslearninghub.github.io/Workflow/facilitator/

## Running it

Plain HTML/CSS/JS, no build step:

```bash
python3 -m http.server 8000
```

## What it teaches (6 sections)

1. The case for redesign: McKinsey's State of AI numbers (88% adoption,
   ~6% high performers, redesign as the strongest EBIT factor, 2.8x)
2. See the work as a process: step maps and the four step types (gather,
   transform, judge, commit), with a privately mapped real workflow
3. Draft, verify, decide: the per-step assignment pattern, bounded by the
   shared AI traffic light (green / yellow / red)
4. Design the verify: automation bias, rubber stamps, and the verifier's
   rubric (named owner, real sources, logged reject path)
5. The Redesign Lab: rebuild the weekly client report step by step and see
   how the design performs at week four
6. Bring the team along: the pilot standard, honest hours, and the
   announcement line judged as a design artifact

Ends with a scored recap, the **Redesign Card capstone** (one workflow, one
draft step, one named failure mode, one dated team mapping session), a
flip-card glossary, and a commitment close. `worksheet.html` mirrors the
capstone on paper; `cheatsheet.html` is built to sit next to the whiteboard
during the mapping session.

## The interactive tools

| Slide | Tool | What learners do |
|---|---|---|
| The case | **Guess the number** | Call four McKinsey findings before the reveal; missed guesses stick |
| The map | **Name the step** | Tag five real work moments as gather, transform, judge, or commit |
| The map | **Map one workflow** | Privately write their workflow, its grind step, and its judgment step |
| The pattern | **Assign the step** | Give five real steps their draft / verify / decide assignment |
| The verify | **Rate the check** | Call five setups: real verification, rubber stamp, or wrong-sized check |
| The team | **Judge the announcement** | Call five pilot announcement lines: good setup, fear or hype, or vague |
| The lab | **The Redesign Lab** | Redesign the Monday report step by step and run four simulated weeks |
| Recap | **Scored quiz** | 6 questions mapped to the objectives |
| Capstone | **My Redesign Card** | Build and copy a dated, private redesign commitment |

## Instructional design

- **Bloom's ladder:** objectives run Explain → Map/Identify → Apply
  (assignment) → Design/Evaluate (verification) → Build/Commit (Create).
- **Kirkpatrick:** L1 fist-to-five at close; L2 inline checks + recap;
  L3 redesign card + 7-day pulse + 30-day re-poll (templates on the
  facilitator briefing slide). The headline L3 metric: mapping sessions
  actually held.
- **Adult learning:** learners bring one real repeating workflow
  (pre-work), every exercise runs on their own material held privately,
  and the capstone ships as a dated 30-minute team mapping session.
- **Privacy by design:** workflows and roles, never names; the mapper and
  redesign card state explicitly that nothing is saved or transmitted.

## The facilitator edition

Generated at `/facilitator/` by `python3 tools/build-facilitator.py` from
`facilitator/notes.json`: ATD-scripted rails (Say / Do / Ask with expected
answers / Debrief / Transition), a briefing slide (prep, materials,
contingencies, tough questions, three copy-paste templates), Full 90 /
Core 60 timing. Its QR encodes the learner URL.

## Editing map

- Copy: `index.html` · Recap: `QUESTIONS` in `assets/js/main.js`
- Trainers: `makeTrainer` configs (statGuess, stepSpot, assignStep,
  checkRate, sayJudge)
- Workflow mapper: `wfMap` block · Redesign Lab: `SLOTS` in main.js
- Capstone maps: `PRACTICE` / `NOT` / `WHEN` in main.js
- Runbook: `facilitator/notes.json` (timing must sum: Full 90 / Core 60)
- Citations to keep honest: McKinsey State of AI (88% adoption, ~6% high
  performers, redesign strongest EBIT factor, 2.8x / 55% vs 20%, ~21%
  redesigned), Metaintro (the manager's-core-job framing), automation-bias
  research (framing only, no invented numbers). The traffic light must
  match AI Basics and AI 201 exactly.
- Publish: `git push origin main && git branch -f gh-pages main && git push -f origin gh-pages`
