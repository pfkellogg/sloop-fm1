# SLOOP + FM-1 Big Screen

[SLOOP](https://github.com/isod89/sloop-fm1) by isod89 (a live groovebox for the M-VAVE FM-1, based on Leo Kuroshita's
[Felucca](https://github.com/hugelton/Felucca)), with one addition: while an app asks for it, the FM-1 sends its screen,
the sound playing and the BPM over its USB cable, so [FM-1 Mirror](https://github.com/pfkellogg/fm1-mirror) shows it big, live.
For players who can't read the FM-1's 1.54-inch screen.

This is an **unofficial** build, not a SLOOP release, and isod89 has nothing to do with it. Everything else is
**SLOOP 2.8.5** (commit `bac9c05`) as published, plus about 340 lines (`firmware/src/screen_mirror.c`,
`firmware/src/sloop_mirror.c` and small hooks in `lcd.c`, `main.c`, `usb.c` and the build). With nobody asking, it does nothing.
USB only: SLOOP has no Bluetooth MIDI.

Tested on a real FM-1 (2026-11-07): installed over the 2.8.4 build with SLOOP's installer, then the screen and the sound's name came through over USB on a Mac. **Watch it:** [SLOOP on a Big Screen](https://youtu.be/Pd4Bm6JvtkU).

## Installing it

Install at your own risk, and back up your sounds and projects first.

1. Charge the FM-1, plug it straight into the computer (no hub), and close every app that uses it.
2. Download **SLOOP-2.8.5-BigScreen.fwsc** from this fork's [Releases](https://github.com/pfkellogg/sloop-fm1/releases).
3. With this repository and Python 3 (`pip3 install mido python-rtmidi`), from its folder:

   ```
   python3 tools/fm1_install.py SLOOP-2.8.5-BigScreen.fwsc --yes
   ```

4. If the computer doesn't see the FM-1 after it restarts, unplug the USB cable and plug it back in.

We installed it over the SLOOP 2.8.4 build, which went on over M-VAVE's V15. Over M-VAVE's Open firmware or the FM-1 Big Screen
firmware, put the official V15 back first (M-VAVE's [FM1 Workbench](https://open.m-vave.com/fm1-workbench): Connect device, then
Device update › Restore original V15).

**Back:** SLOOP's own installer puts the plain SLOOP back, without the big screen.

To build it yourself, see [BUILDING.md](BUILDING.md).

Questions: **pfkellogg@gmail.com**

GPL-3.0, like SLOOP: see [LICENSE](LICENSE).
