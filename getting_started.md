## Thanks

Thanks a lot to the following people

- jpjb (http://www.jpjb.eu) Testing and Bug-Tracking
- em81 (http://www.ewus.de) Encouragement to make this public
- Jean-Baptiste PERIN for his original midi drum-part ipo script

### System requirements

1. you must be running blender 3D 2.59 or later
2. you must have a version of python installed and set up for blender
Getting started with midi to ipo
1. Download and install the add-on. For instructions on how to do that please refer to your favourite search engine.
2. Open up blender and activate the add-on. Check the command-line output for any errors. 
3. Create an Object in blender 3D
4. In the Object panel find the "Midi_Driver" section
5. Choose a midi file
6. Refer to Options page for further instructions

### Options

**Track number** Stepper (1-max)

If your midi file contains more than one track, you can choose the track number to use for this object.

**Handle as Drum** Checkbox (true,false)

If you select this option the given track will be handled as a drum track. This means that the midi_driver will only listen to one note in the track.

**Drum Note** String Input (C1-max)
This option is only available if Handle as Drum is set true. This is the note the Midi_Driver will listen to. Valid values are C1,C#1, B#2 and so on

**Interpolation** SelectBox (Rectangle,Linear,Smooth)

Sets the interpolation the generated ipo-curve will use.

**Clear** Checkbox (true,false)

Check this box to clear out all IPO-Data on the object before generating.

**Reset on Note Off** Checkbox (true,false)

Checking this box will result in "zero" position key-frames being added each time a note off is found in the midi-data. Unchecking this option will generate a continuous movement to the target position generated out of the data, while checking will generate a "up-and-down" behavior.

**Multiplier** FloatVector(x,y,z)

- x the value multiplied with velocity value
- y the value multiplied with key value

**Value to animate** SelectBox (Both, Key, Velocity)

- Velocity will be animated on the x-axis. The Object will move on that axis each time the velocity of the played note is changed.
- Key will be animated on the y-axis. The object will move on that axis each time the key of the played note is changed.

**Keyframe** SelectBox (Set,Additive)

- Set will set the position on all animated axes to the calculated value
- Additive will add the calculated value to the current position of the object
