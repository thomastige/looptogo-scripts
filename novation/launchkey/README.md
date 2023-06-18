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