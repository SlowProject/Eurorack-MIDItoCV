# Eurorack-MIDItoCV
A MIDI to CV eurorack module using Arduino nano

- Modified from https://github.com/elkayem/midi2cv for adapting it to Eurorack.
- Warning! Designed to fit in Eurorack cases similar to Cre8Audio Niftycase. Due to the length of the PCB board, it does not fit in Gie-Tec and similar rails!!
- I use TRS MIDI-IN instead of DIN5.  
- Code by Larry McGovern: https://github.com/elkayem/midi2cv/blob/master/midi2cv.ino  

![alt text](https://github.com/SlowProject/Eurorack-MIDItoCV/blob/main/pics/MIDItoCV-front.jpg)

OUTPUTS:  
- Note CV output (88 keys, 1V/octave) 
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
- Adjust the value of the NOTE_SF constant in the code for precise tunning if necessary  
