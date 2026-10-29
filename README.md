# Bomberman World — [BombMan]

**Student:** [Xinyi Long]

## How to play

- **Controls:** [press WASD or arrow keys to move, press SPACE to place a bomb, press ENTER ro restart the game, and press Q/ESCAPE to quit.]
- **Objective and rules:** [The Winning condition is to destroy all the enemies; the defeat condition is that the player is destroyed(The player dies when touching enemies or explosions' flames), which result in "Victory!" or "Defeat!" shows on the screen; There are 3 power-ups(the little blue dot) on the map, collecting them will increase the power of your bomb.]
- **Configurations / demo setup:** [Default]

## Features and validation

| Feature | Check, observed result, and expected behaviour |
| --- | --- |
| 1. Player damage and death | [I made the player walked into an enemy and stood inside a bomb's blast area. The player was destroyed and the text "Defeat!" appeared, matching the expected bahaviour.] |
| 2. Round states and objective | [I change the size of map from (200, 120) into (40, 24) to help me test it more quickly, and deatroyed all the enemies. The game state immediately switched to "Victory!", showing the winning condition is correctly.] |
| 3. Safe restart | [After games over, I pressed ENTER. The game reset the score, bomb blast range, combo, and the number of enemies. Clearing all previous blast effects and bombs, and repopulated the map perfectly.] |
| 4. Solid bombs with owner escape | [I placed a bomb, stand still on it won't be pushed away, step off it, and walk back, the bomb acted as a solid wall blocking player to return.Matching the expected bahaviour.] |
| 5. Blast-range pickup | [I picked up a power-up and placed a bomb, the range of blast spanned further than the default range, the value for the blast range displayed in the top_left corner is also right.] |
| [# Extension 1: Scoring and combos] | [First, I adjusted the combo countdown from 5.0 seconds to 10.0 seconds to make testing easier.I then defeated two enemies within the countdown. I found the score increase with a rising combo multiplier, and the multiplier corrretly reset to 1x when no enemy was defeated after 10 seconds] |
| [# Extension 2: Entities and ownership] | [I rapidly pressed SPACE, but I can place at most 5 bombs at the same time. Once a bomb detonated and left the active-bomb list, my capacity instantly recovered, allowing me to place another.] |
| [# Extension 3: Chain reactions] | [I placed two bombs within each other's blast range. The fist explosion's flame will immediately trigger the second bomb, causing it to detonate prematurely with no loop crash occurring.] |

Example: “I ended a round with live bombs and restarted three times to check that old-round state was cleared. No old explosions appeared, and bomb capacity reset each time.” Report your actual results, including any failures or remaining limitations; stating that something “works” does not describe a check.   

**Known issues:** [None known after testing]

## Sources and assistance

This project builds on the shared Kotte foundations.

[A friend helped me understand C++ const restrictions and how to use std::ranges syntax.I reviewed and applied the conceptes in my own code.]
