So I wanted to have a front visible set of status LEDs and a power button to safely shut down the RPi without having to open the UI.

https://forums.raspberrypi.com/viewtopic.php?t=343731

https://github.com/raspberrypi/linux/blob/996f28d6295ad091f7edb462b52a91c8112019d1/arch/arm/boot/dts/bcm2711-rpi-4-b.dts#L523

https://github.com/raspberrypi/linux/blob/996f28d6295ad091f7edb462b52a91c8112019d1/Documentation/devicetree/bindings/leds/common.yaml#L82

https://forums.raspberrypi.com/viewtopic.php?t=101598

https://kitronik.co.uk/blogs/resources/which-resistor-should-i-use-with-my-led

https://kitronik.co.uk/blogs/resources/led-resistor-value-calculator

https://www.richinfante.com/2021/08/11/raspberry-pi-gpio-status-lights

--

I designed up a front "hex" mounted thing to hold the LEDs and the button .. 

![image](assets/13251/987c4307-284d-4f36-bcc8-1d1c2b51dace)

I want to use 3 LEDs .. 

Green: System Status (so it should be "on" when the system is on)
Yellow: Disk Activity
Red: panic-indicator (fancy way to hopefully be able to see the RPi is crashed .. 

And I had a little button handy .. so it looks like this:
![WhatsApp Image 2023-12-21 at 21 53 44_223efa18](assets/13251/da4138f6-f2ed-4762-82e7-292ab4254d18)

Based on the docs available I should be able to just make that work with 3 dt-overlay lines .. 

```
dtoverlay=gpio-led,gpio=23,label=power,trigger=default-on,default-state=off
dtoverlay=gpio-led,gpio=25,label=panic,panic-indicator=true,default-state=off
dtoverlay=gpio-led,gpio=24,label=disk,trigger=disk-activity,default-state=off
```

---

Now I just have to get the wiring right .. 

- need to confirm that the status LEDs output 3.3v .. this is fairly sure thing .. 
- need to then figure out what resistor to use .. 
- based on the calculator .. 68 ohms should do it .. (Blue, Gray, Black)

Then something like this should work:

* note, I'm already using the first 6 pines in that row for controlling a PWM fan for the RPi itself, so this could clip in on the next 5 pins nicely

![image](assets/13251/8ce976f2-d76a-4be7-a46d-059b2c234495)

