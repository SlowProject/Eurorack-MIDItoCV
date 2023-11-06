# Eurorack-MIDItoCV
A MIDI to CV eurorack module using Arduino nano

- Modified from https://github.com/elkayem/midi2cv for adapting it to Eurorack.
- Warning! Designed to fit in Eurorack cases similar to Cre8Audio Niftycase. Due to the length of the PCB board (118 mm), it does not fit in Gie-Tec and similar rails!!
- I use TRS MIDI-IN instead of DIN5. The TRS jack (stereo 3.5 mm jack, PJ-301CM type) is cyanoacrylate-glued on the panel, and wired to the MIDI pads in the PCB.  
- The pairs of output jacks NOTE-CLOCK_OUT, CONTROL-GATE_OUT and VELOCITY-TRIGGER_OUT share GND pad in the PCB in order to save space.  
- Code by Larry McGovern: https://github.com/elkayem/midi2cv/blob/master/midi2cv.ino  

![alt text](https://github.com/SlowProject/Eurorack-MIDItoCV/blob/main/pics/MIDItoCV-front.jpg)

OUTPUTS:  
- Note CV output (88 keys, 1V/octave). Adjust the value of the NOTE_SF constant in the code for precise tunning if necessary  
- Note priority selectable with jumper:    
-- Highest Note: No jumper.  
-- Lowest Note: Jumper connected to A0-GND.  
-- Last Note: Jumper connected to A2-GND.  
- Pitch bend CV output (0.5 +/-0.5V)  
- Velocity CV output (0 to 4V)  
- Control Change CV outout (0 to 4V)  
- Trigger output (5V, 20 msec pulse for each new key played)  
- Gate output (5V when any key depressed)  
- Clock output (1 clock per quarter note, 20 msec 5V pulses)  
