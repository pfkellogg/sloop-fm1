# SLOOP + FM-1 Big Screen

[SLOOP](https://github.com/isod89/sloop-fm1) by isod89 (a live groovebox for the M-VAVE FM-1, based on Leo Kuroshita's
[Felucca](https://github.com/hugelton/Felucca)), with one addition: while an app asks for it, the FM-1 sends its screen,
the sound playing and the BPM over its USB cable, so [FM-1 Mirror](https://github.com/pfkellogg/fm1-mirror) shows it big, live.
For players who can't read the FM-1's 1.54-inch screen.

This is an **unofficial** build, not a SLOOP release, and isod89 has nothing to do with it. Everything else is
**SLOOP 2.8.4** (commit `91f3018`) as published, plus about 340 lines (`firmware/src/screen_mirror.c`,
`firmware/src/sloop_mirror.c` and small hooks in `lcd.c`, `main.c`, `usb.c` and the build). With nobody asking, it does nothing.
USB only: SLOOP has no Bluetooth MIDI.

Tested on a real FM-1 (2026-11-04) with FM-1 Mirror on a Mac. **Watch it:** [SLOOP on a Big Screen](https://youtu.be/Pd4Bm6JvtkU).

**Source only for now:** there's no ready-to-install firmware here yet. To build it, see [BUILDING.md](BUILDING.md).
Install at your own risk, and back up your sounds and projects first.

Questions: **pfkellogg@gmail.com**

GPL-3.0, like SLOOP: see [LICENSE](LICENSE).
