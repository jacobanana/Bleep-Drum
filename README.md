# The Bleep Drum with MIDI v12

http://bleeplabs.com/store/bleep-drum-midi/

Now compatible with current versions of MIDI, bounce and pgmspace.
It is no longer necessary to edit MIDI.h

Dam Drum sounds.txt contains the samples used in the second and third Dam Drum. All that was differnt in the Dam vs Bleep drums was the sounds. http://www.stonesthrow.com/news/2013/01/dam-drum

Here's a guide for getting your own sounds into the Bleep Drum.
http://bleeplabs.com/2013/04/07/putting-your-own-samples-in-the-bleep-drum/

All work licensed under a [Creative Commons Attribution-ShareAlike 3.0](https://creativecommons.org/licenses/by-sa/3.0/)

---


This is an Arduino nano based version of the Bleep Drum.

# Build options
All samples are available by using different build flags. These are predefined as separate environments in platformio.ini

Use the following commands to program the different samples:

Bleep Drum : `pio run -e bleep -t upload`
Dam Drum : `pio run -e dam -t upload`
Dam Drum v2 : `pio run -e dam2 -t upload`
Dam Drum v3 : `pio run -e dam3 -t upload`

These commands must be run from the BLEEP_DRUM folder

# Significant changes

## Stereo DAC
This implements support for a stereo DAC (MCP48x2) instead of the mono DAC used on the original. This is just because I had it in stock at the time of the build. In order to use the single channel version, remove the build flag `STEREO` in platformio.ini.

## Output assignement
Hold TAP and any of the trigger switch at boot to assign those to the second DAC output.

## Sample rate adjustment
Hold SHIFT + TAP and turn the right pot to adjust sample rate. Set fully clockwise for original sample rate.
