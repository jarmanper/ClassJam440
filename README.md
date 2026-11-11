# Ice Cube Run 3D

**You're melting. Get to the freezer.**

Class Jam 440 entry. Theme: **Shrinking**. This is the `3d` branch; `main` has the original 2D version.

Open `index.html` in Chrome. One file; it loads three.js from a URL (allowed by the jam rules), so it needs an internet connection.

## How the theme changes what you do

Your size is your health bar, your hitbox, and your speed. Some walls have slots only a small cube fits through,
so you have to melt *on purpose* in the sun to get through, then eat snowflakes to grow back before you run out.
Small cubes also outrun the dog.

## Controls

WASD / Arrow keys move. R restarts the level. Enter / Space starts and advances screens.

## What melts you

| Thing | Effect |
|---|---|
| Just existing | -1.5 / sec |
| Sun patch / sweeping beam | -12 / sec |
| Hot tile (red) | -20 / sec |
| Dog lick | -8 and a shove (dogs won't enter shade; small cubes outrun them) |
| Seagull dive | -10 (it marks you with a shadow first - step off it) |
| Shade | stops all melting |
| Snowflake | +12 |

## Levels

1. Tutorial. Sun, shade, snowflakes, no hazards.
2. The slot (26px) plus a dog and hot tiles.
3. Two slots (34px, 24px), sweeping beams, two dogs, a seagull.

All three levels are machine-verified beatable without collecting a single snowflake (see the `3d` branch history);
the snowflakes are your margin for mistakes.
