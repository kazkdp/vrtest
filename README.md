# Play Lab (vrtest)

Super-simple WebXR games for Meta Quest 3, for young children and for kids who like things calm and predictable. Open the GitHub Pages site (normally https://kazkdp.github.io/vrtest/) in the Meta Quest Browser and pick a game from the menu.

Every game works the same way:

1. Choose **Play in my room** (mixed reality, the real room stays visible) or **Play in a calm world** (a quiet virtual meadow).
2. Grab the play mat and put it on a table or the floor. The panel behind it has Bigger / Smaller, Bring here, Table (snaps onto a table the Quest has scanned), Floor and Exit.
3. Press **Lock & Play**. The mat now stays put. Hold the small padlock for 2 seconds to unlock it.

No way to lose. Fluffkin Catch keeps a score and Hex Power has a timer, and both have a switch to turn the timer off. Hands and controllers both work, and every game can also be tried on a normal screen ("Try it on this screen instead").

## Table games

| File | Game | What it shows |
| --- | --- | --- |
| `bubbles.html` | **Bubble Pop**: a soap tub, two bubble wands in a stand and a bubble machine. Wave a wand slowly for one big wobbly bubble or quickly for a stream; dip the ring when the soap runs out; press the machine's button for a burst; touch bubbles to pop them | Soap-film shader (rainbow swirls, thinning, popping), tools that turn in your hand, air you can push |
| `shape-sorter.html` | **Shape Sorter**: a bigger table with three toys that take turns: a shape box, a puzzle board with outlines, and coloured buckets for sorting by colour. 13 shapes, 8 colours, up to 8 pieces a round, look-alike pairs later on | Pick up and place, magnetic snapping, gentle hints |
| `piano-arcade.html` | **Piano Arcade**: eight giant arcade-style keys (blue and green halves) under a light-up tile screen. Six instruments (piano, xylophone, bells, guitar, organ, drums). "Play a song" shows the song, then waits for the key under the lit tile; 7 songs | Synthesised instruments, follow-along sequencing, a big readable screen |
| `magic-paint.html` | **Magic Paint**: dip a finger in a paint pot, pinch and move to paint glowing ribbons in the air; hold Clear | Free 3D drawing, geometry built live |
| `garden.html` | **Little Garden**: a raised flower bed with five seeds. Tip the watering can over a plant (or press Rain for a smiling rain cloud) and it grows: shoot, leaves, bud, flower. Flowers bring butterflies that visit them and land on a still fingertip. Hold New seeds to start again | Tip-to-pour, things that grow over time, creatures that come to you |

## Fluffkin Catch (`fluff-catch.html`)

The same idea as Meta's mixed-reality demo *First Encounters*, with our own creature: something knocks on the walls of your room, cracks spread and glow, the wall bursts open, and fluffy little space critters come through to bounce around your room. You catch them with bubbles.

1. Put the **jar mat** on a table or the floor and press **Lock & Play**. Choose **2 minutes** or **No timer**, then press **Start**.
2. A hole opens in front of you, then two more over the round (about 25 s and 60 s in). Through each hole you can see the Fluffkins' world: a violet sky with a ringed planet, glowing moss, mushrooms and crystals.
3. The Fluffkins peek out, hop to the edge, jump down and bounce around the floor and onto tables and sofas. They watch you, hop away if you get too close, and sometimes dodge a bubble.
4. **Shoot bubbles**: pull the trigger (each controller becomes a little bubble blaster), pinch with a bare hand, or click on a screen. Hold to keep blowing. Bubbles curve gently towards the nearest Fluffkin.
5. A caught Fluffkin floats up in its bubble and flies into the jar, where it joins the others. **Combos:** catch the same colour again and again for ×2, ×3, up to ×5 points. Three colours are about at a time, and one changes every 30 seconds.
6. When time is up the Fluffkins hop back home and the holes heal. Your score, best score and biggest combo are on the sign. Hold **stop** to finish early.

- **The Fluffkin:** one model in six colours (pink, green, blue, yellow, purple, orange). Real fur made from stacked "shells" that trails behind when it moves, big glossy eyes that blink and look at you, round ears and an antenna with a glowing bulb on springs, squash and stretch on every hop, and happy ^ ^ eyes when caught.
- **Walls:** in **Play in my room** the holes open in your real walls from the Quest room scan (Space Setup), and the Fluffkins land on your real floor and furniture tops. Your walls are drawn as invisible "occluders" so the other world only shows through the holes. With no room scan it builds pretend walls around you instead (and says so). **Play in a calm world** and the screen preview use a cosy pretend playroom.
- Settings stored in the browser: `fluff:timed` (the timer switch) and `fluff:best` (best score).

## Power Wall (`power-wall.html`)

Like the touch walls with projectors at play centres (Lü, BEAM and similar): one big wall, many games.

1. **Set the wall up.** Choose **Play in my room** and a big glowing wall appears.
   - Drag the **yellow corners** to stretch it to any width and height; the opposite corner stays put.
   - Grab the **GRAB HERE TO MOVE** bar on top to move it.
   - Press **Wall** to snap it flat onto the real wall you're facing. After that, moving it slides it along that wall.
   - **Bigger**, **Smaller**, **Up**, **Down** and **Bring here** are on the floating panel.
2. **Lock & Play.** The wall shows its own game menu. Touch a game to start it; every game fills the wall at the size you set.
3. **Switch games:** hold **Games** in the bottom corner.
4. **Change the wall:** hold the padlock beside its lower right corner. If you resize it, the game you were playing comes back re-fitted when you lock again.

| Game | What happens |
| --- | --- |
| **Hex Power** | The original Hex Power Wall game: tap the lit hexagons of the stage colour to power the reactor; stars count double; from stage 3 they hop. Timer switch in the corner |
| **Reaction Lights** | Pads light up anywhere on the wall; slap each before its ring closes in. More light at once as you go; streaks |
| **Colour Call** | The wall calls a colour ("RED!") and its edge glows in it; hit only the drifting orbs of that colour. A new colour every six hits |
| **Meteor Shower** | Fiery rocks fall towards a little planet; smash them before they land. Golden meteors burst into stars. Any that get through bump off the shield |
| **Brick Breaker** | Bat a glowing ball with your hand anywhere on the wall to smash the bricks. At the bottom it just bounces back slowly |
| **Simon Wall** | Four pads, each with a colour, shape and note. Watch the pattern, copy it, and it grows by one. A mistake replays it |
| **Splat Attack** | Bugs scuttle across a tiled wall; touch one and it bursts into paint that stays on the wall |
| **Throw!** | Pinch (or press the trigger) away from the wall to pick up a ball, swing and let go. A helper bends the ball towards the nearest target. On a screen, click to throw |
| **Balloon Pop** | Balloons float up the wall; touch to pop. Star and rainbow balloons have surprises |
| **Join the Stars** | Touch numbered stars in order; the picture fills in and comes alive |
| **Window Wipe** | Wipe the misty window with an open hand to find the picture behind |

Each game is one simple level, there to show the idea. Every touch shows a soft glow under the finger and a ripple where it lands. The menu cards open the wall with a game already chosen (`power-wall.html?game=lights`, `colours`, `meteors`, `bricks`, `simon`, `splat`, `throw`, `hex`, `balloons`, `stars`, `wipe`); it is chosen as soon as you lock the wall. The wall's size is remembered (`kidxr:powerwall:wall`).

## How the files are built

- Each game is one self-contained `.html` file, linked from `index.html` (the menu). three.js r170 loads from unpkg.
- Every game contains an identical copy of the **PLAY LAB KIT** (`createKit`, v1.3; v1.2 added wall mode for the Power Wall, v1.3 stretchable walls) followed by the game's own code. The kit handles the set-up/lock flow, hands, controllers and mouse, touch zones, grabbing (including tools that turn with your hand), 3D buttons, sound, effects, the VR meadow and the screen preview. If you change the kit, change it in every game file.
- To make a new game: copy any game file, keep the kit section, replace the code after the `GAME:` comment, and add a card to `index.html`.
- Settings stored in the browser: the sound level (`kidxr:sound`, shared by all games), each game's mat or wall size (`kidxr:<game>:scale`), Hex Power's timer switch (`kidxr:pw:hexRelaxed`) and Fluffkin Catch's timer switch and best score (`fluff:timed`, `fluff:best`).
- The games were tested in headless Chrome with Meta's Immersive Web Emulation Runtime (an emulated Quest 3 with controllers and tracked hands), including the Table snap, the Power Wall's Wall snap and Fluffkin Catch's holes in scanned walls against captured rooms. Feel on a real headset (hand sizes, reach, sound levels, how easy it is to tip the can or dip a wand, how well the wall lines up with a real wall, how smoothly Fluffkin Catch runs with many Fluffkins in the room) still needs checking on the Quest.
- The original wall version of Hex Power Wall, Rainbow Xylophone, Feed Nomi and Block Tower are in the git history if they are ever needed again.
