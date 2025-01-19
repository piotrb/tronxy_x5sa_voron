The main problem I encountered with the Z / bed assembly is that it was designed to stick out the sides of the frame. If we're convering this into a proper enclosed Voron, we need to tuck all that inside.

There was few problems:

1. The Z motors were center mounted on the extrusion (so ~10mm overhang on each side)
2. The bed assembly itself was wider than the frame.
3. The linear rod bearings have giant flanges, making it impossible to use those if the linear rods were to be mounted on the frame.
4. The Bed mounting itself is a bit unique .. there is 3 holes very close to the edges of the bed on the front and back .. this doesn't really align very well with the Voron bed designs.

## Bed Assembly

The bed assembly is for the most part stock, the main difference is that the square rods had to be trimmed to fit inside the frame.
I played with a few ides but the main one I'm going to try to implement is a very Voron 1.8 style system.

1. Trim the square rods by `32mm` one each side (this will algin the original Screw/Rod plate with the new Z motor position
2. Drill & M3 Tap those rods to allow to use a similar to original 2 screw attachment to allow the bed frame to stay stable and square.

## Bed

For the most part stock ...

I may very quickly want to get a Spring Steel surface though .. not sure how much pain the stock Glass bed will be.

Note:

Looking at how this is fitting into CAD, a bunch of Y space is being eaten up at the back, so it'd be good to be able to create some alternate mount which shifts the bed a bit forward .. I will start trying to make this a light weight thing that can be just attached to the existing aluminum frame that comes with the Tronxy .. I wouldn't want to try to replace the whole mount until I'm working on switching to a more solid Trident 3 stepper setup .. 

## Note about Z Height

Due to the addition of the 1.8/Trident style Gantry level extrusions, the length of the Rods and Screws must be shortened.

See: [XY Setup](XY-Setup.md)

## Z Motors

The Motors will move inside the frame Voron 1.8 style (identical mounting part). They should align perfectly with the trimmed bed mount, so the original screw attachment can be re-used.

The motors do use a bit of a weird way of attaching to the metal plates, half of the stepper screws are longer and they were pulled through the plate.

* Short screw length: ~33.5mm with head .. 
* Long screw: 41.8 with head
* So ~8.3mm have to be trimmed down from those long ones
* And then 4x M3x12 screws can attach it to the V1.8 Z motor mounts
* In the early phases, I'm just using 2x M3x12, probably want to upgrade to 4 screws in the final fit

The Screw will have to be shortened. The how and by how much is TBD.

I have some old screws from my Ender 3 conversion, I may use that to test the cut/finish.

## Linear Rods

The rods will have to be shortened. The how and by how much is TBD.

They will be mounted similar to the 1.8 style with those little accent mount pieces.

They will also align perfectly with the original holes at the bottom at least, so they can actually get a but of extra alignment help and support from the bottom there.
At the top they will just be held by the printed holder (this is good, since it will allow for easy final alignment.

The attachment to the bed frame will be interesting.

Ideally I'd like to re-use the original bearings, after all the goal of this project is to waste as little as possible :). In order to do that I'll have to remove the flanges from those bearings, and then press-fit them into redesigned part that's based on the 1.8 mount. Now I don't actually understand how the 1.8 part was normally fitted, or how tight it was, etc .. from some trial fits, it feels very snug when I try to insert the bearing into it .. but maybe that's good .. it'll hold in place well :) .. hope the ASA I printed the part from is strong enough to take a bit of stretch.

Worst case 4 `LM8LUU` bearings will need to be added to the BOM. I will try to cut the flanges off though first and see if I can salvage them, they appear to be heat fitted (but I don't want to heat it up with the bearing inside, since that feels like it'll melt/damage it), so I'll just have to try to cut it.

Update 1:

The rods will need to be shortened by ~123mm. I designed a cutting jig to make it easier to get the size right.
Still need to see how well my dremel rotary tool will handle cutting the rods.

Trying to figure out how long the screws should be .. this calculation is a bit tricky .. 

In the Voron 1.8 design .. the screws are well below the top of the linear rods .. 
But the trick seems to be to basically algin it so that the linear bearing assemblies touch the top printed stopper .. everything above that is extra rod .. 

I probably want to finish the CAD a bit more before I make that final determination .. since I have a bit of catching up to do in order to reflect the final state of the bed/Z in the current design .. then I can figure out how much the rods need to be cut .. not like that will be an issue until I'm ready to actyally put in the X axis anyways .. 

Ok on a quick look .. ~95mm may need to be chopped off .. I just need to figure out how to finish that cut ... its one of the few things that may need a half decent finish .. 

Also if the original screw is ~453mm .. chopping 95mm would put it at about 358mm total .. my old ender Z screws may actually work here .. they're just around this size .. so I'll have to play with it .. it  at least gives me a backup plan .. and a better sized "make do" option .. 

Yup my old screws are perfect length, so I didn't need to figure out how to cut them .. not using the voron spec stepper with embedded screw type things some Z height will be lost at the bottom .. 