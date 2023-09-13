# tronxy_x5sa_voron

This is a repo to track work I'm doing on converting a Tronxy x5sa to a Voron Chimera of some sort .. 

## The Plan

* Get the Tronxy kit
* Try to re-use as many parts as possible
* Try to make this into a gradual upgrade

BOM:
* Tronxy x5sa
* 350mm MGN9H x2 (for the Y)
* 450mm MGN12H (for the X)
* DIN Rail 484mm x2
* Power Recepticle
* Piles of ASA filament
* GT2 Open Belt LL-2GT-6 (6mm wide) - 6meters
* F695 Bearing x 20
* GT2 20T (6mm wide) Toothed Idler (5mm bore) x 2
* GT2 20T (6mm wide) Pulley (5mm bore) x 2

** I will need to get a cross-bar for the back of the AB mount .. its an annoying size, so this will have to be aded to the BOM
** I'm considering sourcing that from Ali .. it'll take a while .. but I could also grab all the extra extrusion bits for the full conversion .. 
*** I do have a bit of spare extrusion .. at 345mm .. 25mm short may be too much to hope for to be able to assemble the back beam .. so I may need that to be able to assemble the AB drive regardless .. 

* eventually, you'd need to add the AfterBurner / StealthBurner BOM as desired

## Phases

1. The first phase will be just assembling the frame and seeing what I need to make designs for
2. I will try for an "open" design where I mount the Trident AB drive unit to the TOP of the frame at first .. this is just so I can move on .. the open design is not going to get me far
3. I will need to re-design the Z system .. at first without cutting the rods .. I'll try to frankenstein something between the V1.8 Bed mount
4. I will definitely need to tweak some parts of the skirts .. it should be just adding some extensions .. so it shouldn't be too bad
5. I will definitely need to tweak some parts of the AB drive mount
6. The plan is to potentially transition between a V1.8 style Z, to a full 3 stepper Trident design gradually without wasting materials. Ideally I can get this thing serviceable and fully enclosed in V1.8 mode.
7. I do want to basically entirely use the Trident style skirt system, for the taller bottom electronics bay, with DIN rails and all that
8. As this thing nears working state, I'll initially probably install my old AfterBurner (because I literally have it sitting in a box) .. and eventually replace that with a SB

# Notes:

Notes of Skirt:

* Depth is 10mm less .. which means I may have to use the 300mm spec side skirts .. and find a way to patch the gap .. 
* Width is 20mm more .. which means I will have to use the 350mm spec front/back center pieces, but stretch them by 20mm

Notes for XY:

Cross-bar length:	420mm
Back Bar length	360mm

The depth of the cross bar seems to be ~105mm in the tident CAD
So I'd lose that from the max print size .. but I guess that's ok .. 

ah the AB mounts will have to be redesigned .. they need to make room for the 2040 extrusion

Trident Z Frame:
X Beam	490	
Y Bar	202	cut an extra 20mm since the tronxy frame uses 2040 along its depth
Trident Y Bar Length	232	
Tridemt Y Bar Space	238	

1.8 Z Frame:
this uses 2 X beams	490	(same size as trident, just 2x)
and 2 Y Bars		the CAD has this at 150mm .. at least for the 250mm model .. 
		this is based on the guide rail spacing too .. 
		generaly seems like a  more finicky setup
y-bar length	200

Z Rails:
Frame Z Inner Height	530			
Without the upper section (and its extrusion)	405	ok so I'd need 3x 400mm rails		-- at spool3d that's ~$122.09
