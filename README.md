# Play Lab (vrtest)

Super-simple WebXR games for Meta Quest 3, for young children and for kids who like things calm and predictable. Open the GitHub Pages site (normally https://kazkdp.github.io/vrtest/) in the Meta Quest Browser and pick a game from the menu.

Every game works the same way:

1. Choose **Play in my room** (mixed reality, the real room stays visible) or **Play in a calm world** (a quiet virtual meadow).
2. Grab the play mat and put it on a table or the floor. The panel behind it has Bigger / Smaller, Bring here, Table (snaps onto a table the Quest has scanned), Floor and Exit.
3. Press **Lock & Play**. The mat now stays put. Hold the small padlock for 2 seconds to unlock it.

No timers, no scores to beat, no way to lose. Hands and controllers both work, and every game can also be tried on a normal screen ("Try it on this screen instead").

| File | Game | What it shows |
| --- | --- | --- |
| `bubbles.html` | **Bubble Pop**: touch bubbles to pop them; pinch and wave to blow more; a giant bubble with a star every 12 pops | Touch with all ten fingers, gesture input, 3D sound, custom shader |
| `shape-sorter.html` | **Shape Sorter**: post shapes through matching holes; the right hole glows and shapes are pulled in when close; 3 to 5 shapes | Pick up and place, snapping, errorless hints |
| `xylophone.html` | **Rainbow Xylophone**: tap bars to play; "Play a song" demonstrates a tune, then lights the next bar for the child | Synthesised music, tap strength, follow-along sequencing |
| `feed-nomi.html` | **Feed Nomi**: bring food to Nomi's mouth; the thought bubble shows the favourite; Nomi burps after five | A reacting character, eyes that follow held objects, ask-and-reward |
| `block-tower.html` | **Block Tower**: knock the tower down, stack blocks, "Build again" flies them home (tower, pyramid, two towers) | Real physics (cannon-es), hands that push, throwing, collision sounds |
| `magic-paint.html` | **Magic Paint**: dip a finger in a paint pot, pinch and move to paint glowing ribbons in the air; hold Clear | Free 3D drawing, geometry built live |
| `hex-power-wall.html` | **Hex Power Wall** (the first test): a wall panel with timed colour waves | Snap to a real wall |

## How the files are built

- Each game is one self-contained `.html` file, linked from `index.html` (the menu). three.js r170 loads from unpkg; Block Tower also loads cannon-es 0.20.
- The six Play Lab games each contain an identical copy of the **PLAY LAB KIT** (`createKit`) followed by the game's own code. The kit handles the set-up/lock flow, hands, controllers and mouse, touch zones, grabbing, 3D buttons, sound, effects, the VR meadow and the screen preview. If you change the kit, change it in every game file.
- To make a new game: copy any game file, keep the kit section, replace the code after the `GAME:` comment, and add a card to `index.html`.
- Settings stored in the browser: the sound level (`kidxr:sound`, shared by all games) and each game's mat size (`kidxr:<game>:scale`).
- The games were tested in headless Chrome with Meta's Immersive Web Emulation Runtime (an emulated Quest 3 with controllers and tracked hands), including the Table snap against captured rooms. Feel on a real headset (hand sizes, reach, sound levels) still needs checking on the Quest.
