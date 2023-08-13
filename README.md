# Composite-Video-to-RGB
A cheap DYI solution for demodulating an analog composite video signal back to RGB.

UPDATE 13/AUG/23 - taken a small break from this as i still can't get a decent picture and will need to review it further under a scope or redesign  - suspect i need redo the sync component.  I've also seen some cheap circuits (2x scaler) on ebay/Ali that seem to be able to take 240p composite video and svideosignal and convert to 240p  RGB HV (and also upscale x2) - that may be less hassle.
UPDATE 30/APR/23 - still working on this but no luck so far, with initial protoypes.

As a big fan of the cheap GBS 8200 video scaler (especially once modified with GBS Control), i was keen to find a method to input a color composite video signal.
While primarily for upscaling, this may be useful for adding a composite video signal into an rgb only monitor.

Note this schematic and associated PCB will not upscale an input signal.  It will just seperate the  sync, colour, luma information already in the signal.

Why composite video?
Composite video is a busy signal, often youll see a messy effect called 'dot crawl' which creates a wavey effect on straigh lines in most analog video. This effect can also make upscaled composite video look very average.  
It's one of the lowest quality signals youll get from a video device (much worse than svideo, component, scart rgb, or vga (rgb hv), or hdmi etc).
However it was widely used across many video gaming consoles, vhs, pvrs etc.

While some video devices can be modified to output a better quality rgb signal, many are not able to (or in some cases it is cost prohibitative to do so).

Why not just use those cheap composite to hdmi converters?
They do an ok job, but they often introduce a lot of delay in video processing. For most users this isnt noticable but when playing time sensitive video games- this can greatly impact the enjoyment/ experience of a game.


This circuit is therefore intended to 'convert' video very quickly into a format that can be quickly processed and upscaled using very low lag uoscalers.  It does not 'fix' any quality issues with a composite video source.




Parts
For this project, Ive used an old analog ic that can still be found cheaply and in plentiful supply on ebay/ali express.
After finding it, it appears to have been used heavily in portable handheld lcd tvs that had an av in socket as a block step before the video was converted/scaled by the lcd panel driver ic.

Ive used the application example in the found datasheet, with modification to make it work properly in this scenario.
.



This is currently a WIP. More info will appear once initial build and tests are completed.

Dek 26/1/2022
