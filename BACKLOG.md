# Marble Rush: backlog

Updated 2026-11-22. BC decides the order.

## Done

- v0.2.0 (2026-11-20): the gray box and the race in one release. One track in four parts (Desk Drop, Book Stairs, Rug Run, Block Tower), eight marbles, a gate with a 3, 2, 1 count, steering and hop, falls back to the checkpoint, the rug split, results with coins, six marbles to unlock, Easy, Normal and Hard, ten achievements.

- v0.3.0 (2026-11-20): fixed the marbles rolling inside the desk at the start (BC's first run), Patch.gg music, the Fredoka title font, time trial against your ghost (K11), three stars per race (G4.18), name tags over the computer marbles.

- v0.4.0 (2026-11-20): BC's picks applied (Quirky Dog, Hyperfun, Luckiest Guy, clean toy render, keep the name). The Kitchen, a second track: Counter Top, Dish Rack slalom, Table Run S curves, a spiral into the Mixing Bowl. Menu > Tracks. Each track keeps its own best, stars and ghost.

- v0.5.0 (2026-11-20): BC's full set of picks: Racing pack icon, Galaxy marble (Ruby stays free), Life of Riley, Glitter Blast, wooden toy sounds, the new tagline. New page pictures.

- v0.6.0 (2026-11-22): HD backgrounds, BC's ask. The Toy Room stands in four painted walls, BC's picks from the decision page: the window seat ahead of the gate, the cubby shelves, the bunk bed with a slide and the chalkboard. Painted at 4K through the Nano Banana art workflow, 2048 x 1152 in the game. Kit 1.27.0.

## Now

- BC plays 0.6 on his phone. Notes on the painted walls: strong enough or too soft, sharp enough up close, frame rate.
- The Kitchen walls, once BC likes the Toy Room (G4.13): a decision page with the window over the sink, the fridge, the stove and shelves and the table side.
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
10. Sharper walls up close: each wall as two textures side by side (about 13 MB more in the browser build, 58 of 70 MB used today).
11. Small motion in the painted room: dust in the sunbeams, twinkling fairy lights on the bunk bed, a toy train far off. Reduce motion holds them still.
12. Giant props between the track and the walls: a toy chest, a rocking horse, a teddy bear by the bucket.

## Later

- Before the Kitchen walls: the browser build is 58 of 70 MB (G6.16) because every wall ships in two texture formats. Four more walls the same way would pass the budget. Options: smaller Kitchen textures, one format per platform or a smaller engine build (fresh review note, 0.6.0).
- A missing wall painting prints its warning on every Toy Room rebuild, not once (fresh review note).
- The wall camera check in `_place_cam()` runs every frame of a normal game. Harmless, only test commands set it (fresh review note).
- `tools/common/release_check.py` looks for `const VERSION: String`, and `main.gd` writes `const VERSION :=`, so that one check passes without checking. A kit matter: propose it to BC for `common/` (fresh review note).
- Fix the `nofog` test command: it looks for the environment under `world`, but it lives under `stage` (found in the 0.6.0 build, not in play).
- `project.godot` still lists the 4.6 feature tag. The game runs on 4.7.2.
- Suno or Patch.gg race music per track.

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
