# Ice Cube Run

**You're melting. Get to the freezer.**

A browser game for ClassJam 440. Theme: **Shrinking**.

Open `index.html` in Chrome — that's it. One file, vanilla JS + HTML5 Canvas,
no libraries, no images, no sound files. Every sprite is drawn in code.

## The idea

Your size *is* your health bar, and it's also your hitbox.

- Size starts at 100 and drains ~1/sec just from existing.
- **Sun** (yellow) melts you at 8/sec. **Shade** (dark blue) stops melting entirely.
- **Snowflakes** give back +15, capped at 100.
- Smaller = faster, but smaller also = closer to dead.
- Some walls have slots only a small cube fits through, so sometimes you have to
  melt *on purpose* to get through, then refill on the far side.

Hit 0 and you're a puddle.

## Controls

| Key | Action |
|-----|--------|
| WASD / Arrow keys | Move (8-directional) |
| R | Restart the current level |
| Enter / Space | Start, and advance between screens |

## Levels

1. **Tutorial** — one sun patch, one shade patch, two snowflakes. Learn what melts you.
2. **The slot** — the freezer is behind a 26px gap. Melt to fit, then refill.
3. **Finale** — a sun corridor, two slots of different widths (34px and 24px), and two
   sweeping sun beams moving out of phase. There's a safe lane between the beams.

The whole game runs well under 5 minutes.

## Beatability

All three levels were machine-verified beatable: a search over
(position × size) states — where shrinking is only allowed inside a sun patch,
exactly as the game works — finds a surviving route to the freezer on every level
**without collecting a single snowflake**. The snowflakes are the safety margin,
not the solution.
