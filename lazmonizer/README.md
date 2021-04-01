# Lazmonizer

![Lazmonizer Screenshot](https://github.com/mlazarev/m4l/blob/main/lazmonizer/images/lazmonizer_main.jpg)

A multi-oscillator monophonic synthesizer based on a harmonic series of sine waves. 

## Concept

When enabled, the *lazmonizer* will trigger a metronome to generate a random number for each sine wave in the harmonic series, applied to its amplitude
and thus mutating the dynamics and timbre of the produced drone. The random number generator is based on a *drunk* function which limits the step range
of the next number - so it doesn't jump all over the place, but rather moves with a limit up or down, in a *drunken* walk.

## Controls
**Attack** + **Release** - A basic AR envelope applied to each MIDI note

**Laz** - Engage the internal metronome to generate the randomness

**Rate** - The rate of random number generation in milliseconds

**Depth** - The step size applied to random numbers - lower values will produce smaller fluctuations, while large values will incur big jumps

**Smooth** - Apply a slew between two generated random jumps in amplitude. When *depth* is very high, a higher *smooth* rate will reduce jagged jumps and smooth out the sound.


## Visual Source

![Lazmonizer Source](https://github.com/mlazarev/m4l/blob/main/lazmonizer/images/lazmonizer_src.0.2.jpg)

Top level view of the entire device. The oscillator bit is encapsulated to be reused by this and other devices. See below.

![Lazillator Source](https://github.com/mlazarev/m4l/blob/main/lazmonizer/images/lazillator_src.0.2.jpg)

The oscillator which is used N times in the main device. 


## Changelog
v1.0 - Initial release to [maxforlive.com](https://maxforlive.com/library/device/7152/lazmonizer) (April 1st, 2021)

v0.2 - Added **Depth** of the steps (essentially modulation) as well as **Smooth** function to control the rate of ramp up to the next value.

v0.1 - Initial commit with a new **Rate** control.
