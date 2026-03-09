# Monkey Mind
*Too many tabs open.*

An interactive electronic literature piece — two voices in stochastic dialogue, exploring relational anxiety and the weight of what lingers. Optional text-to-speech narration.

## Overview

Monkey Mind presents two concurrent streams of generative text — each producing phrases composed from randomized subjects, predicates, and conjunctions. The result is an evolving, meditative dialogue that explores themes of relational anxiety, identity, and the significance that lingers from past relationships.

Based on Theo Lutz's groundbreaking 1959 program *Stochastische Texte* (Stochastic Texts), reimplemented by [Nick Montfort](http://nickm.com).

## Features

- **Dual Generative Voices**: Two independent text generators with distinct word pools and timing
- **Adjustable Speed**: Click to cycle each voice's interval (1000–7000ms)
- **Text-to-Speech**: Listen to the generated poetry read aloud
  - Machine voices (built-in, no setup required)
  - Human voices (natural-sounding, requires OpenAI API key)
- **Stereo Panning**: AI voices are spatially positioned — one voice on the left, the other on the right
- **Individual Muting**: Silence either voice independently — voices start muted, letting text accumulate before listening
- **Terminal Aesthetic**: Monospace type, dark background, color-coded voices (green/blue)

## Getting Started

1. Open `index.html` in a modern web browser
2. Click anywhere on the overlay to begin
3. (Optional) Enter an OpenAI API key for enhanced AI voices

### Voice Options

| Mode | Setup | Quality |
|------|-------|---------|
| Machine voices | None required | Synthetic, robotic |
| Human voices | OpenAI API key | Natural, expressive |

To use human voices, enter your OpenAI API key in the input field before starting. The key is saved locally for future sessions.

## Project Structure

```
├── index.html              # Main application (combines both voices)
├── stochastic_thing2.html  # "Him" voice generator
├── stochastic_thing3.html  # "Her" voice generator
├── js/
│   └── monkey-mind.js      # Core stochastic text engine
├── css/
│   ├── base.css            # Shared styles
│   ├── him.css             # "Him" character styling
│   ├── her.css             # "Her" character styling
│   ├── presentation.css    # Presentation mode styles
│   └── text-only.css       # Minimal text-only theme
├── images/                 # Character background images
├── archive/                # Experimental/test variants
│   ├── stochastic_test.html
│   ├── stochastic_thing3-1.html
│   ├── stochastic_thing3_use.html
│   └── stochastic_thing_testfile.html
└── mockups/                # Alternative visual layouts
    ├── dark-gallery.html
    ├── split-screen.html
    └── terminal.html
```

## How It Works

The `MonkeyMind` module generates sentences by randomly combining:

- **Subjects**: Relationship phrases ("you are my", "I am not your", "we were our")
- **Predicates**: Abstract nouns ("silence", "dream", "darkness", "freedom")
- **Conjunctions**: Connectors with parenthetical asides ("and", "but", "(please listen)")

Each voice has its own word pool and interval timing, creating an organic, overlapping conversation effect.

## Roadmap

- **Flexible gender pairings**: Allow any combination of voices — him/him, her/her, him/they, they/her, they/they, etc. Moving beyond the current fixed him/her duet to support a wider range of identity and relationship dynamics.

- **Syntactical variety**: Introduce multiple sentence templates beyond the current fixed `subject + predicate + conjunction + subject + predicate` structure:
  - Simple declarations ("I am your dream")
  - Question forms ("was she my distance?")
  - Negation contrasts ("we are our silence not our anger")
  - Endearment-addressed phrases ("darling, you are my darkness")
  - Templates selected stochastically with configurable weights, keeping the classic structure dominant
  - Endearments and interjections woven in — terms of address ("honey", "darling") and parenthetical asides ("(I hear you)", "(please don't)") that break the formal sentence pattern

- **Stochastic → responsive transition**: The voices currently generate independently with no awareness of each other. The vision is a piece that opens in pure stochastic mode and gradually shifts into dialogue:
  - Early phrases are fully random; over time, voices echo, mirror, or invert each other's words (e.g., "you are my silence" prompting "I am not your silence")
  - Transition is probability-based, ramping over phrase count rather than clock time, tracking the piece's internal rhythm
  - Even at full responsiveness, generation stays probabilistic — never fully scripted, always synthetic
  - Crucially, voices can only hear each other — unspoken text remains private. Turning on speech is what transforms parallel monologues into dialogue, making the listener complicit in bridging the two voices

- **Emotional arc**: The piece moves through emotional phases that mirror the rhythms of a real relationship:
  - meditation → tension → anger → defensiveness → despair → reconnection → recommitment
  - Word pools blend across phases based on phrase count, with each phase introducing and retiring vocabulary
  - Early predicates are contemplative (meadow, dream, quiet, gift); middle phases introduce friction (fury, wound, absence, thorn); later phases circle back toward repair (forgiveness, return, morning, hands)
  - The arc is not linear but cyclical — ebbing and flowing, with the possibility of revisiting earlier emotional ground at deeper levels

## Credits

- **Original Program**: Theo Lutz (1959) — *Stochastische Texte*
- **Reimplementation**: Nick Montfort
- **Text Translation**: Helen MacCormack

## License

```
Permission to use, copy, modify, and/or distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY
SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR
IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
```

## Browser Compatibility

Requires a modern browser with:
- ES6 JavaScript support
- Web Speech API (for browser voices)
- Web Audio API (for AI voice stereo panning)
- Fetch API (for OpenAI TTS)

Tested in Chrome, Firefox, Safari, and Edge.
