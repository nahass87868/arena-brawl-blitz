# Arena Brawl Blitz 3D

A chaotic 3D arena shooter that runs in the browser. Solo, co-op or versus, on desktop or phone.

The whole game is one file, `index.html`, built with [Three.js](https://threejs.org) r128 (loaded from cdnjs). There is no build step.

## Modes
- **Solo**: 3 lives against bomb bots. Works on mobile with touch controls and auto-aim.
- **Co-op**: two players on one keyboard, shared team score, no player-vs-player damage.
- **Versus**: two players on one keyboard, highest score wins, ring-outs count as kills.

Round length is selectable: 5, 10, 15, 20 or 30 minutes.

## Controls
| | Player 1 | Player 2 |
|---|---|---|
| Move | WASD | Arrow keys |
| Shoot | Space | Enter |
| Jump (twice for double jump) | Left Shift | Right Shift |

In solo mode on desktop, Player 1 can use either WASD or the arrow keys. Esc ends the round.
On phones: left joystick to move, FIRE and JUMP buttons on the right. Landscape works best.

## Run locally
```bash
python3 -m http.server 8000
# open http://localhost:8000
```
Opening `index.html` directly also works. An internet connection is needed to load Three.js from the CDN.

## Deploy with GitHub Actions
1. Push this repo to GitHub with `main` as the default branch.
2. In the repo go to **Settings → Pages → Build and deployment → Source** and choose **GitHub Actions**.
3. Push to `main` (or run the workflow manually from the Actions tab). The game is published at `https://<your-username>.github.io/<repo-name>/`.

The workflow is in `.github/workflows/pages.yml`. It copies `index.html` into `_site/` and deploys that folder.
