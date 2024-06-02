# Configuration
## Enabling the functionality
In order for the included functionality to work in LoopToGo, the DAW Mode must be enabled. Executing `enter_daw_mode.ltgs` will do it, and `exit_daw_mode.ltgs` will turn it off.

## MIDI I/O
When plugged in, the device is recognized with two MIDI devices on both input and output: 
* MIDI IN: `LKMK3 MIDI` and `MIDIIN2 (LKMK3 MIDI)`  
* MIDI OUT: `LKMK3 MIDI` and `MIDIOUT2 (LKMK3 MIDI)`
Both devices are used in LoopToGo. Depending on the functionality used, one or the other will be used.

# Pad Modes
## Drum
`set_drum_pad_colors.ltgs` sets the colors of the pads according to preference. However, the pads need to be mapped to the proper kit pieces in the VSTs used.

# Loading scripts
Only load scripts from the `Entrypoints` directory. This directory contains all the "public" interfaces and loads dependencies used by all their underlying scripts, as needed. This was done like this to avoid duplicating the loading of some scripts before LTG supported the ability to load scripts only once. It also makes it easier to identify which scripts orchestrate the different flows.

# Flows
The following flows are implemented, based on different triggers:

## Drawing
The drawing flow is triggered when LoopToGo is started, thanks to the `autoStart` script in the root folder.
This flow continuously redraws the display and the pads on the LaunchKey device.

## Button Press
The functionality related to the pads and some buttons on the LaunchKey are triggered by button press events. All button press events start in the same script, which evaluates which button was pressed and dispatches the event accordingly.

## Markers
Some scripts are intended to be used by markers. These scripts are used to manipulate the configuration of the LaunchKey throughout a song, e.g. change the pads to drum mode before a specific section in a song, or to enable/disable the arpeggiator.

# User Guide
## Navigation buttons
* Play: play the loop, starting from the tick