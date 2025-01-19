Alright .. so what do we do with the Electronics .. 

I had an Octopus Pro 1.0 kicking around so I plan to use that .. 
It also has CANBUS built in which is nice .. 

Its up to the reader to decide how you're going to wire this up .. 

Some basic info .. 

There is 4 core Drive Steppers:

Z1, Z2, X, Y

There is also the Extruder stepper if you're not using CANBUS .. if you are using CANBUS .. you can really even get away with using any basic controller board, and just wire up the Extruder stepper as Z2 .. 

---

Other bits .. 

The V1.8 design puts the steppers touching the left/right edges of the enclosure .. This blocks using oversized 60mm fans in the skirt area .. or at least for half of it .. 

I do kind of still want to try to use Noctua fans .. but their 60mm ones are 25mm thick .. 

I may see about instead of mounting them on one side and having them "blow through" .. I can set one up on the left, and one on the right .. and they can help eachother move air .. 

---

RPI setup .. 

I really wanted to improve on my old setup from when I did my Ender 3 conversion .. that had so little room underneath I opted to mount the RPI outside .. but here .. I can do it all inside .. 

The power hookup is a bit annoying with the main power switch on the intake .. I wanted some way to individually power cycle the MCU and the RPI .. 

For that you need the correctly power rated switches .. ideally small enough to be able to be mounted in the Hex holes in the skirts .. 

I found this model: https://www.printables.com/model/147203-voron-24-skirt-rocker-switch-skirt-fitting which gives a nice way to mount round switches in the Voron Skirt holes.

So here is the breakdown .. 

The 5V side is no real issue .. its so little power .. 

I had a RS25 PSU from the VORON BOM, so I used that .. 

Output: 5V 5A
Input: 0.7A/115VAC

This is a passively cooled PSU so I figured I can just put a switch on the DC line.

I found these guys on Amazon: https://www.amazon.ca/dp/B07W4HGMZS They seem to do the job well enough, and even though they say they're for 12V, the little status LED works just fine.

Now for the main board .. 

The stock PSU .. (I'll eventually want to replace it with a genuine meanwell .. but hey this project is about minimizing waste .. for now at least .. )
The stock PSU is a bit loud .. ther's writing on it implying that there is a thermal sensor toggling the FAN .. it feels like a lie .. with no load .. on a cold start .. it seems to still run the fan .. 

Ideally I'd love to be able to turn off that PSU entirely .. 

Now I could set the board to be able run its electronics off the USB power .. but that's not that useful .. since a CANBUS toolhead needs a 24V line to stay connected .. and Klipper will lose connection to the board if that disconnects .. 

So if that's the case the whole MCU may as well go offline .. 

anyways .. 

The one that came in my kit was:
Cheng Liang
Model: P360W24V

Input: 115/230VAC
Output: 24V 15A

Based on some random comment on an amazon review .. 

> Used 176 watts input for 144 watts output, about 81% efficiency.
> Uses 6.5 watts with no load.
> Power factor was 0.6, so doesn't seem there's power factor correction.
> The fan is decently loud. It's tied directly to the 24v output; it does not change speed based on load or heat as the description or case describes. With ambient noise measuring at 35db, meter shows 48db with fan on. -1 star for non-temperature controlled fan with higher noise than described.

If I understand this correctly .. 

81% efficiency means .. 
At max load of 360W .. it'd consume ~450W .. 
450W for 120VAC .. is about 4A

So I need a switch that's rated for at least 4A (double for safety .. so 8A)

I found this:

https://www.amazon.ca/gp/product/B09TXLNQVZ

Which claims its a 10A, with light .. I'm going to give this a try .. and it seems to be in the same form factor, which is great!

So long story short .. I'm going to have a way to toggle the actual AC power to the PSU

Now basically all switches I see on Amazon in this format seem to cap out at 24V 10A which is not enough for switching the whole output .. 
But maybe .. If I switch each component separately .. 

The Toolhead MCU won't need THAT much amps .. 
And the Octopus takes multiple power inputs .. separtaly for Motors, Bed, Logic/Fans .. this is great .. since that's pretty major power draw breakdowns .. 

Really hard to tell what the actual specs of the bed are in terms of power draw .. its all covered up with insulation and I don't want to rip it off .. and even that may not say anything .. 

My hotend probably uses something like a 50W cartridge .. plus a bit for the electronics/extruder .. so 2A .. Voron spec has the stepper running at 0.5A plus electronics .. so let's say 3A .. its nicely covered by the 10A rated switches .. 

Steppers .. 
Looks like Voron examples run then between 0.6A to 0.8A .. so even if we round that up to 1A .. that's 4A on the Motors line .. again totally fine .. 

Electronics .. Fans .. can't really be consuming that much power .. let's say that's 1A max .. 

so let's work this in reverse .. 

360W @ 24V = 15A
15 - ~3 (Toolhead) - ~4 (Motors) - ~1 (Electronics/Fans) = ~7A .. 

That would make the bed max ~165W .. or would it .. 

Looking around Aliexpress .. CR10 heated beds which are 310mm in size actually draw a LOT more power .. ~220W .. making them almost 10A .. 

SO even that should be ok .. except that the power supply wouldn't even have the juice for it ;)

...

Alright .. so if I do this .. 

BOM:

* 1x (or 2x if I decide to just match it up and add a switch for the 5V for parity) .. of those AC switches
* 1x of the lower rated 12V (5V works) switches for RPI power
* 3x of the higher rates 24V 10A switches for the various parts of the power system .. 

I don't know how this will work for routing all those wires around .. oh well .. worth a shot .. 

