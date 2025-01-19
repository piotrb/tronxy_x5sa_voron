# 1. Shopping

## 1. For the Frame

You will need to order a few extrusion pieces:
* 420mm (x2) with m5 tap on both ends
* 360mm (x1) no tap
* 405mm (x1) M5 tap on one side only (both sides is ok, but only need one)

I had good success with this store: https://www.aliexpress.com/store/911747370 they have preset sized extrusions, but they will cut/tap them on request. They did that quite quickly for me and the packaging was great too, good padding, so there little change of damage in transit.

While you're there also pick up:
* (at least 4pcs, they sold them in increments of 5) LM8LUU 8mm High quality Longer Linear Ball Bearing from them

The stock linear bearings can be damaged easily when trying to de-flange them .. so you may as well have spares, and they seemed smoother for me when I replaced them anyways.

# 2. Frame

Assemble the frame as per the Tronxy spec

Have a look over the blind joint information in the Trident Manual (Page 10)
https://github.com/VoronDesign/Voron-Trident/blob/main/Manual/Assembly_Manual_Trident.pdf

> [!IMPORTANT]
> Print out the drill guides for the blind joints as well as the spacing helpers. (you can print this in PLA if that makes it easier, these are disposable helpers)
> 
> You can find them in `STL/Frame` folder of the repo. These are specifically `105mm Y Alignment Spacer x2.stl`, `115mm Extrusion Drill Guide.stl` and `Back Center Drill Guide A.stl` (as well as the `Back Center Drill Guide B.stl` counterpart). You will need the last two in a second.

Drill out the ~4 mm access holes through the wide end of the 2040 extrusions as per the guide.

What this looks like:
![PHOTO-2023-12-11-10-32-34](assets/13251/9716e8e5-70cd-44ae-a9ce-28f93758f804)

> [!NOTE]
> TODO: add some photos/drawings on how to do this

Take off the top pieces of the frame, and slide in the pre-threaded cross-bars (420mm pieces) with M5x16 BHCS screws, and tighten them through the access holes. Use the spacing guides to help align the spacing to be as close a possible to even.

Between the Trident Assembly guide and the Trident Frame Upgrade guide you can find some tips visually on how this is supposed to come together. We're just using slightly different lengths of the drill guides.

https://github.com/VoronDesign/Voron-Trident/blob/main/Manual/Frame_Upgrade_Trident.pdf

> [!IMPORTANT]
> Also print out the bottom drill guides ..  (you can print this in PLA if that makes it easier, these are disposable helpers)

For the bottom access holes, I made a different kind of guide, made up of 2 parts, you slot it into the extrusion, and drill with a 3mm drill in the right spot which should be centered on the extrusion.

> [!NOTE]
> TODO: add some photos/drawings on how to do this

You will need to do a similar thing with the 405mm piece, just with a single screw, take apart as much of the frame as needed (probably just the two bottom screws holding the back bottom extrusion) and slide the vertical piece in. Tighten it using the access hole you made. This being exactly centered is not as big of a deal.

> [!IMPORTANT]
> Print out the back corner braces (ABS) (from the Trident STLs)
> 
> Located: https://github.com/VoronDesign/Voron-Trident/tree/main/STLs/Z_Assembly .. specifically `z_rear_extrusionbracket_left.stl` and `z_rear_extrusionbracket_right.stl`.

Secure them loosely to the frame (why not, take care of the loose piece of extrusion)

# 3. Skirts

Print a bunch of stuff (standard Voron settings)
1. Print the corner pieces as per Trident spec
2. Print the Fan holding assemblies as per Trident spec.
3. Print the 350mm spec Front left/right skirt pieces
4. Print the Rear Left/right pieces .. I did create a slight variant of the power inlet piece .. but it being a main "power" component (and generally cheap, I recommend you replace it with the Voron spec at least Adam tech version) .. but you can just use the stock one too .. up to you how you feel about the safety of the stock electrical components.
5. Print my customized extra large back center piece in 3 parts
6. Print my customized left/right skirt parts
7. Choice:
  a. Print the customized blank center piece
  b. Or print the stock Trident Mini12864 assembly
8. Choice:
  a. Print my customized stock foot adapters
  b. Or don't .. and purchase the stock larger round feet as per Trident spec, they're quite cheap and readily available on Amazon .. I liked this option more, it seems to allow the frame to feel more rigid on the feet.

Assemble all that basically according to the Trident spec, with the few customized pieces swapped in.'

You will likely need a bunch of fasteners here, a bunch of M3 SH screws, some M5 and a bunch of t-nuts, and I think an M5 Hex Nut for each foot.

# 4. Z Assembly

> [!IMPORTANT]
> Print out the Bed Mount trimming jig, and the Linear Rod trimming Jig.

1. Trim those parts as needed.
2. You will need to drill some M4 holes and Tap them (I think its ~3.5mm drill, but double check) .. the jig has the holes for where you need to drill.

> [!NOTE]
> TODO: add some photos/drawings on how to do this

Assemble the bed mount similar to how it would be for the Tronxy, but now using the trimmed mount positions.

1. Option:
  a. Try to de-flange the stock linear bearings -- you will likely need to cut the flange open on two ends and then try to pry it off. Be careful not to get filings into the inside of the bearings and not to lose balls from it due to the vibrations.
  b. Just buy some linear bearings (I suggested a store that also sells you the extra extrusion pieces) .. the bearings are quite cheap, so its a case of why not .. 
2. Print my custom linear bearing mounts
3. Print the Voron 1.8 Z motor mount plates and the linear rod fasteners
4. Choice:
  a. Try to trim the stock Z rods to the correct length ~350mm (I've not tried this)
  b. Or purchase some correctly sized rods (I had some leftovers from an Ender 3)
  c. Or purchase some motors with built in rods .. I've not done this .. I'm going to go with this option when I start converting towards a Trident design)
5. Assemble all of this together into a working Z mount (just the bed mount for now, don't attach the bed)

# 5. XY

1. You will need a bunch of components .. mostly pulleys, bearings, and fasteners.
2. You need to print my inverted versions of the XY system
3. I focused on making the "xy limit pod" system to work .. it possible to use the V1.8 style Y endstop located next to the motor .. and then we'd need a modified toolhead mount that allows for an endstop switch .. If there is enough interest I could try to design the right pieces to make that system work .. what I really gave up on trying to make work is the X chain setup .. the inverted components just don't fit a chain on the X properly .. so this setup expects to use an umbilical style setup, ideally with a CANBUS toolhead.
4. I bought some magnetic sensor pod board for the XY limit .. but you're free to use the standard microswitch version of it from the Voron Trident spec.
5. I have a fair bit of little modifications to attach the Y chain.

# 6. Bed

1. you will need the custom bits of mounting for the chain top and bottom .. 
2. and then you mount the bead .. with all its 6 leveling screws .. 
3. the chain attachment fits in-between the right back screws .. you want to fit that all before you mount the bed
4. I highly recommend getting the spring steel print surface for the Tronxy x5sa .. it seems overpriced .. but I think its worth it over the stock glass bed .. you can defainitly make do with the glass bed to start with

# 7. Toolhead

This setup can fit any regular Voron toolhead. Given we're not using any parts from the stock toolhead .. its your choice what setup you use here.

# 8. Electronics

1. Get a DIN rail .. ~1000mm will be just enough to cut the two pieces you need, with a tiny sliver leftover.
2. The stock PSU will work well enough with the Meanwell 350 mount pieces .. the only problem with it is that its a fair bit taller and basically there would be no air flow if you attach the bottom panel .. the stock PSU also does not turn off its FAN even when idle .. so its quite loud .. I'd recommend getting a genuine Meanwell 350 PSU, it's smaller and the fan turns off when not needed.
3. You will need a 4 driver controller board (so pretty much anything will do) .. 
4. A raspberry PI .. ideally a Pi4, a Pi3b will be ok if you don't run a camera

You will need to wire it all up in a way that makes sense :) 