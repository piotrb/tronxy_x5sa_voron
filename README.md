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

> [!NOTE]
> I will need to get a cross-bar for the back of the AB mount .. its an annoying size, so this will have to be aded to the BOM
>
> I'm considering sourcing that from Ali .. it'll take a while .. but I could also grab all the extra extrusion bits for the full conversion ..
> 
> I do have a bit of spare extrusion .. at 345mm .. 25mm short may be too much to hope for to be able to assemble the back beam .. so I may need that to be able to assemble the AB drive regardless ..

* I'm expecting to need random hardware .. but I do have a bunch of that on hand .. so I'll see what I actually need to get .. I'll try to keep track of what I'm adding to the core kit for BOM purposes :)

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

## Phase 1: Frame + Legs

Materials Used:
* M3x6 BHCS x12 (for attaching the accent to the legs)
* M5x16 BHCS x4 (for the actual rubber feet)
* M5 Nut x 4 (also for the rubber feet)
* The Tronxy rubber feet x4 (you can easily put a M5 screw through them)
* M5 T-Nut x4
* M3 T-Nut x4
* M5x10 BHCS x 4 (or a couple of washers and a M5x12 .. its for the legs .. probably doesn't need to be that perfect)
* M3x8 SHCS x 4

### New Z Frame

The Plan is to re-use the original Aluminum square 10mm rods .. but to chop 20mm from each end .. 
This will cut it just in the middle of the mounting screws, hopefully still giving a stable enough mount

Then the idea is to replacate some hybrid of the 1.8 bed mount .. 

One trick here is that the linear rods will have to be moved inward just a little bit (10mm) .. because the linear bearings that come with the TronXY have a wide base (30mm) .. so it has to partially move in

Ok so if I chop 32mm from each end of the front/back Bed frame bits .. 
And then drill/tap some new holes in there .. 
Then the original plate can be used .. this is good .. it'd allow that to be fairly sturdy

So now I just need to design the new linear rod mounts to work with this

# Notes:

## Notes of Skirt

* Depth is 10mm less .. which means I may have to use the 300mm spec side skirts .. and find a way to patch the gap .. 
* Width is 20mm more .. which means I will have to use the 350mm spec front/back center pieces, but stretch them by 20mm

## Notes for XY

I'm making up a few names .. I should look up what the voron folks call them in the CAD :)

> [!NOTE]
> `Cross-bar` - the horizontal beams along which the XY gantry moves (x2)<br/>
> `Back Bar` - the short piece of extrusion in the back where the AB motors are mounted

* Cross-bar length: 420mm
* Back Bar length: 360mm

The depth of the cross bar seems to be ~105mm in the tident CAD .. So I'd lose that from the max print size .. but I guess that's ok .. 

ah the AB mounts will have to be redesigned .. they need to make room for the 2040 extrusion

## Trident Z Frame

> [!NOTE]
> `X Beam` - the long extrusion along the front of the bed<br/>
> `Y Bar` - the short extrusion from the X Beam towards the back rail

* X Beam lengh: 490mm
* Y Bar: 202mm

## 1.8 Z Frame

* this uses 2 `X Beams`: 490mm (same size as trident, just 2x)
* and 2 `Y Bars`: the CAD has this at 150mm .. at least for the 250mm model .. 
* Y Bar length: 200mm

## Trident Z Rails

* Frame Z Inner Height: 530			
* Without the upper section (and its extrusion): 405 mm
* ok so I'd need 3x 400mm rails for the full Trident setup
  * at spool3d that's ~$122.09

## Taking apart the Tronxy BOM

First impressions:
Damn that's a substantially bigger print bed!

Frame:
* 2040 530mm x4
* 2020 530mm x4
* 2020 460mm x4

X Gantry:
* 2020 485mm x1

Z Motion:
Linear Rod - 8mm - 527m long - x4
Screw 8mm (M8?) - 450mm x 2

---

**Trident Frame Bom: (blind joints)**

Misumi HFSB5-2020-470-TPW	9 - top/bottom/X

Misumi HFSB5-2020-500-LCP-RCP-AV360	4 - verticals

Misumi HFSB5-2020-470-AH235-TPW	1
Misumi HFSB5-2020-470-AH235	1

Misumi HFSB5-2020-430	1
Misumi HFSB5-2020-340	1
Misumi HFSB5-2020-332-LTP	1
Misumi HFSB5-2020-330-LTP	1

**Corner Cubes Version:**

Misumi HFSB5-2020-470-TPW	9 - top/bottom/X?

Misumi HFSB5-2020-460-AV340-TPW	4 - verticals

Misumi HFSB5-2020-470-AH235-TPW	1
Misumi HFSB5-2020-470-AH235	1

Misumi HFSB5-2020-430	1
Misumi HFSB5-2020-340	1
Misumi HFSB5-2020-332-LTP	1
Misumi HFSB5-2020-330-LTP


# Credits & Achnowledgememnts

* [Sanity Agathion](https://forum.vorondesign.com/members/sanity-agathion.13/) on the VoronDesign Forum for encouraging me to go through with this build
* [@MatthewSitton](https://www.printables.com/@MatthewSitton_362947) on Printables for the amazong [TronXY X5SA CAD](https://www.printables.com/model/372048-tronxy-x5sa-full-cad-model) which made starting out on the Voron-izing work so much easier.
