# HoovyTools

<img width="1919" height="1079" alt="Display" src="https://github.com/user-attachments/assets/93156f39-7cd5-4b90-9d73-6dda37d26e1c" />

## What is HoovyTools?

HoovyTools is a Blender addon to import and manipulate Source Filmmaker sessions, models, animations, and cameras directly inside Blender. It follows this workflow:

## Session Importer

- Imports an entire SFM session's contents into Blender, including models, their in-SFM names for animation import later on
- Configurable `SFM Usermod Path` via addon preferences
- Works in harmony with Source IO, calling it's IMPORT .MDL feature and it's the only dependency with non raw-Blender environments


## DMX Animation & Camera Importer

- Imports `.dmx` animation files directly onto matching armatures
- Imports `.dmx` cameras with `Quaternion Flip Fix` for sign-flipped rotation curves
- `Stereo Split` utility for HWM stereo camera setups
- Works on both `Blender 4.x` and `Blender 5.x` via a built-in animation API shim

## Shape Key & Flex Tools

- Imports SFM HWM flex controls as Blender shape keys
- `HWM Localvar Baking` converts flex driver chains into bakeable shape key animations
- `Symmetrize Shape Keys` mirrors left/right shape keys across an axis
- Bulk shape key import from `.dmx` files

## Source Engine Utils

- `Rig Fixer` repairs broken bone hierarchies using bundled reference DMX files for each TF2 mercenary class
- `Fix Eye Constraints` restores eye targeting constraints lost during import
- `Remove Drivers` strips Blender drivers from imported rigs for clean re-export
- `Reduce Lag` disables expensive viewport features on heavy SFM scenes
- `Organize Scene` groups imported objects into clean collections

---

## Installation

1. Download the latest `HoovyTools.zip` from the [Releases](../../releases) page
2. In Blender, open **Edit → Preferences → Add-ons → Install...**
3. Select the zip and enable **HoovyTools**
4. Set Your SFM `usermod` path in the addon preferences
5. The menu appears under **File → Import → Source Engine (HoovyTools)**

## Compatibility

Tested on `Blender 4.3` and `Blender 5.0.1`. Should work on Blender 4.0+ and 5.x via the built-in API shim.

## Credits

Bundles a subset of [Blender Source Tools](https://github.com/Artfunkel/BlenderSourceTools) by Tom Edwards (GPL-2.0+), redistributed here under GPL-3.0.

## License

`GPL-3.0`. Required by Blender's GPL inheritance and the bundled Blender Source Tools.
