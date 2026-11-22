# Nne Says!

**Learn Igbo with Mama.** A fun, funny Igbo language game. Mama calls out a word, you answer before the timer runs out, and if you get it wrong, the slipper comes flying.

**Play it:** https://techlady93.github.io/nne-says/ (sound on)

## Why this exists

Many Nigerian-American kids grow up never learning their parents' language. I'm one of them. Igbo has tens of millions of speakers, but it often isn't passed down in diaspora homes, and Duolingo, the app most young people try first, doesn't teach it.

Nne Says! is a way to reconnect with Igbo roots. It is for first-generation Nigerian-Americans, for Igbo children growing up without lessons at home, and for anyone heading to the East of Nigeria who wants basic Igbo on the fly, so the language keeps living.

**Audience:** teens 13+, young adults, and travelers.

## Features

- **Lessons:** 10 units, from "Ndewo" (hello) to a first real conversation. Each unit has four steps: Learn (flashcards with audio), Practice (multiple choice), Build (put the words of a sentence in order) and Talk (a short dialogue Mama reads aloud).
- **Quick play:** a 60-second round with 3 slipper "lives," streaks and score multipliers up to x4.
- **Traveler mode and Phrasebook:** market, taxi, directions and emergency phrases, searchable in English or Igbo.
- **Mama's voice:** 144 Igbo words and lines, 15 reactions and 116 spoken corrections, voiced in a warm Nigerian-mother voice. She praises, teases and scolds, and the game waits for her to finish talking.
- **Mama reacts:** her face changes (happy, calm, cross) with every answer, and a slipper flies across the screen when you miss.
- **Progress saved** on the device, best score, and a "copy score to share" button.
- **Slipper revive:** a sample rewarded-ad break, showing how the free version will make money.
- **Accessible:** keyboard keys 1–4, screen-reader labels, large tap targets, dark mode and reduced-motion support.

## How it's built

- One self-contained `index.html` (HTML, CSS and vanilla JavaScript) with no framework and no build step, so it loads fast and works on any phone browser.
- Mama, the slipper and the wax-print background are drawn in SVG and CSS, so there are no image files.
- Audio is plain MP3 files played with the HTML Audio API. A small promise-based player queues clips so Mama is never cut off.
- Progress is stored with `localStorage`.
- Fonts: Baloo 2 and Nunito (Google Fonts), chosen because they support Igbo letters like ị, ọ, ụ and ṅ.

## Run it locally

1. Clone the repo: `git clone https://github.com/TechLady93/nne-says.git`
2. Open `index.html` in any modern browser (Chrome, Safari, Edge, Firefox).
   If your browser blocks audio from local files, run `python3 -m http.server` in the folder and open http://localhost:8000.

No install, accounts or API keys needed.

## Project layout

| Path | What it is |
| --- | --- |
| `index.html` | The game: Lessons, Quick play, Phrasebook |
| `audio/words/` | One MP3 per Igbo word or sentence (e.g. `mmiri.mp3`) |
| `audio/mama/` | Mama's reactions (`praise-1.mp3`, `scold-3.mp3`, ...) |
| `audio/means/` | Mama's corrections: "It means: ..." for every English meaning |
| `meaning-script.csv` | The 116 correction lines and their file names |
| `voice-script.csv` | Every word and Mama line to voice, with its file name |
| `APP-STORE-PLAN.md` | Plan for the iOS/Android app and how it makes money |

## Use of AI tools

- **Claude (Anthropic)** helped write the code, lesson content and Mama's lines, with me directing the design, humor and cultural details.
- **ElevenLabs** generated Mama's voice from the script.
- The Igbo is a draft in standard Igbo. A native speaker will review spelling, tone marks and dialect before launch.

## Roadmap

- [x] 10 lesson units (learn, practice, sentence builder, conversations)
- [x] Mama's voice for every word and line
- [x] Traveler mode and phrasebook
- [x] Slipper lives with a sample rewarded-ad revive
- [ ] Native-speaker review of all vocabulary and tone marks
- [ ] Playtest with 20 to 30 people
- [ ] "Say it like Mama": record yourself and compare
- [ ] iPhone and Android app (Capacitor), with reminders and a word-of-the-day widget
- [ ] Premium subscription and dialect packs

Built by Joycelynn "Chioma" Okezie ([@TechLady93](https://github.com/TechLady93)).
