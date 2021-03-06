Dexed - FM Plugin Synth
=======================

Dexed is a multi platform, multi format plugin synth that is closely modeled on the Yamaha DX7. 
Under the hood it uses [music-synthesizer-for-android](https://github.com/google/music-synthesizer-for-android) 
for the synth engine and [JUCE](http://wwww.juce.com) as a plugin wrapper.

The goal of this project is to be a tool/companion for the original DX7. Sound engine 
with 'float' value parameters, different waveform à la TX81z would be great but anything that 
goes beyond the DX7 should and will be a fork of this project. This is to keep the compatibility with
the original machine.

Dexed is licensed on the GPL v3. The msfa component (acronym for music synthesizer for android, see msfa 
in the source folder) stays on the Apache 2.0 license to able to collaborate between projects.

[Dexed User Website](http://asb2m10.github.io/dexed)

Changelog
---------
#### Version 0.9.1
* Mark I engine now uses 10-bit sine/exp tables. Still a work in progress but we are getting there
* More accurate FM feedback on the Mark I and OPL Series engine
* Wheel, Foot, Breath, Aftertouch modulation support
* Fixed the display of some more 'complex' algorithms
* Drop of .syx files in the cartridge manager
* Dexed data directory can now optionally reside in the same location where the binary is installed
* 'Send current program to DX7' in Cartridge Manager works as designed
* Support for sysex streams (multiple sysex messages in one .syx file)
* falkTX upstream fixes for Linux

#### Version 0.9.0
* Apple AU support
* Cartridge Manager
* Store action also can update the currently loaded cartridge
* Basic theming
* Fixed the UI corruption when more than one Dexed instance was loaded
* Fixed wrong display value issues (coarse and fine)

#### Version 0.8.0
* New UI by [AZur Studio](http://bji.yukihotaru.com/)
* You can now copy/paste the operator/envelopes values by using the right-click mouse button on the operator
* Fixed some of mono mode ticks on lower frequencies
* SynprezFM preset are now in a submenu

#### Version 0.7.0
* Preliminary Algo 4 & 6 feedback support
* DX Engine 'Dirty DX' emulation, including one based on OPL chips
* DX Engine LFO amplitude. This still needs tuning.
* Monophonic mode
* Added the 'INIT' button to re-initialize a program
* Fixed stucked notes when programs where changed
* Fixed engine envelopes wrong timing if it was not 44100Khz
* Fixed only .syx are shown when we are using the Dexed_cart.zip cartridges collection
* The DX7 Sysex port are now only used for sysex messages. This is used to avoid any midi note feedback.

#### Version 0.6.1
* Mouse over + LFO type fix + pitch eg values

#### Version 0.6.0
* Added external midi interface to send / receive sysex messages
* Fix Tracktion crash upon startup 
* Middle C (transpose) now works
* Identify the parameter knob/switch by simply moving the mouse over it
* Knobs now works with vertical mouse drags
* User DX7 zip cartridges

Credits & thanks
----------------
* DX Synth engine : Raph Levien and the [msfa](https://code.google.com/p/music-synthesizer-for-android) team 
* Graphical design : [AZur Studio](http://bji.yukihotaru.com/)
* LP Filter : Filatov Vadim (2DaT); taken from the excellent [Obxd](https://obxd.wordpress.com) project
* PPPlay : Great [OPL3](https://github.com/stohrendorf/ppplay) implementation, with documented code :D
* DX7 program compilation : Jean-Marc Desprez (author of [SynprezFM](http://www.synprez.com/SynprezFM)) 
* DX7 programs : Dave Benson, Frank Carvalho, Tim Conrardy, Jack Deckard, Chris Dodunski, Tim Garrett, Hitaye, Stephan Ibsen, Christian Jezreel, Narfman, Godric Wilkie
* falkTX [distrho](http://distrho.sourceforge.net/)

TODO - Dexed 
------------
* Yamaha 4 operators (DX21/DX27/DX100) sysex import
* UI threaded messaging to avoid DAW automation 'clicks' 
* Zomby UI changes: this occurs in Live
* Various code cleanup
* More smoothness in mono mode

TODO - msfa
-----------
* Portamento implementation
* Better Amplitude Modulation
* Test maximum delay lfo values that seems to be reset