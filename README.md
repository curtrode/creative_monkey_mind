# Monkey Mind
*Too many tabs open.*

An interactive electronic literature piece — two voices in stochastic dialogue, exploring relational anxiety and the weight of what lingers.

## Overview

Inspired by [Nick Montfort](http://nickm.com)'s [Memory Slam](https://nickm.com/memslam/) — a collection of stochastic text engines running classics like "Love Letters" (Strachey) and "House of Dust" (Knowles & Tenney) — *Monkey Mind* began as an apprentice's remix and grew into something more ambitious. Where those foundational works exist as poetic monologues, *Monkey Mind* aspires to create a cluttered dialogue that dramatizes the anxieties of intimacy. Two voices generate text simultaneously, each assembling phrases from relational subjects ("you are my," "I am not your," "we were our") and abstract ("silence," "dream," "darkness," "freedom") or pastoral ("horses," "meadow," "yellow bird") predicates. The voices run at different speeds, creating an overlapping texture that evokes two minds thinking past each other.

The title references the Buddhist concept of "monkey mind" — restless consciousness swinging from thought to thought. The subtitle, *Too many tabs open*, updates the metaphor.

## Features

- **Dual Generative Voices**: Two independent text generators with distinct word pools and timing
- **Adjustable Speed**: Click to cycle each voice's interval (1000–7000ms)
- **Text-to-Speech**: Listen to the generated poetry read aloud
  - Machine voices (built-in, no setup required)
  - AI-generated voices (natural-sounding, requires OpenAI API key)
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
- **Predicates**: Abstract nouns ("silence", "dream", "darkness", "freedom") and pastoral imagery ("horses", "meadow", "yellow bird")
- **Conjunctions**: Connectors with parenthetical asides ("and", "but", "(please listen)")

Each voice has its own word pool and interval timing, creating an organic, overlapping conversation effect.

## Roadmap

- **Flexible gender pairings**: Allow any combination of voices — him/him, her/her, him/they, they/her, they/they, etc. Moving beyond the current fixed him/her duet to support a wider range of identity and relationship dynamics.

- **Richer language**: New sentence templates will introduce declarations, questions, negation contrasts, and direct address, expanding the grammar-based generation at the heart of this tradition.

- **Real-time responsiveness**: The voices currently generate independently. The next phase will expand the dialogic features so that unmuted stochastic voices begin to respond to one another under certain conditions — echoing, mirroring, or inverting each other's words. The central question: is it even possible to carry the stochastic nature of the original into something truly dialogic, in real time?

- **Emotional arc**: AI-generated texts will traverse registers of nostalgia, tension, anger, defensiveness, and reconnection — without guaranteeing resolution.

## Credits

- **Inspirations**: Christopher Strachey — *Love Letters* (1952); Alison Knowles & James Tenney — *A House of Dust* (1967)
- **Memory Slam**: Nick Montfort

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
