# ender3_skr
This is where I keep my configs for my ender 3 with an SKR mini e3 v2. 

Contains Klipper, for marlin 2.0 see my marlin fork.

# Pin outs for bltouch and lcd screen are (finally) found.

I have a genuine bltouch v3 with the sensor in the z-stop, please see the relevant section for the pin-outs.
In the klipper github there is a bare bone skr mini v2 config without bltouch nor lcd, finding the pins was a bit cumbersome, but I managed with an skr 1.2 config I found on reddit as a reference.   

For setting up the bltouch, please see the official docs and don't forget the config refernce:

https://github.com/KevinOConnor/klipper/blob/master/docs/Config_Reference.md



# esteps calibration is rotation_distance

https://github.com/KevinOConnor/klipper/blob/master/docs/Rotation_Distance.md

To calculate the rotation_distance from the marlin esteps you may already know:

```
rotation_distance = <full_steps_per_rotation> * <microsteps> / <steps_per_mm>
```

For the ender 3 with a creality 42-40 stepper motor this comes to:

```
rotation_distance = 200 * 16 / <steps_per_mm>
```


