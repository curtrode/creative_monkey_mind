# Monkey Mind
*Too many tabs open.*

An interactive electronic literature piece — two voices in stochastic dialogue, exploring relational anxiety and the weight of what lingers.

## Overview

Built on [Nick Montfort](http://nickm.com)'s reimplementation of Theo Lutz's 1959 *Stochastische Texte*, *Monkey Mind* turns the tradition's stochastic sentence generation toward the language of intimacy — possession, negation, longing, and silence. Two voices generate text simultaneously, each assembling phrases from relational subjects and abstract predicates. The voices run at different speeds, creating an overlapping texture that evokes two minds thinking past each other — a stochastic duet that never quite resolves into conversation.

The title references the Buddhist concept of "monkey mind" — restless consciousness swinging from thought to thought without resolution. The subtitle grounds this in contemporary digital attention.

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

- **Stochastic → responsive transition**: The voices currently generate independently. The vision: open in pure stochastic mode and gradually shift into dialogue, where one voice echoes, mirrors, or inverts the other's words. The transition is probabilistic, never fully scripted, tracking the piece's internal rhythm. Voices can only hear each other through vocalization — unspoken text remains private. Enabling speech transforms parallel monologues into dialogue, making the listener complicit in bridging two minds. The central question: is it even possible to carry the stochastic nature of the original into something truly dialogic, in real time?

- **Emotional arc**: Word pools evolve through phases mirroring the rhythms of a real relationship — meditation, tension, anger, defensiveness, despair, reconnection, recommitment. The arc is cyclical, ebbing and flowing, revisiting earlier emotional ground at deeper levels.

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
