![IPSwitch](https://raw.githubusercontent.com/3096/ipswitch/master/icon.png)
## Pronounced as "I-P-S-witch".
Use text to generate `.ips` patches to use with Atmosphere.

### To use `.ips` patches make sure you have Atmosphere 44e2412a (July 30, 2018) or later loader build.

See example for details.

---
## About this fork
Upstream IPSwitch stopped building a while ago. libnx removed the old HID input API it depended on, and that same break is what makes the old build crash on recent firmware. This fork ports the input code to the current libnx `pad` API so it compiles again on an up to date devkitPro and targets recent firmware (21.x and later). Nothing else changed, the patching logic is untouched. Confirmed booting on hardware (firmware 22.5.0).

---
## Credit
- plutoo for making elf2nso, used in compressing patched elf to nso (ISC License)
- [Violet Inkling](https://www.deviantart.com/violetinkling) for the app icon art *(with permission)*
- OatmealDome for help in testings and feature suggestions
- All of my preview testers on SPH/SMH

---
## Build
You need a current devkitPro with:
- devkitA64
- libnx
- the lz4 portlib, installed with `dkp-pacman -S switch-lz4`

Build from a path with no spaces in it, since the devkitPro build system does not handle spaces in the project path. Then run `make`. The output is `ipswitch.nro`.

---
## How to use
See [example](example)

For further assistance, please join our [Discord server](https://discord.gg/BFEuuaBNR4)
