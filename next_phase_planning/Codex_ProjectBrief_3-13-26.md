# Monkey Mind --- Development Notes from Session

Date: 2026-03-13

## Core Concept

Monkey Mind stages a transition between two generative language
paradigms:

1.  Rule-based stochastic generation
2.  LLM improvisational generation

The transition itself becomes the dramatic arc of the piece.

**Concept sentence:**\
Monkey Mind stages the moment when mechanical language begins to listen.

------------------------------------------------------------------------

# Dramaturgical Structure

## Phase 1 --- Mechanical Speech

Characteristics: - stochastic combinatory grammar - patterned phrases -
no memory - no listening

Audience perception: machines producing language but not communicating.

------------------------------------------------------------------------

## Phase 2 --- Emergent Listening

LLM begins operating but remains constrained by earlier grammar.

Key behavior: - quoting earlier phrases - transforming fragments -
partial responsiveness

Audience perception: the system hears itself.

------------------------------------------------------------------------

## Phase 3 --- Improvisation

LLM generates freely.

Characteristics: - longer lines - expanded vocabulary - emotional
specificity - references to earlier language

Audience perception: language becomes intentional.

------------------------------------------------------------------------

# Dialogue Structure for Multi‑Model Version

Introduce **asymmetric conversational roles**.

### Voice A --- Reaching

-   attempts connection
-   interprets the other voice generously
-   uses metaphor and emotional openness

### Voice B --- Resisting

-   questions meaning
-   deflects emotional claims
-   interrupts or redirects

Purpose: - prevents parallel monologues - produces dramatic tension -
simulates relationship dynamics.

------------------------------------------------------------------------

# Artistic Framing

The work intersects three traditions.

## Electronic Literature

Relevant works: - Taroko Gorge --- Nick Montfort - Sea and Spar Between
--- Montfort & Strickland

Connection: rule-based generative poetry.

## AI Poetry

Relevant works: - ReRites --- Jhave Johnston - contemporary LLM poetics

Connection: machine learning text generation.

## Improvisational Performance

Relevant traditions: - jazz improvisation - theater improv - networked
improvisational fiction

Connection: responsive dialogue.

------------------------------------------------------------------------

# What Is New About the Piece

1.  **Dramaturgy of generation**\
    The artwork is the transition between generative paradigms.

2.  **Models as characters**\
    Different LLMs act as distinct psychological voices.

3.  **Prompts as direction**\
    System prompts function like dramaturgical instructions.

------------------------------------------------------------------------

# Conceptual Metaphors

Useful explanatory metaphors.

### Jazz

stochastic system = the head\
LLM improvisation = the solo

### Listening

speech → hearing → response → intimacy

### Computation

deterministic grammar → probabilistic language

------------------------------------------------------------------------

# Teaching Connection --- Creative Coding (Spring 2027)

The project supports teaching generative language systems.

Possible course sequence:

1.  rule-based generative text
2.  combinatory grammars
3.  Markov systems
4.  limitations of rule systems
5.  LLM prompting
6.  hybrid generative systems

Students learn: - history of computational literature - mechanics of
generative systems - creative uses of AI tools.

------------------------------------------------------------------------

# Design Insights

### Echo phase should reference earlier lines

Creates perception of listening.

### Voices should have asymmetric roles

Prevents AI agreement loops.

### Transition should be gradual

Mechanical → responsive → improvisational.

------------------------------------------------------------------------

# Proposal Positioning Sentence

Monkey Mind extends the tradition of combinatory electronic literature
by staging the transition from rule‑based text generation to
large‑language‑model improvisation as a dramatic event.

------------------------------------------------------------------------

# Development Priorities

## Immediate Prototype

-   implement stochastic accumulation
-   send context to Gemini
-   staged prompts (echo → bend → drift)

## Residency Goals

-   multi‑model dialogue
-   text‑to‑speech embodiment
-   cross‑model interaction

------------------------------------------------------------------------

# Repository README Suggestions

For Banff reviewers, the repository front page should quickly
communicate what the project is.

Recommended additions to the README:

## 1. One‑sentence description

Example:

Monkey Mind stages the transition from rule‑based text generation to
large‑language‑model improvisation as a dramatic event between two
machine voices.

## 2. Link to the live piece

Example:

https://curtrode.github.io/monkey_mind/

## 3. Screenshot or GIF

A visual of the terminal interface helps reviewers immediately
understand the format of the work.

## 4. Brief explanation of the generative system

Example structure:

1.  stochastic grammar generates patterned dialogue\
2.  lines accumulate as context\
3.  Gemini begins echoing the patterns\
4.  generation drifts into improvisation

## 5. Repository structure overview

application_docs/ --- Banff proposal materials\
src/ --- stochastic generator code\
improv/ --- Gemini improvisation prototype

Purpose: Help reviewers orient themselves in the project within 10--15
seconds.

------------------------------------------------------------------------

# Gemini Prototype Implementation Plan

Goal: build a single-voice improvisation prototype demonstrating the
transition from stochastic generation to Gemini-driven improvisation.

## Step 1 --- Context accumulation

Store stochastic lines in a buffer:

    let contextBuffer = [];
    contextBuffer.push(line);

Collect approximately 15--40 lines before activating Gemini.

## Step 2 --- Phase tracking

Use a simple phase state:

    let phase = "stochastic"; // stochastic | echo | bend | drift

Possible triggers: - line count threshold - timer threshold - manual
toggle (for testing)

## Step 3 --- Gemini API call

Send accumulated context with stage-specific prompt instructions.

Example flow:

1.  stochastic generator produces lines
2.  context buffer accumulates lines
3.  Gemini receives context and system prompt
4.  Gemini generates the next line

## Step 4 --- Echo / Bend / Drift prompts

Echo phase: - mimic grammar patterns - reuse existing vocabulary - quote
fragments from previous lines

Bend phase: - introduce new vocabulary - expand phrase length - begin
responding to earlier lines

Drift phase: - free improvisation - emotional specificity - references
to earlier context

## Step 5 --- Interface continuity

Maintain the same terminal-style interface so the transition appears
seamless.

Important: The stochastic generator should continue running in the
background so its language remains present as memory.

------------------------------------------------------------------------

# Banff Proposal Positioning Notes

Key framing idea:

Monkey Mind explores what happens when the deterministic logic of
rule-based text generation encounters the improvisational language of
large language models.

## Position in electronic literature

Relevant lineage:

-   Taroko Gorge --- Nick Montfort
-   Sea and Spar Between --- Montfort & Strickland
-   ReRites --- Jhave Johnston

The project extends this tradition by staging the transition between
generative paradigms.

## Conceptual emphasis

Important points to communicate:

1.  The work investigates listening in machine language.
2.  The shift from stochastic generation to LLM improvisation forms the
    dramatic arc.
3.  Multiple models can function as distinct voices in dialogue.

## Teaching connection

Residency research will inform the first offering of Creative Coding
(Spring 2027).

Students will explore:

-   rule-based generative text systems
-   combinatory grammars
-   limitations of deterministic systems
-   LLM prompting and hybrid systems

This provides a bridge between the history of computational literature
and emerging AI-assisted creative practice.
