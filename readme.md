# QuNeo MIDI feedback in VDMX 

A 'repost' of a practical example for the VidVox VDMX forums.

Check out the preset/project. It has a custom QuNeo preset and a VMDX control surface that mirrors the preset. Inputs are mapped, and although not all outputs are mapped right there's enough going to for a fun light show when you launch it. I also included the control surface JSON export, because I freaking love this new feature and have been using it plus the TouchOSC import feature non-stop. YMMV, I have a better time of mapping controllers by creating a control surface that mirrors the hardware and mapping VDMX internally from there. Great for when the hardware isn't hooked up too.

The QuNeo -- while flexible -- can be a pain to map for feedback for several reasons: 
* The MIDI feedback assignments are global, not per-preset (usually; unless you specifically change it for each bank in the current preset under the 'LEDs' tab). 
* The MIDI notes and channels don't always match up with what the software uses for its base references The confusing channel 0 vs channel 1 issue is a good example (VDMX uses the computer convention of starting counting at zero). VDMX channel 0 == QuNeo channel 1. I guess you'd run into that in many other situations too!
* Another example would be Traktor and note numbers, which use different values for "C3". Any time you use "Note C3" on one side and "Note 60" on the other is just asking for a headache. 
* In some cases (such as setting up a clock output) there's no choice but to use the Sending tab in the UI inspector, where you don't have the benefits of MIDI Learn. Every time I set up the media bins with the pad corner LED feedback I pray a little.

QuNeo manual pages 38 and 39 are worth just printing out because you end up referencing them all the bloody time. Only the sliders and rotaries use CC for feedback, the rest are Notes, as seen in another forum example. Also, having QuNeo local LED control on or off makes a difference whether a pad will show feedback or not later on, ack. I ended up creating 2 dedicated presets for mapping outputs. For all the caveats above, I've gotten good use out of the QuNeo. You _do_ pay in time spent for its flexibility, but hey -- you can put VU meters and das blinkenlights just about anywhere.

One more opinion: Don't bother using the rotary pads as encoders unless you hate yourself. They have a nonstandard output which VDMX doesn't read well (confirmed with dlublin of VidVox a while ago, we were both scratching our heads).

![](VDMX-QuNeo_Feedback.png)