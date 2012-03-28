# Synth Patches for AMS, PHASEX, and WhySynth

These are synth patches I either created or modified throughout the years as a working Linux-based electronic musician. I used them live and in studio projects for years.

The patches are for Linux softsynths [AMS](http://alsamodular.sourceforge.net/),  [PHASEX](http://disabled.github.com/phasex-dev/), and [WhySynth](http://smbolton.com/whysynth.html)

## Usage
* It's been a while, but IIRC there is a command in the PHASEX GUI to load patches.

* Loading patches in AMS can be done on the command line via a switch, or from the GUI in the File menu.

* WhySynth required all the patches as a single file, which I'd do by concatenating them. To load them, WhySynth required they be sent via OSC, which I used to do as follows:

```python
m=osc.Message('/dssi/whysynth/WhySynth/chan00/configure', ('load', "/path/to/patchfile"))
s.sendto(m.get_packet(), ('localhost', int(port)))
```

It's been years since I used these synths so my apologies for the thin instructions. I wanted to put these out there for others to use in case they wanted to.

## License

Copyright (C) 2006-2010 ken restivo

Distributed under the GPL, same license as the synths above.
