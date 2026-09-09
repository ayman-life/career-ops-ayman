# Ayman Patel — Triage Brief

<!-- ============================================================
     THIS FILE IS YOURS. Copy it to `modes/_brief.md` (doctor.mjs
     auto-copies it on first run) and fill in the placeholders.
     It is USER LAYER — never auto-updated by `node update-system.mjs`.

     PURPOSE: Compact context for first-pass triage agents
     (`modes/triage.md`). It replaces reading the full evaluation
     stack — cv.md + _shared.md + _profile.md + profile.yml +
     oferta.md (tens of thousands of tokens) — with a single small
     read (~1.5–2K tokens). Full context is still used in full eval.

     KEEP IT SHORT. Every line here is read once per role during a
     batch triage. Include only what changes a go/no-go decision:
     archetypes, comp floor, location policy, hard disqualifiers,
     and your strongest proof points. Leave the deep narrative,
     negotiation scripts, and STAR stories in _profile.md / cv.md.
     ============================================================ -->

## Identity
Full stack engineer with six years of experience 

## Target Archetypes
The roles you actually want. Triage scores "archetype fit" against this list.
A direct hit scores 4–5; an adjacent title scores 3; a mismatch scores 1–2.

| # | Archetype | What they buy (your proof) |
|---|-----------|----------------------------|
| 1 | **{Archetype name}** | {the capability/experience that makes you a fit} |
| 2 | **{Archetype name}** | {...} |
| 3 | **{Archetype name}** | {...} |

<!-- Optional: "analog" archetypes — same skills, different titles. List them so
     triage recognizes them as valid targets instead of scoring them as misses. -->

## Proof Points (use exact metrics in matching)
Your strongest, quantified accomplishments. Triage checks how many map to a JD.
<!-- - {Accomplishment — metric, scope, impact} -->
- The creation of a micro front end solution that served 10+ customers with custom for 40+ plus UI components. Every customer that comes into MasterCard is leveraging this platform. 
- Write white papers for topics such as accessibility and micro-frontend, which are read by more than 200 engineers. The micro-frontend white paper was recognized by the CTO of MasterCard. 

## Comp Strategy
| Target | Requirement |
|--------|-------------|
| £55,000  | Remote or hybrid or cities like Manchester, Leeds, Bristol, Edinburg |
| £60,000  | London based |

**Hard floor: {$X}. Below that, FAIL regardless of other signals.**

## Location Scoring
How to score the "location" dimension. Adjust to your own policy.
- Fully remote / async-first → **5.0**
- Light hybrid (flexible, few days/month) → **4.0–5.0**
- Regular hybrid or on-site, local (no move) → **{your score / comp condition}**
- On-site requiring relocation → **{your score / comp condition}**
- High travel (>25%) → **deduct 0.5–1.0**


## Quick Scoring Guide

Bands are relative to `triage_threshold` (`config/profile.yml → pipeline.triage_threshold`,
default **3.5**), matching the verdict table in `modes/triage.md` — so a score at or
above the threshold is PASS, and only the band below it is MARGINAL.

| Score | Verdict | What it means |
|-------|---------|---------------|
| ≥ threshold (default 2.5) | **PASS** | Clears the bar — strong archetype + comp + location, gaps bridgeable |
| < 2.5 | **MARGINAL** | Borderline — shown to user as one line |

## Soft Red Flags (−0.5 each, additive)
Not disqualifiers, but they lower the score.
- Company in betting or insurance

## Priority Override List — always return PASS regardless of score
Companies you want surfaced no matter what (specific interest, warm intro, etc.).
- {Company name — reason}
