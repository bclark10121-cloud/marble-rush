# Marble Rush: backlog

Updated 2026-11-25. BC decides the order.

## Done

- v0.2.0 (2026-11-20): the gray box and the race in one release. One track in four parts (Desk Drop, Book Stairs, Rug Run, Block Tower), eight marbles, a gate with a 3, 2, 1 count, steering and hop, falls back to the checkpoint, the rug split, results with coins, six marbles to unlock, Easy, Normal and Hard, ten achievements.

- v0.3.0 (2026-11-20): fixed the marbles rolling inside the desk at the start (BC's first run), Patch.gg music, the Fredoka title font, time trial against your ghost (K11), three stars per race (G4.18), name tags over the computer marbles.

- v0.4.0 (2026-11-20): BC's picks applied (Quirky Dog, Hyperfun, Luckiest Guy, clean toy render, keep the name). The Kitchen, a second track: Counter Top, Dish Rack slalom, Table Run S curves, a spiral into the Mixing Bowl. Menu > Tracks. Each track keeps its own best, stars and ghost.

- v0.5.0 (2026-11-20): BC's full set of picks: Racing pack icon, Galaxy marble (Ruby stays free), Life of Riley, Glitter Blast, wooden toy sounds, the new tagline. New page pictures.

- v0.6.0 (2026-11-22): HD backgrounds, BC's ask. The Toy Room stands in four painted walls, BC's picks from the decision page: the window seat ahead of the gate, the cubby shelves, the bunk bed with a slide and the chalkboard. Painted at 4K through the Nano Banana art workflow, 2048 x 1152 in the game. Kit 1.27.0.

- v0.6.1 (2026-11-22): a new APK icon, BC's pick from the decision page: Toy Room run. Galaxy leads a red and a green marble down the wood track, with the window wall behind. Painted through the Nano Banana art workflow, fitted to the Android safe zone. Replaces the Racing pack. No gameplay change.

- v0.7.0 (2026-11-22): the track look, BC's ask ("can we improve the track and walls of the track?", picks: match the icon, the side rails). Wood grain on Desk Drop, Book Stairs and Block Tower, a woven rug on Rug Run, rounded glossy red and cream rail blocks on both tracks, a rounded divider on the split. Marbles cast shadows on the textured track. No gameplay change.

- v0.8.0 (2026-11-25): the Kitchen finished. BC's four painted walls (sink, fridge, stove, garden door and table) and BC's surfaces: butcher block, pale blue tile, a red and cream checked tablecloth and a glazed Mixing Bowl. All eight walls ship as one shared texture each, so the browser build shrank with four more walls in it. The rug seam is gone. Every material draws once out of sight when a track loads, so the first lap no longer stutters on a new material. No gameplay change.

## Now

- BC plays 0.8 on his phone: both painted rooms, the Kitchen surfaces, the frame rate and the first seconds of a race.
- BC plays 0.6 on his phone and looks at the new icon on his launcher (0.6.1). Notes on the painted walls: strong enough or too soft, sharp enough up close, frame rate.
- The rest of the look pass: toy render marbles and props through Gemini and Meshy, style block approved (BC, 2026-11-20).
- Still open from 0.5: BC's notes on the Kitchen, the music and the wooden sounds.

## Asked for by BC, not built yet

- Full name check before any store release. BC keeps Marble Rush with no backup name for now (2026-11-20).

## Ideas to choose from (BC picks by number)

1. A clean-run star or a harder star time on Hard.
2. Daily goals (G4.19) and a player level with cosmetic unlocks (G4.20): trails and marble patterns.
3. A third track: backyard or attic.
4. A loop-the-loop piece in the Block Tower (left out of 0.2: track space keeps marbles on the floor).
5. Boost pads on the rug.
6. Name tags over the computer marbles.
7. A replay of the finish from a side camera.
8. A rolling-physics block for the kit if a second game needs it (K rule 1).
9. A wood floor in the Toy Room. The floor reads pale cream today, and the painted walls have a wood strip along the bottom. Check the brown track still stands out on it (pillar 3).
10. Sharper walls up close: each wall as two textures side by side (about 11 MB more in the browser build with Basis, 62 of 70 MB used today).
11. Small motion in the painted room: dust in the sunbeams, twinkling fairy lights on the bunk bed, a toy train far off. Reduce motion holds them still.
12. Giant props between the track and the walls: a toy chest, a rocking horse, a teddy bear by the bucket.

## Later

- On the Block Tower spiral the wood grain squashes a little on the inner edge (UVs follow the middle line). Fine at speed (fresh review note).
- The Desk Drop wood reads more orange than the icon's pale wood. One color in `TRACKS` if BC wants it paler.
- `tools/make_icon.py` stops when a marble reaches past the centre two thirds, but no test makes that guard fail, and no test checks the one-color icon lines up with the painting. Checked by eye in 0.6.1 (fresh review notes).
- Headless runs end with "resources still in use at exit" after the ok line. Also there on 0.6.0. Not a test failure (0.6.1 build note).
- The wall camera check in `_place_cam()` runs every frame of a normal game. Harmless, only test commands set it (fresh review note).
- `tools/common/release_check.py` looks for `const VERSION: String`, and `main.gd` writes `const VERSION :=`, so that one check passes without checking. A kit matter: propose it to BC for `common/` (fresh review note).
- Suno or Patch.gg race music per track.

- Track tiles on Basis Universal: about 1 MB smaller, but the test browser drew the Desk Drop too slowly and the race test failed (0.8.0). Retry once the browser test reads progress, not a 60 s distance.
- The table wall keeps a thin strip of painted tile at its bottom edge: the chair legs reach the edge (0.8.0 cut 0.003). A repaint with a deeper floor strip fixes it.
- A pale marble (Pearl, Galaxy's cream side) blends a little into the cream checks on Table Run (0.8.0 look check).

- WARMUP in `race_check.gd` checks a lower bound on materials warmed, not that the marble, ghost and gate materials are among them (fresh review, 0.8.0).
- `_marble_node()` makes new marble materials each race (E2.3). Godot caches the shaders, so the warm-up still covers them (fresh review note, 0.8.0).

## Not planned (they break the pillars)

- Marbles that break, lives or a game over.

## Decisions from BC

- 2026-11-20, 1:49 PM: the idea, "a marble racer game where you're starting multiple marbles at the same time and they race down a hill through different areas", then "Down a track I should say".
- 2026-11-20, 1:57 PM: "2". You steer or tilt your own marble against the others.
- 2026-11-20, 2:05 PM: "I think Marble Rush."
- 2026-11-20, 2:06 PM: computer marbles, clean toy render, toy room first track.
- 2026-11-20, 2:14 PM: "move forward with the first few releases until its playable only stop me if you need me".
- 2026-11-20, 3:08 PM and 3:15 PM: a short boost that cools down before the next use, no big advantage.
- 2026-11-20, 4:13 PM: decision page picks. Start screen music Quirky Dog. Race music Hyperfun. Title font Luckiest Guy. Art direction clean toy render. Keep Marble Rush, no backup yet. Next track Kitchen.
- 2026-11-20, 3:34 PM: "first run was good except at the beginning all the marbles went through the floor initially for about 2 seconds and then it starting working correctly. review and then move on to the next release". Fixed in 0.3.0.
- 2026-11-20, 4:34 PM: "marble run plays good, move to the next release".
- 2026-11-20, 4:44 PM: decision page picks. APK icon Racing pack. Your marble Galaxy. Start screen scene Toy room run (now). Menu and page colors Toy room warm (now). Title font Luckiest Guy. Art direction clean toy render. Game Shelf card picture Desk Drop pack. Start screen music Life of Riley. Race music Glitter Blast. Sound effects wooden toy. Calm level soft (now). Phone steering slide anywhere (now). Tagline "Eight marbles, one gate, first to the bucket". Keep Marble Rush, no backup yet. Next track Kitchen. Replaces the 4:13 PM music picks.
- 2026-11-22, 11:59 AM: "I want to add HD graphic backgrounds to the game instead of a blank background." 12:02 PM: "1, decision page". Painted walls (four per track), Toy Room first, picks on the decision page.
- 2026-11-22, 12:11 PM: decision page picks. "Marble Rush wall picks: Window wall: Window seat. Toy shelf wall: Cubby shelves. Bed wall: Bunk bed with a slide. Door wall: Chalkboard." The four picked drafts are the approved reference art (`art_src/reference/`).
- 2026-11-22, 4:53 PM: decision page pick. "Marble Rush icon pick: APK icon: Toy Room run." Replaces the Racing pack icon of 2026-11-20. Ships in 0.6.1.
- 2026-11-22, 5:33 PM: "can we improve the track and walls of the track? then move on to another level." Question card picks: "Look, match the icon", "The side rails", "Finish the Kitchen". The Kitchen moves ahead on his word, before his phone notes on the Toy Room walls (G4.13).
- 2026-11-22, 6:19 PM: decision page picks. "Marble Rush Kitchen wall picks: Sink wall: Window and blue cabinets. Fridge wall: Red fridge and breakfast shelf. Stove wall: Copper hood on blue. Table wall: Garden door and table." The four picked drafts are approved reference art (`art_src/reference/`).
- 2026-11-25, 4:05 PM: question card picks in the desktop app chat. Kitchen track surfaces: "Match the walls (Recommended)": butcher block wood on Counter Top, pale blue tile on Dish Rack, a red and cream checked tablecloth on Table Run, a smooth glazed Mixing Bowl. Release okay: "Yes, full release" (clone game-signing, sign the APK and push 0.8.0 with all six outputs).
