# Nne Says!

A fun, funny Igbo language game. Mama calls out a word, you answer before the timer runs out, and if you get it wrong, the slipper comes flying.

## Why this exists

Many Nigerian-American kids grow up never learning their parents' language. Nne Says! is a way to reconnect with Igbo roots. It is also for Igbo children growing up without lessons at home, and for anyone heading to the East of Nigeria who wants basic Igbo on the fly, so the language keeps living.

**Audience:** teens 13+, young adults, and travelers.

## Play

Open `index.html` in a browser. It runs on phones too, with no install.

## Project layout

| Path | What it is |
| --- | --- |
| `index.html` | The game (single file: HTML, CSS, JS): Lessons, Quick play, Phrasebook |
| `APP-STORE-PLAN.md` | How the app passes Apple review, plus monetization setup |
| `voice-script.csv` | Every word and Mama line to voice, with its target file name |
| `audio/words/` | One MP3 per Igbo word (e.g. `mmiri.mp3`) |
| `audio/mama/` | Mama's reactions (`praise-1.mp3`, `scold-3.mp3`, ...) |

## Roadmap

- [x] 10 lesson units (learn, practice, sentence builder, conversations)
- [x] Slipper lives with rewarded-ad revive
- [ ] Native-speaker review of all vocabulary and tone marks
- [x] Voice every word and Mama line (ElevenLabs, 129 clips)
- [x] Voice the lesson sentences and conversation lines (18 clips)
- [ ] Playtest with 20 to 30 people
- [x] Traveler mode: market, transport, greetings and directions phrases
- [ ] Wrap for iOS and Android (Capacitor)
- [ ] Ads for 13+ audience and a paid ad-free unlock

Built by Joycelynn "Chioma" Okezie ([@TechLady93](https://github.com/TechLady93)).
