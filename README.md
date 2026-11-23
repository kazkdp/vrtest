# Play Lab (vrtest)

Super-simple WebXR games for Meta Quest 3, for young children and for kids who like things calm and predictable. Open the GitHub Pages site (normally https://kazkdp.github.io/vrtest/) in the Meta Quest Browser and pick a game from the menu.

Every game works the same way:

1. Choose **Play in my room** (mixed reality, the real room stays visible) or **Play in a calm world** (a quiet virtual meadow).
2. Grab the play mat and put it on a table or the floor. The panel behind it has Bigger / Smaller, Bring here, Table (snaps onto a table the Quest has scanned), Floor and Exit.
3. Press **Lock & Play**. The mat now stays put. Hold the small padlock for 2 seconds to unlock it.

No scores to beat and no way to lose. Hex Power is the only game with a timer, and it has a switch to turn the timer off. Hands and controllers both work, and every game can also be tried on a normal screen ("Try it on this screen instead").

| File | Game | What it shows |
| --- | --- | --- |
| `bubbles.html` | **Bubble Pop**: a soap tub, two bubble wands in a stand and a bubble machine. Wave a wand slowly for one big wobbly bubble or quickly for a stream; dip the ring when the soap runs out; press the machine's button for a burst; touch bubbles to pop them | Soap-film shader (rainbow swirls, thinning, popping), tools that turn in your hand, air you can push |
| `shape-sorter.html` | **Shape Sorter**: a bigger table with three toys that take turns: a shape box, a puzzle board with outlines, and coloured buckets for sorting by colour. 13 shapes, 8 colours, up to 8 pieces a round, look-alike pairs later on | Pick up and place, magnetic snapping, gentle hints |
| `piano-arcade.html` | **Piano Arcade**: eight giant arcade-style keys (blue and green halves) under a light-up tile screen. Six instruments (piano, xylophone, bells, guitar, organ, drums). "Play a song" shows the song, then waits for the key under the lit tile; 7 songs | Synthesised instruments, follow-along sequencing, a big readable screen |
| `magic-paint.html` | **Magic Paint**: dip a finger in a paint pot, pinch and move to paint glowing ribbons in the air; hold Clear | Free 3D drawing, geometry built live |
| `garden.html` | **Little Garden**: a raised flower bed with five seeds. Tip the watering can over a plant (or press Rain for a smiling rain cloud) and it grows: shoot, leaves, bud, flower. Flowers bring butterflies that visit them and land on a still fingertip. Hold New seeds to start again | Tip-to-pour, things that grow over time, creatures that come to you |
| `hex-power-wall.html` | **Hex Power**: the first test game (Hex Power Wall), now on the shared play mat. Tap the lit hexagons of the stage colour; their energy flows into the reactor in the middle; stars count double; from stage 3 the targets hop. Timer can be switched off | Fast tapping, energy effects |

## How the files are built

- Each game is one self-contained `.html` file, linked from `index.html` (the menu). three.js r170 loads from unpkg.
- Every game contains an identical copy of the **PLAY LAB KIT** (`createKit`, v1.1) followed by the game's own code. The kit handles the set-up/lock flow, hands, controllers and mouse, touch zones, grabbing (including tools that turn with your hand), 3D buttons, sound, effects, the VR meadow and the screen preview. If you change the kit, change it in every game file.
- To make a new game: copy any game file, keep the kit section, replace the code after the `GAME:` comment, and add a card to `index.html`.
- Settings stored in the browser: the sound level (`kidxr:sound`, shared by all games), each game's mat size (`kidxr:<game>:scale`) and Hex Power's timer switch (`kidxr:hex:relaxed`).
- The games were tested in headless Chrome with Meta's Immersive Web Emulation Runtime (an emulated Quest 3 with controllers and tracked hands), including the Table snap against captured rooms. Feel on a real headset (hand sizes, reach, sound levels, how easy it is to tip the can or dip a wand) still needs checking on the Quest.
- The original wall version of Hex Power Wall, Rainbow Xylophone, Feed Nomi and Block Tower are in the git history if they are ever needed again.
