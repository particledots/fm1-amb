# AMB-1 Sound (unofficial additions)

This is an **unofficial** fork of Charles Vestal's AMB-1 for the M-VAVE FM-1 (https://github.com/charlesvestal/fm1-amb,
MPL-2.0). It is not affiliated with or endorsed by Charles Vestal, M-VAVE or Hügelton Instruments. It adds three
controls on a new "Sound" page (SEQ pressed twice):

- **Palette**: the bells become struck objects with a drifting material, size and stiffness; one slow scene moves the
  bells, the pad and the bass together. 0 is AMB-1's own sound, byte for byte.
- **Pulse sound**: Drums (as AMB-1) or Melodic (each pulse hit plays a short plucked note of the sounding chord).
- **Chance**: leaves out a share of the Melodic hits.

The same engine additions run in the AMB-1 Audio Unit plugin (https://github.com/particledots/amb1-plugin). The
changes are in `app/dsp/amb.c` and `amb.h` (marked `AMB1-SOUND`), `app/ui.c` (the page), `app/project.c` (settings saved
by an earlier version are carried over), `app/app.h`, `app/host.c` and `tests/scenarios/`. In this firmware a partial of a
struck-object bell is skipped once it has died away (below about -86 dB), which keeps the load close to AMB-1's.
Files keep their MPL-2.0 licence and Charles Vestal's copyright line.
