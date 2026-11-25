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

The same idea as Meta's mixed-reality demo *First Encounters*, with our own creature: little black holes ("space holes") pop open in the air around your room and cute space critters called Fluffkins pour out of them. You catch them with bubbles. Single player.

1. Put the **jar mat** on a table or the floor and press **Lock & Play**. The sign stands on a post above the jar. Choose **2 minutes** or **No timer**, a difficulty (**Gentle**, **Normal** or **Wild**), switch the **Music** on or off, and press **Start**. **Stickers** shows your sticker book and catcher level.
2. **Waves:** a hole tears open and Fluffkins pour out in a quick stream, flung out in arcs in every direction. Each wave is bigger (one hole, then two, then three); the next wave comes early if you have caught nearly all of them. In a timed round the last 22 seconds are the **Fluffkin Rush**: holes pouring non-stop. Without a timer the waves keep coming, with a rush every sixth wave.
3. **The Fluffkins play in your room:** they bounce around the floor and onto tables and sofas, wave at you cheekily, do zoomies, and hop away if you get too close. They also:
   - **hide behind furniture** (the far side from you) and **peek up** over it now and then: you can only catch one while it is peeking. In mixed reality, solid furniture from the room scan (sofas, beds, cabinets, not tables) gets an invisible block so a Fluffkin behind your real sofa is really hidden by it; furniture near the jar mat is left out so the mat and sign are never hidden. The pretend playroom has a little sofa and a toy box.
   - **cling to walls** like stickers, paws up, sliding slowly down, then hop off.
   - **raid your jar:** a few seconds into some waves a sneaky one hops onto the mat, tiptoes to the jar, pops the lid and lets the newest Fluffkin out. Catch the sneaky one before it gets there (+200), or catch the escaped one again ("Got it back!").
4. **Blow bubbles**: pull the trigger (each controller holds a chunky toy bubble blaster), pinch with a bare hand, or click on a screen. A bubble comes out **the moment you press**; **keep holding** to blow a big one (easier to hit, a bit slower) and let go to send it. A small bubble crosses 2 m in about a fifth of a second. There is no aim help: a bubble goes where you point it, slows down in the air, then floats, slowly sinks, thins and pops. It pops on walls, the floor, tables and solid furniture, and a space hole swallows it.
   - **Aim guide:** a dotted line shows the path your bubble will take. It turns the Fluffkin's colour and puts a ring round it when you are on target. On Wild it only shows while you blow a big one.
5. A caught Fluffkin floats up in its bubble and flies into the jar. **Combos:** the same colour again and again for up to ×5 points. A rare **golden Fluffkin** glitters, hops fast and is worth 500 (it keeps your combo going). **Bonuses:** long shot (over 2.6 m) and mid-air +50, wall catch +50, peekaboo +100, sneaky one +200, got it back +100.
6. When time is up the holes suck the Fluffkins back in and close. The sign shows your score, best score, biggest combo, golden catches and catcher level. Hold **stop** to finish early.

- **Difficulty:** **Gentle** has a much bigger catch area, about half as many Fluffkins, slower hops, a bright guide, no dodging and rare mischief. **Normal** is the standard game. **Wild** has more and faster Fluffkins, more hiding, climbing and jar raids, more dodging, four holes in the rush and no guide unless you blow a big bubble.
- **Sticker book:** 16 stickers kept between plays: one for each colour, the golden one, Combo ×5, 20 in a round, 3 mid-air, long shot, peekaboo, wall catch, sneaky one, rush hero (15 in the rush) and a Wild round (10+ caught on Wild).
- **Catcher level:** every Fluffkin you ever catch counts towards 11 levels, from New Catcher to Fluffkin Legend, shown with a progress bar on the sign.
- **Music:** a bouncy tune made in the page, which gets busier from the third wave and fastest in the rush.
- **The Fluffkin:** one model in six colours plus the golden one, styled like a soft vinyl toy, with glossy eyes that glow in its own colour, a "ω" mouth, ears with pink insides, waving paws and a glowing antenna. Each is only 6 draw calls, so a full rush stays light.
- **Your room:** in **Play in my room** the Quest room scan (Space Setup) gives the real floor, walls and furniture. With no room scan it uses pretend walls around you (and says so). **Play in a calm world** and the screen preview use a cosy pretend playroom. On a screen the holes open, and the Fluffkins land, where the camera can see them.
- Settings stored in the browser: `fluff:timed`, `fluff:music`, `fluff:level` (difficulty), `fluff:best`, `fluff:total` (Fluffkins ever caught) and `fluff:stickers`.

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

## Hex Wall (`hex-wall.html`)

Hex Power and three newer hexagon games on one touch wall (the same set-up, lock, **Games** button and padlock as the Power Wall). The wall starts at the size the Power Wall (or the old Hex Lab) was last set to, then keeps its own (`kidxr:hexwall:wall`). `hex-lab.html` (the earlier Hex Game Experiments test bed) now just forwards here.

Every new game has a **goal bar** across the top showing the level, what to aim for and the stars it is heading for, and ends each level with **1 to 3 stars**. They use the bright rainbow colours and the music from the old Hex Beats experiment: each colour has its own note from one happy (pentatonic) scale, and a backing groove (drum, clap, hi-hat, bass going C, A, F, G) plays along. **Music on / Music off** at the bottom right switches the groove for all of them (remembered as `kidxr:hexwall:music`). Nothing can be lost.

| Game | How it plays | Goal and stars |
| --- | --- | --- |
| **Hex Power** (`?game=hex`) | The original game, copied unchanged from `power-wall.html`: tap the lit hexes of the stage colour; their energy races into the reactor. | Fill the reactor; optional timer |
| **Hex Crush** (`?game=crush`) | Like Candy Crush. Swap two hexes that touch (slide from one to the other, or tap one then the other) to make a straight line of 3 or more of one colour, up and down or along either slant. They pop, the hexes above drop down and new ones fall in from the top, which can set off more lines (combos, each one higher up the scale). A swap that makes no line slides back. **Line up 4** for a striped hex that clears its whole column when it goes; **line up 5** for a rainbow hex: swap it with any colour to clear every hex of that colour. A hint wiggles two hexes after 6 seconds; if no swap is possible the hexes shuffle. 5 colours, 6 from level 4. | Collect the colours shown (level 1: 12 of one colour, then two colours, then three). 3 stars for using no more swaps than the par, 2 for up to 1.6 times it |
| **Power Path** (`?game=path`) | Slide a hand across the hexes to lay a path from the gold power hex to the lamp. Each new hex is the next colour of the rainbow and the next note up, so the path sings; touch the path to go back. Reaching the lamp plays the tune back along the path and lights it up. Dotted help trail on level 1 and after 7 seconds stuck; rocks to go round from level 3. | Pick up the 3 stars on the way (on level 1 one is right on the way). A star for each, at least 1 for lighting the lamp |
| **Hex Match** (`?game=match`) | Memory pairs on hex cards round the reactor. They all flip up for a look, then back. Every picture has its own colour and note and plays it when turned over, so a pair also sounds the same. 3 pairs, then 4, up to 8. | Find all the pairs. 3 stars for 0 or 1 misses |

- Every game ignores the finger that chose it on the menu until that finger lifts.
- `hex-wall.html` is put together from `power-wall.html` (page head, PLAY LAB KIT, wall code and the Hex Power game copied unchanged) plus the new games after the `HEX WALL: shared pieces` comment. Another game goes in as one more `registerGame(...)` with a picture in `tileArt`.

## How the files are built

- Each game is one self-contained `.html` file, linked from `index.html` (the menu). three.js r170 loads from unpkg.
- Every game contains an identical copy of the **PLAY LAB KIT** (`createKit`, v1.3; v1.2 added wall mode for the Power Wall, v1.3 stretchable walls) followed by the game's own code. The kit handles the set-up/lock flow, hands, controllers and mouse, touch zones, grabbing (including tools that turn with your hand), 3D buttons, sound, effects, the VR meadow and the screen preview. If you change the kit, change it in every game file.
- To make a new game: copy any game file, keep the kit section, replace the code after the `GAME:` comment, and add a card to `index.html`. The one exception is `riftlings-mr.html`, a finished page from another author that is copied in untouched and has only a card on the menu.
- Settings stored in the browser: the sound level (`kidxr:sound`, shared by all games), each game's mat or wall size (`kidxr:<game>:scale`, and `kidxr:powerwall:wall` / `kidxr:hexwall:wall` for the two walls), Hex Power's timer switch (`kidxr:pw:hexRelaxed`) and Fluffkin Catch's timer switch and best score (`fluff:timed`, `fluff:best`).
- The games were tested in headless Chrome with Meta's Immersive Web Emulation Runtime (an emulated Quest 3 with controllers and tracked hands), including the Table snap, the Power Wall's Wall snap and Fluffkin Catch in captured rooms. Feel on a real headset (hand sizes, reach, sound levels, how easy it is to tip the can or dip a wand, how well the wall lines up with a real wall, how smoothly Fluffkin Catch runs with many Fluffkins in the room) still needs checking on the Quest.
- The original wall version of Hex Power Wall, Rainbow Xylophone, Feed Nomi and Block Tower are in the git history if they are ever needed again.
