# GAMMA Bleed Fix

Shows a screen bleed effect only while the player actor is actually bleeding.

## What this mod does

- Plays `dorn_bleed.ppe` on a loop while `actor.bleeding > 0`
- Leaves stock damage blood splash (`blood_splash` / `bloody.ppe` hit flashes) alone
- Development options: refresh keybind, **Always cycle effect** toggle for testing without bleeding

## Editing the effect

1. Open `gamedata/anims/dorn_bleed.ppe` in **X-Ray SDK Postprocess Editor**
2. Save your changes
3. In-game: bind **MCM → Dorn's Bleed Fix → Development → Refresh bleed effect**, then press it to reload

The refresh key replays the effect immediately so you can iterate without reloading the save.

## Installation

1. Install with Mod Organizer 2 like any other mod
2. **Requires [Dorns Common](https://github.com/JoshuaCarter/GAMMA-Common/releases)** — enable it **above** this mod in load order
3. Place below mods that change player visual effects if you see conflicts

Releases: https://github.com/JoshuaCarter/GAMMA-Bleed-Fix/releases

## Files

- `gamedata/anims/dorn_bleed.ppe` — bleed screen effect (forked from stock `bloody.ppe`)
- `gamedata/scripts/dorn_bleed_fix_main.script` — bleed loop logic
- `gamedata/scripts/dorn_bleed_fix_mcm.script` — MCM + dev refresh keybind
