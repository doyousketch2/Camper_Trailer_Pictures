# Camper_Trailer_Pictures
Twitter sucks, so I'm posting Trailer build PNG's here.  

This "sin() cos()" app is something I wrote to pose people in, for drawing.  
Wasn't originally intended to be a CAD program,  
but parts of it are truly leaning toward that.  

Wrote a tapered-draw routine, for fleshy bits, a few times;  completely wrecks my brain.  
Succeeded at it in PovRay, but then that computer died on me, so having to write it again.  

PovRay's great, but render times take a while, so progress is slow there.  
Tweak something, wait an hour for your image to draw.  
Tweak something else, wait another hour...  

Decided to look into a simple draw library that'll run on just about anything.  
Love2D kinda will.  PyGame as well.  Later versions require OpenGL -  
which, while that's handy, you'd have to have new hardware to do it.  

It's fine if that's available, but the thought is:  
to run on something like a RPi, where memory and all that, is constrained.  

**SDL2** looked like a good cantidate.  Both Love2D and PyGame use it, as do others,  
so I was already somewhat familar with it.  

Attempted to write this in Lua, but it was missing a couple draw routines;  
specifically,  sdlgfx.thickLineRGBA  &  sdlgfx.filledCircleRGBA  
which are pretty much all that's being used here.  

So I turned to Python3.  I'm not a fan of Python.  
It's OK, but it's really just BASIC with 4 f'kin types of lists,  
and layers upon layers of *required* tabs.

Prefer Lua, with *one list type*, "table" as they call it;  
even tho counting begins from 1, instead of zero-based,  
like any reasonable computer programmer would expect.  

But yea, menu on the side for posing people, then you can draw what'cha see.  
I'll get back to that, eventually.  I know how to do it, it's just frustrating.  
Math is hard.  Portions aren't hard, but it gets complicated, quick.  

Figured I'd write in object modelling routines, the thought being:  
that you can then pose people in buildings and whatnot,  
give them surroundings, and objects to interact with.  

While that's tricky, everyday objects are way easier to do than people.  
Mostly trig & perspective.  Easier to imagine, than to write.  
Even if the math doesn't stump ya, you sometimes run into programming gotcha's,  
like needing to deepcopy contents of a list, in order to mirror across an axis.  
You wouldn't expect that initially, but hindsight.  
