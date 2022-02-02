# study-synth.pd

This is a subtractive synthesizer based on the ones used in my [master's thesis
research](https://traviswest.ca/making_mappings/). The architecture is slightly
different, but the overall character is similar.

There are two oscillators: a square wave and a saw wave. The saw is implemented
using feedback FM. The square is a logistic map coupled to a digital waveguide,
sort of like a simple physical model of a clarinet model. Both oscillators
share an energy parameter. From 0 to 0.5, the energy increases from silence
through a simple near-sinusoidal spectrum to a full bright square or saw. Above
0.5 the oscillators are driven into their unstable regimes, and grow
increasingly chaotic and noisy.  The oscillators are mixed by a cross fader,
and the mix goes through a resonant low pass filter and a reverb before heading
to the speakers.
