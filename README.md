# Dice Brawl

A pixel-art dice-throwing prototype. Pick a die, drag it and flick it across a board full of zones and obstacles to defeat the Golem in as few throws as possible.

**Play it:** https://enricomartina97.github.io/dice-brawl/

## How to play

1. Click **START**.
2. Pick a die from the tray (d4 to d20). Bigger dice roll farther and bounce more, but need a few turns to recharge (CD).
3. Drag the die in the launch area and release it with a flick. The faster the flick, the stronger the throw.
4. When the die stops, its face is the damage. The zone it stops on changes that value.
5. After each throw the Golem attacks you, shuffles the zones or moves the obstacles at random.

Win before your HP runs out. Fewer throws earn more stars (3 stars at 6 throws or fewer, 2 at 9 or fewer).

### Zones (apply where the die stops)

| Zone | Effect |
|---|---|
| x2 | Damage x2 |
| +2 / -2 | Damage +2 / -2 |
| INV | Inverts the face (N+1-value) |
| VOID | No damage |
| ROLL+ | Rolls the die again and adds the result |

### Obstacles (apply when hit)

| Obstacle | Effect |
|---|---|
| Bumper (orange) | Pushes the die away faster |
| Rune (+1) | +1 to the die |
| Spikes (-1) | -1 to the die |
| Crystal | Breaks and clones the die |
| Pillar (grey) | Plain bounce |

## Running locally

Open `index.html` in a browser. It is a single file; it loads [Matter.js](https://brm.io/matter-js/) for physics and the Press Start 2P font from public CDNs, so it needs an internet connection.

Balance values (HP, enemy damage, throw strength, star thresholds) are in the `CONFIG`, `DICE` and `ZONE_TYPES` objects at the top of the script.
