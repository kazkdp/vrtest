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

The same idea as Meta's mixed-reality demo *First Encounters*, with our own creature: little black holes ("space holes") pop open in the air around your room, and cute space critters called Fluffkins come out to bounce around. You catch them with bubbles.

1. Put the **jar mat** on a table or the floor and press **Lock & Play**. Choose **2 minutes** or **No timer**, then press **Start**.
2. A space hole tears open in front of you: a black disc with a bright edge and a slowly turning violet and cyan swirl. More open at random spots over the round (up to two at once); each lets out two to four Fluffkins and then closes.
3. Each Fluffkin squeezes out, floats at the mouth of the hole for a moment, then jumps down and bounces around the floor and onto tables and sofas. They watch you, hop away if you get too close, and watch bubbles float by.
4. **Blow bubbles**: pull the trigger (each controller holds a chunky toy bubble blaster, about 22 cm long), pinch with a bare hand, or click on a screen. **Tap** for a small, fast bubble; **hold** to blow a big one (easier to hit, a bit slower), and let go to send it. A small bubble crosses 2 m in about a fifth of a second. There is no aim help: a bubble goes where you point it, slows down in the air, then floats, slowly sinks, thins and pops. It pops on walls, the floor and tables, and a space hole swallows it.
   - **Aim guide:** a faint dotted line shows the path your bubble will take (brighter while you blow). It turns the Fluffkin's colour and puts a ring round it when you are on target.
5. A caught Fluffkin floats up in its bubble and flies into the jar. **Combos:** catch the same colour again and again for ×2, ×3, up to ×5 points. Three colours are about at a time, and one changes every 30 seconds. **Bonuses** of 50: a long shot (over 2.6 m), a mid-air catch (while it hops), and a quick catch (while it is still at its hole).
6. When time is up the holes suck the Fluffkins back in and close. Your score, best score and biggest combo are on the sign. Hold **stop** to finish early.

- **The Fluffkin:** one model in six colours (pink, green, blue, yellow, purple, orange), styled like a soft vinyl toy: a smooth velvety coat with a glossy shine, a cream tummy and soft lighter spots on the back, big glossy eyes that glow in its own colour with two sparkles, a tiny "ω" mouth and blush, rounded ears with pink insides, little paws that wave, feet, a cream pom-pom tail and an antenna with a glowing bulb. Everything wobbles on springs; it squashes and stretches on every hop and has happy ^ ^ eyes when caught.
- **Your room:** in **Play in my room** the Quest room scan (Space Setup) gives the real floor, walls and furniture tops, so Fluffkins land on them and bubbles pop on them; the holes open inside the room. With no room scan it uses pretend walls around you (and says so). **Play in a calm world** and the screen preview use a cosy pretend playroom. On a screen the holes open in front of you.
- Settings stored in the browser: `fluff:timed` (the timer switch) and `fluff:best` (best score).

## Riftlings MR (`riftlings-mr.html`), made by Gemini

A second take on the same First Encounters idea, written by Gemini and published here **exactly as it was supplied** (the file is byte-for-byte the original, so the two can be tested side by side). It is not built on the Play Lab kit, so it plays differently from the other games:

- Choose **Enter Mixed Reality (Quest 3)**, then shoot the glowing crystal beacon under the little saucer to start a 90 second round. There is no play mat to set up or lock.
- Both controllers are blasters: tap for a rapid bolt, hold the trigger for a charged nova. You can also shoot the walls (twice, or once charged) to crack open your own portals.
- Six fluffy "Riftlings" with different behaviours (a boss and armoured ones take several hits). Captured ones are beamed up into the saucer.
- **Creature Lab** (a button on its menu) lets you look at each colour up close. **Play Desktop Demo** runs it on a screen.
- There is no link back to this menu from inside it; use the browser's Back button.
- three.js r169 loads from jsDelivr (the other games use r170 from unpkg).

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

## Hex Game Experiments (`hex-lab.html`)

A test bed for new games built from Hex Power. It is a second touch wall (the same set-up, lock, **Games** button and padlock as the Power Wall) with its own menu of experiments. Each one reuses Hex Power's pieces: the honeycomb of hex sockets, glowing hex tiles that pop in and breathe, hex ripples, energy racing along a conduit into the reactor, the same colours and sounds. Hex Power itself (in `power-wall.html`) is not changed. The wall starts at the size the Power Wall was last set to (`kidxr:hexlab:wall` after that).

| Experiment | What happens | What it tries out |
| --- | --- | --- |
| **Power Path** (`?game=path`) | A gold power hex on one side, a dark lamp on the other. Slide a hand across the hexes to lay a path of light from the power to the lamp; each hex must touch the end of the path (one skipped hex is filled in). Touch the path to go back to that hex. When it reaches the lamp, energy runs along the path and the lamp lights up. Stage 1 shows a dotted trail; later the trail only appears after 7 seconds without progress. Stage 2 adds bonus stars just off the straight route; stage 3 on adds rock walls to go round | Planning a route, sliding rather than tapping, undo by touching back |
| **Chain Reaction** (`?game=chain`) | Every hex is filled with a colour. Touch one and every touching hex of the same colour bursts too, ring after ring, rising up the scale, and the energy flies into the reactor. New hexes pop back in, often next to the same colour. A chain of 7 or more leaves a white star hex: touch it for a blast that clears everything within two rings. Fill the reactor (40, 50, 60...) for the next stage; stages go from 3 to 5 colours | One touch, big result; colour grouping |
| **Hex Match** (`?game=match`) | Memory pairs on hex cards round the reactor. All cards flip up for a look, then back. Touch two: a match lights up and powers the reactor; a miss flips back after a moment. 3 pairs, then 4, 5, 6, 7, 8. Twelve pictures (heart, star, circle, triangle, moon, square, flower, drop, lightning, diamond, sun, cross) | Memory, turn-taking, no clock |
| **Hex Beats** (`?game=beats`) | A music maker. Each row is a sound: bottom row drum, next row clap, every row above a note, higher as you go up (one pentatonic scale, so anything sounds nice). A bar of light sweeps across and plays every lit hex. Touch to light or unlight; a slide paints a line (the first hex decides whether the slide lights or clears). Starts with a little tune; hold **Clear** to empty it, then the same button says **Tune** to bring the tune back | Free creative play, cause and effect, high/low |

- Every experiment ignores the finger that chose it on the menu until that finger lifts, so the game never starts with a stray touch.
- `hex-lab.html` is put together from `power-wall.html` (page head, PLAY LAB KIT and wall code copied unchanged) plus the new games after the `GAME: Hex Lab` comment. A new hex experiment goes in as one more `registerGame(...)` with a picture in `tileArt`.

## How the files are built

- Each game is one self-contained `.html` file, linked from `index.html` (the menu). three.js r170 loads from unpkg.
- Every game contains an identical copy of the **PLAY LAB KIT** (`createKit`, v1.3; v1.2 added wall mode for the Power Wall, v1.3 stretchable walls) followed by the game's own code. The kit handles the set-up/lock flow, hands, controllers and mouse, touch zones, grabbing (including tools that turn with your hand), 3D buttons, sound, effects, the VR meadow and the screen preview. If you change the kit, change it in every game file.
- To make a new game: copy any game file, keep the kit section, replace the code after the `GAME:` comment, and add a card to `index.html`. The one exception is `riftlings-mr.html`, a finished page from another author that is copied in untouched and has only a card on the menu.
- Settings stored in the browser: the sound level (`kidxr:sound`, shared by all games), each game's mat or wall size (`kidxr:<game>:scale`, and `kidxr:powerwall:wall` / `kidxr:hexlab:wall` for the two walls), Hex Power's timer switch (`kidxr:pw:hexRelaxed`) and Fluffkin Catch's timer switch and best score (`fluff:timed`, `fluff:best`).
- The games were tested in headless Chrome with Meta's Immersive Web Emulation Runtime (an emulated Quest 3 with controllers and tracked hands), including the Table snap, the Power Wall's Wall snap and Fluffkin Catch in captured rooms. Feel on a real headset (hand sizes, reach, sound levels, how easy it is to tip the can or dip a wand, how well the wall lines up with a real wall, how smoothly Fluffkin Catch runs with many Fluffkins in the room) still needs checking on the Quest.
- The original wall version of Hex Power Wall, Rainbow Xylophone, Feed Nomi and Block Tower are in the git history if they are ever needed again.
