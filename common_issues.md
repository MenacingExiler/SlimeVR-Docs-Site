---
layout: page
nav_order: 6
---

# Common issues
{:.no_toc}

So something isn't working and you find yourself stuck, this page is here to give answers to common issues. If nothing here answers your question, please feel free to ask in the #technical-support channel on the discord.

* TOC
{:toc}

## Please specify upload_port while updating firmware

Something is messing with your physical connection to the tracker. Make sure that your trackers are plugged in via USB, the USB cable is a data and charging cable and that your drivers are up to date. Additionally, this can be caused by software hogging COM ports (VSCode and Cura can be the cause of this).

## The SlimeVR Server won't start

A lot of the time this issue is due to Java not being installed / issues with your installation of Java. Check [the setup page for more info](slimevr-setup.md#install-java).

## The WiFi Settings window outputs ERROR 

Try reseting your tracker, this may fix the issues immediately. If this doesn't work, your COM port may be being hogged, which can be tested by going through the firmware update process in VSCode (as it has more verbose error messages). If this is the case, close any application that might be hogging the ports (VSCode and Cura are often the cause). If the issue persists, try connecting the tracker to a different USB port.

## The WiFi Settings window outputs symbols and nothing else

There are two common causes that you should check:
- Make sure that you have the right driver installed.
- Check that your PIO firmware upload worked. If you have multiple firmware versions open in VSCode you will have to set the correct one to default to upload.

## My tracker keeps flashing

This is intended behaviour, the number of flashes lets you know the current status of your tracker. Check the top of the [the setup page for more info](slimevr-setup.md#readiness-checklist).

## My aux tracker isn't working

In order to make sure your aux tracker is set up you need to specify it in your defines.h uploaded to the primary tracker's firmware. Check the [bottom of the section mentioning defining the pins on the configuring the SlimeVR firmware page](configuring_project.md#define-pins-of-the-selected-board).

## Sensor was reset error

Check your INT wire, there is either a bad connection or you have it connected to the flash pin.

## The trackers are connected to my wifi but don't turn up on SlimeVR

Check that you do not have two copies of the SlimeVR server running, as only one of them will show trackers connected.

If only one server is running, this is most likely a firewall issue, go to SlimeVR Server folder and run `firewall.bat` as administrator.

If you are still having trouble, try manually adding the SlimeVR Server to your firewall. 

1. Go to **Settings** > **Network & Internet** then click on the text link **Window Firewall** (you may have to scroll down). 
1. In the firewall window, click the link **Allow an app through firewall**.
1. Click the **Allow another app...** button, and then **Browse...** in the opened **Add an app** window. If your options are greyed out in the **Allowed apps** window, click the **Change Settings** button to allow changes.
1. In the **File name** text box, type `*.*` and press enter before navigating to `slimevr.jar` in your SlimeVR server folder and select it (if you cannot see files in this folder, try typing `*.*` and pressing enter again to show all files).
1. Click the **Add** button to add the file to your firewall settings.
1. Finally, make sure both public and private check boxes are selected in the **Allowed apps** window before clicking **OK** to save the changes.

## The trackers are connected to the SlimeVR server but aren't turning up on Steam

There are two common causes that you should check:
- Make sure that you have the right driver installed.
- SlimeVR should always be launched before SteamVR. Close both and then launch SlimeVR Server before launching SteamVR. 

## My trackers are bound to the wrong controllers in SteamVR

You have to set them to the right location within Steam, check [the setup page for more info](slimevr-setup.md#configure-proportions-and-trackers).

## Getting extreme drift

Make sure that when you turn on your tracker it's sitting flat on the table, the sensors need to calibrate for 10-20 seconds in a stable environment.

## Trackers are moving in the wrong direction when I move

When you set up your defines file you may have put in the wrong rotation. Take note of which trackers are the issue and refer to the [configuring the SlimeVR firmware page](configuring_project.md#adjust-board-rotation) to get the board's rotation right.

*Created and updated by CalliePepper#0666, edited by Emojikage#3095*