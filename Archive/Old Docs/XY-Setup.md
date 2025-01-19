The XY will require a bunch of work .. 

First of all, there is a number of extrusions needed to be ordered .. 4 in total.

First there is the XY sub-level itself. This design is shared between the 1.8 and Trident.

On the Trident spec, this sub-level is ~105mm down from the top of the frame.

Item | Length | Qty | Instructions
--- | --- | --- | ---
Side Gantry Extrusions | 420mm | 2 | M5 Tap Both Ends
Back Motor Extrusion | 360mm | 1 | 

And then I also decided to use Trident's Back Support (and third Z rail) extrusion for extra support. This sets up the frame for being able to try to go Trident style 3 Z motors eventually.

Item | Length | Qty | Instructions
--- | --- | --- | ---
Back Support Extrusion | 405mm | 1 | M5 Tap One Side

## XY/AB assembly

Mechanically this should all work pretty similar to the 1.8/Trident setup .. but there is subtle differences between them and there will need to be more for this.

For one, the AB motor mounts will need to be altered to fit around a 2040 extrusion, this shouldn't be a big change in itself, so I'm not worried.

The placement of the limit switches will be a bit troublesome. I will probably need to custom design some variant of the X gantry attachment.

I'm going with the Trident style single linear rail design, but the Trident depends on mounting the X limit switch on the Frame end of the gantry (it uses a V2 style X/Y unified limit location). The 1.8 still has split limit switches .. anyways since I'm using the X mount from the Trident, I'll have to modify it to include the limit switch in the toolhead (so its back to 1.8/Switchwire style) .. probably anyways .. as I have the CAD closer to where it needs to be I'll see if there is any way I can re-use the v2/trident limit switch design .. but there may just not be room for it .. in those designs it depends on vertical linear rails, so it can put stuff below the rail Y extrusion .. in the linear rod design, those are in the way there .. so I'd have to find a way to literally flip that design and place all thar ABOVE the Y extrusion.

## Further Notes

The X extrusion will have to be cut down to ~450mm to make room for the Voron mounting on it.

The X linear rail I got will need to be cut to 400mm .. since there is more X distance being eaten up by the mount, I over-estimated what will be needed there.

I also played with the XY mounts .. and if I kind of rotate and swap them .. they end up seemingly aligning and fitting .. 

This also means that I would be able to use the fancy voron 2 style unified XY endstop board from the look of it

The chain path is a bit up in the air .. but it looks like it may work .. its a bit more .. specific now .. so I'm not sure that we can actually re-use the tronxy chains .. they are a bit clunky .. but the general idea seems to be that I'll be mounting the chains similar in principle as the standard 1.8 build does .. which is a chain fitting in the upper section above the Y axis .. the X chain should be no issue .. routing all the cables outside the chains may be a bit interesting too but I don't anticipate it being too much of a problem .. 

I ended up using Mirrors of ALL the XY drive mount pieces .. The X caps, the AB drives and the Y attachments .. this flips the belt path entirely, but it does so uniformly .. so we should be able to use the Trident style parts, but driven on TOP of the extrusion instead of below .. This all looks pretty good in CAD, waiting for my extrusions to arrive .. 

 
---

Belt lengths .. 

Without the "maximizing Y" mods .. the belts are ~190mm each .. 

with the maximizing mod .. we're adding .. just a bit under ~32mm length to the rail .. so 2x that of belt .. so ~64 .. so ~225 per side .. this is with a lot of padding .. 