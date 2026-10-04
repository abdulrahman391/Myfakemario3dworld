# ⚙️ Gear Quest 3D

A 3D platformer in the spirit of Mario 3D World. It runs in the browser on desktop and mobile as a single `index.html` (Three.js loads from a CDN).

## Play
- **GitHub Pages:** push `index.html` and `README.md` to a repo, then go to Settings → Pages → deploy from `main` / root.
- **Locally:** open `index.html` in a browser (needs internet for the Three.js CDN).

## Heroes
| Hero | Colour | Attack |
|---|---|---|
| **Sprocket** (robot) | Grey | Water shot that freezes enemies. Frozen enemies are harmless, and hitting one again does double damage |
| **Flame** | Red | Bouncing fireballs |
| **Bull** | Dark red | Wide wind gust that pierces through enemies |

**Villain:** Evil Sprocket, Sprocket's red twin. He guards the end of every world and fires bolts. Beat him to reveal the goal flag.

## Worlds
1. Gear Meadow
2. Magma Foundry (lava)
3. Storm Sky Tower

Each world has static, sliding and rising platforms, coins and patrolling enemies.

## Power-ups
- 🟢 **Gear:** +1 health
- 🟡 **Star:** invincible for 8 seconds
- 🩷 **Spring Boots:** faster and higher jumps for 12 seconds

## Controls
| | Player 1 | Player 2 (Local) |
|---|---|---|
| Move | WASD | Arrow keys |
| Jump | Space | Enter |
| Attack | F | Right Shift |

Rotate the camera with **Q/E** or by dragging. **Mobile:** left stick to move, **A** to jump, **B** to attack, drag to turn the camera. Stomping on enemies also hurts them.

## Multiplayer
- **Local 2P:** two players on one keyboard with a shared camera.
- **Online / local network:** peer-to-peer over WebRTC, with no server needed.
  1. Host picks **Online** and presses **Host**, then sends the code to a friend.
  2. Friend picks **Online** and presses **Join**, pastes the code and presses **Connect**, then sends back the reply code.
  3. Host pastes the reply, presses **Connect**, then **START**.

  Player positions and attacks are synced. Enemies and pickups are simulated on each player's own device. Some strict networks block WebRTC.

## Physics
Platforms are axis-aligned boxes. The player is carried by the platform's movement each frame, with coyote time and jump buffering, plus side and head collision. Landing uses the previous frame's position, so fast falls don't tunnel through.

## Files
- `index.html`: the whole game
- `README.md`: this file
