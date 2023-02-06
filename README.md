# Guide how to get 500 nits of brightness on Gigabyte M28U in SDR

Hello fellow community,

Gigabyte M28U by default and specifications supports only around 300 nits of brightness in SDR. But in firmware v07 there was a bug allowing you to boost brightness up to **~500** nits by enabling Local Dimming feature. Unfortunately they have fixed it in new FW 08 and 10 making this monitor dim again.

Many people who already upgraded to newer firmware, or just bought a monitor recently (like i did) have around 300 nits max. According to multiple posts on reddit, it seems like people are struggling to enable 500 nits again.

After some time of tinkering, tries and fails I have found a working solution. So here is my guide

## My starting conditions:
1. New (mid 2022) dim M28U with FW10 and local dimming doing nothing to brightness
2. Installed official [drivers from Gigabyte](https://download.gigabyte.com/FileList/Driver/GIGABYTE_M28U_HDR_Drivers.zip)
3. Monitor connected to a laptop via USB-C with display port alt mode. So the USB-C cable also works as both video and data cable for controlling the monitor (in case it matters). But my assumption that other connection methods will work too.
4. Laptop PC with latest Windows 11

## GUIDE
1. If you use HDMI or DP connection also connect monitor to PC via USB cable
2. Download and install Gigabyte [OSD Sidekick](https://download.gigabyte.com/FileList/Utility/OSD_Sidekick2204181.zip)
3. Download and unzip somewhere 2(!) firmwares from Gigabyte website [FW03](https://download.gigabyte.com/FileList/Firmware/M28U_F03_20210322.zip) and [FW07](https://download.gigabyte.com/FileList/Firmware/M28U_F07_20210913.zip)
4. For clean start, reset all settings on monitor in Monitor OSD menu - "Reset All" and restart monitor completely (by pressing joystick button for a few seconds to turn off and then turn on)
5. Launch Sidekick, go to About section -> Monitor Firmware. Click Browse and select FW03 (!). Then click Update. Update process should start. It takes around 10 minutes (may be even longer). Progress bar could be incorrect, just have patience. On finish monitor will restart itself. You are on the oldest FW03.
6. **Now an important trick**: in Windows settings go to System -> Display and select HDR mode ON for this monitor.
7. Go to Monitor OSD menu settings -> Picture -> HDR -> **Local Dimming and turn it ON** (monitor should become significantly brighter). Keep it in that state (!)
I also strongly suggest using light windows themes and wallpaper (or whatever you have on screen) here, so local dimming in HDR will pull monitor brightness to the max.
8. Launch Sidekick again, and via About section select FW07 and click Update. Wait through the whole procedure again for like 10 minutes till the monitor finishes and restarts.
9. A good sign will be if the GIGABYTE logo on monitor booting will be brighter.
10. After monitor restart windows should revert back to SDR mode by itself (otherwise you can set HDR to off by yourself)
11. Go to the Monitor OSD menu, select any Picture profile (like Standard or so), and set Local Dimming to ON.
**Voila! It should be significantly brighter now! Here we go 500 nits**
Let me know if it works for you.

## Tip 1
The way Local dimming works on M28U is that it will dim brightness as soon as content on the screen is dark and after you switch back to bright scene colors for the first seconds look washed out until the monitor pulls brightness up again. I don't like the way it works. But there is a fix for that too!

Assuming you already have a bright Picture profile with local dimming on.
Open Sidekick an on Display Settings select Crosshair ON. It should draw an ugly green crosshair in the middle of the screen. It's supposed to be a gaming feature, but we will have another use for it.

Select [1] or any other number next to the crosshair icon, and then click Pencil icon. It should open a popup with a crosshair drawing tool and blank canvas.
Don't draw anything there and just click Save.

Voila! Now you have "invisible" crosshair on screen. Main trick here, that the monitor will stop dimming the screen on dark scenes and slowly dim it back with washed out colors :)

## Tip 2

It seems like a local dimming bug, allowing to keep SDR brightness on 500 nits is not only FW07 specific. If you really want - you can upgrade again to FW10 and keep 500 nits. But there is a trick again.

Before upgrading, go to Monitor OSD settings, select Save Settings -> Settings 1 (2 or 3) and Save them.

Now you can upgrade to FW10 using Sidekick. Then go to Save Settings -> Settings 1 -> Load. **Your 500 nits should be back!**

## Tip 3

When Local Dimming is on, brightness adjustments in the monitor won't work (as they are already on max). But what effectively replaces brightness in this case is the Contrast slider.

If you want to have a handy utility to control monitor brightness and contrast from your PC I can recommend https://github.com/xanderfrangos/twinkle-tray

*PS: Please keep in mind that even though this guide uses only official Gigabyte app and firmwares, you are still doing it at your own risk :)*

Thanks for reading and good luck!

