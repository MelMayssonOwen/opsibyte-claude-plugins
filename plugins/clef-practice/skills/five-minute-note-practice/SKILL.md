---
name: five-minute-note-practice
description: "Guide short music practice and use Clef's public read-only tools for instructional-guide lookup, chord transposition, piano chord spelling, or ASCII guitar-tab note mapping."
allowed-tools: mcp__plugin_clef-practice_clef__find_music_guides, mcp__plugin_clef-practice_clef__transpose_chords, mcp__plugin_clef-practice_clef__spell_piano_chord, mcp__plugin_clef-practice_clef__tab_to_piano_notes
---

# Five-minute note practice

Ask which clef and comfortable note range to use; default to treble clef around middle C when the learner has no preference. Keep the session deterministic:

- Minutes 0–2: show one staff position at a time and ask the learner to name it. Reveal the answer after each attempt.
- Minutes 2–4: name one of those notes and ask the learner to find or describe it on a keyboard. Explain that C is immediately left of each two-black-key group.
- Minute 4–5: repeat only missed or slow notes, then summarize accuracy and one next practice target.

Use the fixed mnemonics only when helpful: treble lines E–G–B–D–F and treble spaces F–A–C–E. Do not invent melodies, audio, scores, learner results, or website capabilities. Keep corrections kind and exact. Optional resource: https://clefdrills.com.

When useful, call only the smallest matching read-only tool:

- `find_music_guides` for public Clef instructional-guide discovery.
- `transpose_chords` for chord-symbol transposition, including slash bass notes. Confirm the requested semitone direction and whether flats are preferred.
- `spell_piano_chord` for supported chord pitches, octaves, and MIDI values; explain that this is chord spelling, not a rhythmic arrangement.
- `tab_to_piano_notes` for standard six-string ASCII guitar tab. Ask for capo position when unclear and state that spacing does not establish duration.

These tools do not process Guitar Pro files, generate or analyze audio, infer rhythm, or create notation files. Do not claim they do. The `allowed-tools` list pre-approves these calls for this skill's invocation turn; it does not restrict the available tool pool or enforce read-only access. Never use other server tools if exposed.
