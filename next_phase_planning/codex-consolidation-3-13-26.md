# Monkey Mind Consolidation Plan

**Date:** March 13, 2026
**Purpose:** Consolidate the two March 13 planning notes into one actionable working plan for the Banff application sprint.
**Source files:** `Claude_ProjectBrief_3-13-26.md` and `Codex_ProjectBrief_3-13-26.md`

## Goal

Establish a single source of truth for the project narrative, prototype scope, and March 13-24 execution plan.

The immediate aim is not to expand scope. The immediate aim is to make the existing direction legible, prioritized, and executable before the March 24, 2026 Banff deadline.

## Primary Conclusion

Use the Claude brief as the base master document.

Reason:
- It already has the strongest high-level structure for application-facing work.
- It clearly separates current state, prototype needs, Banff framing, timeline, and open questions.
- It is closer to a canonical brief than the Codex session notes.

Use the Codex notes as a secondary source document.

Reason:
- It contains strong language for concept framing.
- It adds useful design constraints and implementation thinking.
- It includes material that should be preserved, but not kept as a parallel master brief.

## What To Consolidate

### Keep in the master document

- Problem statement: the current work needs clearer differentiation from Montfort.
- Core concept: the transition from stochastic generation to LLM improvisation is the dramatic event.
- Creative vision: intimacy, listening, drift, and formal transition.
- Prototype scope: single-voice Gemini piece in a separate file.
- Banff strategy: three-part portfolio and residency-scale multi-model dialogue.
- Timeline: March 13-24 sprint.
- Decisions made.
- Decisions still open.

### Pull in from the Codex notes

- Concept sentence: "Monkey Mind stages the moment when mechanical language begins to listen."
- Positioning sentence about extending combinatory electronic literature through the transition between generative paradigms.
- Asymmetric voice roles for the future multi-model dialogue.
- Implementation checklist logic:
  - accumulate stochastic lines
  - phase state
  - staged prompt handoff
  - interface continuity

### Move out of the master brief into appendix or backlog

- Long precedent research details
- Full model output samples
- Teaching connection and course rationale
- README improvement ideas
- Broader repository presentation ideas that are not required for March 24

## Organizational Problems To Fix

### Problem 1: Two active planning documents are competing

Risk:
- Decisions will drift.
- Wording will diverge across proposal, cover letter, README, and prototype notes.
- The sprint will lose time to re-deciding the same questions.

Action:
- Name one document as the master brief.
- Reframe the other as supporting notes or archive.

### Problem 2: Confirmed decisions and hypotheses are mixed together

Risk:
- Teaming with the documents will feel more certain than the project really is.
- Prototype work may absorb unnecessary complexity too early.

Action:
- Add a section titled `Decision Status`.
- Divide content into three buckets:
  - `Locked Now`
  - `Needs Testing This Week`
  - `Residency Version`

### Problem 3: Immediate sprint work is mixed with later-stage ideas

Risk:
- The March 24 application prototype becomes overloaded.
- Lower-value tasks compete with submission-critical work.

Action:
- Separate `Application Sprint` tasks from `Post-Submission Backlog`.
- Treat teaching language, README refinement, and repository polish as backlog unless needed for reviewer clarity.

## Recommended Master Document Structure

The consolidated master brief should use this order:

1. Title, date, purpose
2. One-sentence concept
3. The problem
4. Creative vision
5. Prototype for the application
6. Banff residency-scale vision
7. Decision status
8. Timeline and dated checklist
9. Appendix

## Decision Status Framework

### Locked Now

- Gemini 2.5 Flash is the prototype model.
- The application prototype is single-voice, not full multi-model dialogue.
- The prototype should be built as a separate file and should not disrupt the existing piece.
- The formal engine of the piece is stochastic generation drifting into improvisation.
- The authorial intervention happens through staged system prompts.

### Needs Testing This Week

- Transition trigger:
  - timer
  - line-count threshold
  - manual trigger for testing
- Transition visibility:
  - seamless drift
  - noticeable break
  - both modes for experimentation
- Gemini browser integration approach:
  - JS SDK
  - direct REST calls
- Video capture format:
  - short excerpt
  - full run
  - narrated or silent

### Residency Version

- Two or more models in live dialogue
- Asymmetric roles between voices
- One voice transitioning before the other
- TTS embodiment for improvisation
- Cross-model listening and response logic
- Model-specific prompt direction as dramaturgy

## Action Plan: March 13-24

### Phase 1: Consolidate the planning layer

Target date: March 13-14

Actions:
- Designate one master brief.
- Extract the strongest framing language from the Codex notes into that brief.
- Move non-essential material into an appendix or backlog section.
- Add the `Decision Status` section.
- Convert broad prose priorities into a dated checklist.

Deliverable:
- One planning document that can drive the prototype build and the written materials without contradiction.

### Phase 2: Resolve open prototype decisions quickly

Target date: March 14-16

Actions:
- Test transition trigger options.
- Decide how visible the handoff from stochastic to Gemini should be.
- Choose the Gemini browser integration path.
- Decide the minimum viable video format for reviewers without API access.

Deliverable:
- A short implementation decision list that locks the prototype scope.

### Phase 3: Build only the application prototype

Target date: March 15-21

Actions:
- Build the single-voice improvisation prototype.
- Keep the terminal-style interface consistent with the existing piece.
- Feed accumulated stochastic output into staged prompts.
- Support the three drift phases:
  - echo
  - bend
  - drift
- Keep optional features optional.

Do not expand into:
- full two-model dialogue
- deep TTS redesign
- README overhaul
- teaching materials

Deliverable:
- A working prototype that demonstrates the formal transition clearly enough to document and show.

### Phase 4: Package the application

Target date: March 18-24

Actions:
- Record a strong prototype run.
- Revise the proposal using the consolidated language.
- Revise the cover letter using the same framing.
- Present the portfolio as three linked stages:
  - 2019 original
  - current version
  - improvisation prototype

Deliverable:
- A coherent submission package with one narrative across prototype, proposal, and support materials.

## Immediate Priorities

These are the highest-value next actions:

1. Freeze the core narrative: stochastic-to-improvisational drift is the main claim.
2. Choose the master brief and stop treating both March 13 documents as peers.
3. Resolve the four open prototype decisions.
4. Build only the single-voice Gemini prototype needed for the application.
5. Package the submission around the three-artifact portfolio and a reviewer-friendly video.

## Content To Reuse Verbatim or Near-Verbatim

These lines are strong enough to standardize across materials:

- "Monkey Mind stages the moment when mechanical language begins to listen."
- "The transition from stochastic generation to LLM improvisation is the dramatic event."
- "System prompts function as directorial instruments."

These should become the canonical language pool for:
- proposal revision
- cover letter revision
- repository framing
- prototype description

## Scope Guardrails

During the March 24 sprint, reject or defer work that does not directly improve one of these outcomes:

- prototype clarity
- proposal clarity
- reviewer accessibility
- portfolio coherence

Defer unless necessary:
- README redesign
- teaching framing
- extensive precedent expansion
- residency-scale architecture beyond proposal language

## Recommended File Roles

- `Claude_ProjectBrief_3-13-26.md`
  - Keep as the likely basis for the master brief
- `Codex_ProjectBrief_3-13-26.md`
  - Treat as supporting notes to mine for language and design logic
- `codex-consolidation-3-13-26.md`
  - Use as the operational plan for consolidation and next actions

## Definition of Done

This consolidation effort is complete when:

- one document is clearly the master brief
- decisions are separated from experiments and future ideas
- the March 24 sprint tasks are explicit and prioritized
- the prototype scope is constrained to the application need
- proposal, cover letter, and prototype planning all draw from the same core language
