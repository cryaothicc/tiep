# TIEP

A typing test that looks like an amber CRT terminal. Single HTML file, no build step, no dependencies.

> **Status: under construction.**
> TIEP is a work in progress. Features change often, things are unfinished, and bugs are expected. Nothing here is stable yet.

## Running it

Open `Type.html` in a browser. That's it.

- The font (JetBrains Mono) loads from Google Fonts. Offline, it falls back to your system monospace font.
- Sound needs a first key press or click before the browser lets it play.
- Best on a desktop browser with a physical keyboard. Mobile is not a target yet.

## What works so far

**Typing**
- Words mode and code mode (JavaScript and Python snippets)
- 15, 30 and 60 second timed tests
- Normal and blind variants (blind blurs the text ahead of you)
- Untyped text is gray, correct text lights up amber, wrong text turns red
- Focus mode: the controls fade out when you start typing and come back when you move the mouse

**Shortcuts**
- `Tab` + `Enter`: new test
- `Tab` + `R`: repeat the same text
- `Tab` in code mode: types the indentation when the next characters are indent spaces

**Feedback**
- Left panel with live registers, a WPM chart, per-key accuracy bars and an event log
- On-screen keyboard that presses down as you type
- Three keyboard sounds (clack, thock, soft) plus off, cycled with the `snd` button
- Results: WPM, raw WPM, accuracy, correct/wrong/extra counts and a WPM-over-time graph
- Mistake breakdown: your most common key swaps, missed words and your weakest keys over time
- Replay: after a test, the keyboard replays your typing and leaves a heatmap of the keys you used most
- Drill mode: a practice test built from your weakest keys

**Saved in your browser** (localStorage, never sent anywhere)
- `tiep_keys`: per-key attempts and errors
- `tiep_runs`: your last 50 runs
- `tiep_pairs`: which wrong key you tend to type for each key

Clear your site data to reset all of it.

## Known rough edges

- The results screen can still scroll in short windows.
- The right Shift key on the on-screen keyboard is decorative.
- Only a handful of code snippets exist, so they repeat quickly.
- Key sounds are synthesized, not recorded, and haven't been tuned on real hardware.
- No settings are remembered between visits (sound choice, mode, length).
- Small screens are not laid out properly.

## Planned

- More code snippets and more languages
- Remember settings between visits
- A cleaner, shorter results layout
- Better key sounds
- A history view for past runs

## Contributing

It's too early for outside contributions. If you find a bug, a note about what you typed and which mode you were in helps.
