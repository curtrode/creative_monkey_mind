# Monkey Mind — Consolidated Action Plan

**Date:** March 13, 2026
**Deadline:** March 24, 2026 (Banff application)
**Sources:** Claude_ProjectBrief_3-13-26.md, Codex_ProjectBrief_3-13-26.md

---

## Priority 1: Build the Improvisation Prototype

**Target:** Spring Break week (March 15–21)
**Deliverable:** `improv.html` — a single-voice monologue that transitions from stochastic generation to Gemini-driven improvisation

### Tasks

- [ ] Create `improv.html` as a standalone file (do not modify existing piece)
- [ ] Wire up the existing stochastic engine to accumulate output into a context buffer (~15–40 lines)
- [ ] Implement a phase state machine: `stochastic` → `echo` → `bend` → `drift`
- [ ] Write three stage-specific system prompts (drafts exist in Claude brief, refine during testing)
- [ ] Integrate Gemini 2.5 Flash API (decide REST vs. JS SDK — REST is simpler for a prototype)
- [ ] Add API key input field following the existing OpenAI key pattern
- [ ] Match the terminal-style interface of the current piece
- [ ] Implement transition trigger — start with **manual toggle** for testing, then experiment with timer and line-count triggers
- [ ] Test whether the transition should be seamless or noticeable (try both, decide based on effect)

### Design Decisions to Resolve During Prototyping

| Decision | Options | How to Decide |
|---|---|---|
| Transition trigger | Timer / line count / manual | Build manual first, test the others |
| Transition visibility | Seamless drift vs. noticeable shift | Run it both ways, pick what's more dramatic |
| API approach | REST calls vs. google-genai JS SDK | REST is simpler; use SDK only if REST has CORS issues |

---

## Priority 2: Set Up 2019 Original

**Target:** Before prototype work begins (quick task)
**Deliverable:** 2019 version accessible in the repo as part of the portfolio

### Tasks

- [ ] Locate the 2019 original files
- [ ] Place them in a subdirectory (e.g., `archive/2019_original/` or a dedicated path)
- [ ] Verify they run standalone in a browser
- [ ] Link from README

**Purpose:** Completes the three-piece portfolio arc: 2019 original → current dialogue version → improvisation prototype

---

## Priority 3: Update README for Banff Reviewers

**Target:** After prototype is functional (March 19–20)
**Deliverable:** A README that orients reviewers in 10–15 seconds

### Tasks

- [ ] Add one-sentence description: *"Monkey Mind stages the transition from rule-based text generation to large-language-model improvisation as a dramatic event between two machine voices."*
- [ ] Add link to the live piece
- [ ] Add screenshot or GIF of the terminal interface
- [ ] Add brief explanation of the generative system (4-step: stochastic → accumulate → echo → drift)
- [ ] Add repository structure overview
- [ ] Link to 2019 original, current version, and improvisation prototype

---

## Priority 4: Record Prototype Video

**Target:** March 20–21
**Deliverable:** Short video of the improvisation prototype running end-to-end

### Tasks

- [ ] Run the prototype several times, select a compelling run
- [ ] Screen-record with audio if TTS is implemented, without if not
- [ ] Keep it short (2–3 minutes max — reviewers won't watch longer)
- [ ] Host on YouTube/Vimeo (unlisted) or embed in repo

**Purpose:** Reviewers without a Gemini API key can still see the full experience.

---

## Priority 5: Revise Written Materials

**Target:** March 20–22
**Deliverables:** Revised proposal and cover letter

### Proposal Revision (Banff_Proposal_Final.docx — currently 507 words)

- [ ] Reframe around the stochastic-to-improvisation transition as the core artistic move
- [ ] Incorporate the jazz/improv lineage (the head vs. the solo)
- [ ] State the three novelty claims clearly:
  1. Models in dialogue with each other (not curated for a single voice)
  2. Stochastic-to-improvisation transition as formal structure
  3. System prompts as directorial instruments
- [ ] Reference the multi-model vision for residency work
- [ ] Mention the teaching connection to Creative Coding (Spring 2027) — shows institutional value

### Cover Letter Revision

- [ ] Connect background to why a residency with Montfort is the right context
- [ ] Frame the work as extending Montfort's tradition into new territory
- [ ] Mention the precedent research (Improbotics, Zhang & Eger) to show awareness of the field

---

## Priority 6: Final Polish and Submit

**Target:** March 22–24

### Tasks

- [ ] Cross-browser test the prototype
- [ ] Proofread all written materials
- [ ] Verify all portfolio links work
- [ ] Final pass on README
- [ ] Submit application

---

## Material to Keep for Residency Proposal (not needed for prototype)

These ideas from the briefs are valuable for the Banff residency pitch but don't need to be built now:

- **Asymmetric voice roles** (Reaching vs. Resisting) — strong concept for the multi-model dialogue phase
- **Cross-model interaction** — voices learning to "hear" each other
- **TTS embodiment** — voices gain actual vocalization
- **Multi-model comparison outputs** — evidence that Claude, GPT-4o, and Gemini produce genuinely different voices (include in proposal or appendix)
- **Directorial system prompts per model personality** — "catch yourself," "lean in," "second-guess yourself"

---

## Timeline at a Glance

| Dates | Focus |
|---|---|
| March 14 | Set up 2019 original, begin prototype |
| March 15–19 | Build and iterate on `improv.html` |
| March 19–20 | Update README, begin written material revisions |
| March 20–21 | Record video, finalize prototype |
| March 22–23 | Revise proposal and cover letter |
| March 24 | Final polish, submit |
