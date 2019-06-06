# Using IFTTT to Add Presence Detection Hardware to Meeting Room Displays

### Force check-ins without the hassle.


We've added an IFTTT integration, which allows you to connect hundreds of hardware devices to Meeting Room 365, including Blink and Wyze cameras, and various IR presence detection sensors, to enable room booking, automatic reservations, end early, forced check-ins, and calendar sync, based on the physical presence of employees in a particular meeting room.

[![](https://downloads.intercomcdn.com/i/o/120720062/1a4e731e789a44be1ef050ba/0%2A_yUSXPSvHC7OZd_Q.jpg)](https://downloads.intercomcdn.com/i/o/120720062/1a4e731e789a44be1ef050ba/0%2A_yUSXPSvHC7OZd_Q.jpg)

This makes it much easier to enable the "force-check-in" option, and "end-early" features, since they happen automatically, regardless of whether your team knows how to use them (or remembers).

[![](https://downloads.intercomcdn.com/i/o/120720063/722fb3dd9f0223fb327ae632/1%2ADiieKR-42m5QyJnNCH7kzg.png)](https://downloads.intercomcdn.com/i/o/120720063/722fb3dd9f0223fb327ae632/1%2ADiieKR-42m5QyJnNCH7kzg.png)

# Choosing Hardware

We've tested presence detection ourselves extensively with the inexpensive  [Wyze camera](https://www.wyze.com/wyze-cam/)  ($26 shipped), and the  [Blink](https://www.amazon.com/Blink-Home-Security-Detection-Included/dp/B019S3ULQM/)  cameras (from $64). Additionally, there are hundreds of supported devices in the IFTTT ecosystem, which can be used for presence detection.

While every situation is different, there seems to be many paths to reliably implementing this and many factors to consider. Purchasing a single test device for a pilot is almost always a safe bet.  

# Setting up your Camera in Meeting Room 365

Your first step will be to set up your camera hardware in Meeting Room 365. To do this, just open your display, head to the Hardware tab, and check  `Receive Motion events from IFTTT`.

[![](https://downloads.intercomcdn.com/i/o/120723074/1775f61c73e1e7022bd2954c/Screen+Shot+2019-05-12+at+3.17.54+PM.png)](https://downloads.intercomcdn.com/i/o/120723074/1775f61c73e1e7022bd2954c/Screen+Shot+2019-05-12+at+3.17.54+PM.png)

This will give you a unique URL which you can later use in IFTTT to configure a webhook trigger.

Optionally, you can disable automated check-ins from the Meeting Room 365 admin portal, by later checking the box  **"Disable automated check-ins"**. This lets you keep IFTTT configured if you need to modify or disable this feature in the future.

# Configure a trigger in IFTTT

Next, you'll want to configure a trigger in IFTTT. We'll be setting up the Wyze camera in our example, but you should be able to do this with a variety of hardware products, including motion sensors, and cameras with presence detection.

## Create a New Applet

[![](https://downloads.intercomcdn.com/i/o/120723411/f3656b6704aa0e79620f4ad2/Screen+Shot+2019-05-12+at+3.20.41+PM.png)](https://downloads.intercomcdn.com/i/o/120723411/f3656b6704aa0e79620f4ad2/Screen+Shot+2019-05-12+at+3.20.41+PM.png)

  
**Choose your service**

[![](https://downloads.intercomcdn.com/i/o/120723416/19f94470574ae303110ae7f8/Screen+Shot+2019-05-12+at+3.20.46+PM.png)](https://downloads.intercomcdn.com/i/o/120723416/19f94470574ae303110ae7f8/Screen+Shot+2019-05-12+at+3.20.46+PM.png)

**Choose a motion detection trigger**

[![](https://downloads.intercomcdn.com/i/o/120723442/24660fa9b7456810ead5ca9d/Screen+Shot+2019-05-12+at+3.20.50+PM.png)](https://downloads.intercomcdn.com/i/o/120723442/24660fa9b7456810ead5ca9d/Screen+Shot+2019-05-12+at+3.20.50+PM.png)

**Choose a device  
**You may have to configure this device by connecting it to IFTTT

[![](https://downloads.intercomcdn.com/i/o/120723475/28098960eb3a58e790234f0c/Screen+Shot+2019-05-12+at+3.24.05+PM.png)](https://downloads.intercomcdn.com/i/o/120723475/28098960eb3a58e790234f0c/Screen+Shot+2019-05-12+at+3.24.05+PM.png)

**Configure a Trigger**

[![](https://downloads.intercomcdn.com/i/o/120723485/2098f2aeffcd86883839501b/Screen+Shot+2019-05-12+at+3.24.20+PM.png)](https://downloads.intercomcdn.com/i/o/120723485/2098f2aeffcd86883839501b/Screen+Shot+2019-05-12+at+3.24.20+PM.png)

Select  **Webhooks**

[![](https://downloads.intercomcdn.com/i/o/120723508/67afdd7e6e31ad0a120a839e/Screen+Shot+2019-05-12+at+3.24.50+PM.png)](https://downloads.intercomcdn.com/i/o/120723508/67afdd7e6e31ad0a120a839e/Screen+Shot+2019-05-12+at+3.24.50+PM.png)

Choose  **Make a Web Request**

[![](https://downloads.intercomcdn.com/i/o/120723528/d3dee0394abf95b95443124c/Screen+Shot+2019-05-12+at+3.24.53+PM.png)](https://downloads.intercomcdn.com/i/o/120723528/d3dee0394abf95b95443124c/Screen+Shot+2019-05-12+at+3.24.53+PM.png)

**Grab your Webhook URL from Meeting Room 365**

[![](https://downloads.intercomcdn.com/i/o/120723550/1ce2b45df6b68d437f94eb77/Screen+Shot+2019-05-12+at+3.25.10+PM.png)](https://downloads.intercomcdn.com/i/o/120723550/1ce2b45df6b68d437f94eb77/Screen+Shot+2019-05-12+at+3.25.10+PM.png)

**Configure this as your trigger URL**

[![](https://downloads.intercomcdn.com/i/o/120723563/d2db849d84d3da4ca30c0a02/Screen+Shot+2019-05-12+at+3.25.26+PM.png)](https://downloads.intercomcdn.com/i/o/120723563/d2db849d84d3da4ca30c0a02/Screen+Shot+2019-05-12+at+3.25.26+PM.png)

Make sure to select GET method and text/plain content type.

**Turn off notifications**

[![](https://downloads.intercomcdn.com/i/o/120723590/db126a74d2b33c5b9988465d/Screen+Shot+2019-05-12+at+3.25.36+PM.png)](https://downloads.intercomcdn.com/i/o/120723590/db126a74d2b33c5b9988465d/Screen+Shot+2019-05-12+at+3.25.36+PM.png)

You won't want to get an email each time motion is detected, unless you're just troubleshooting your initial setup.

**Click Finish**

[![](https://downloads.intercomcdn.com/i/o/120723635/ab8e3e466e6cd22971ac68be/Screen+Shot+2019-05-12+at+3.25.37+PM.png)](https://downloads.intercomcdn.com/i/o/120723635/ab8e3e466e6cd22971ac68be/Screen+Shot+2019-05-12+at+3.25.37+PM.png)

That's it!

**You should now see this IFTTT applet enabled:**

[![](https://downloads.intercomcdn.com/i/o/120723653/0aaf98513d8d8b76bc67a283/Screen+Shot+2019-05-12+at+3.25.44+PM.png)](https://downloads.intercomcdn.com/i/o/120723653/0aaf98513d8d8b76bc67a283/Screen+Shot+2019-05-12+at+3.25.44+PM.png)

Now, if you have I**nstant Reservations**  enabled, they will happen automatically (in 15 minute increments) when someone walks into an empty meeting room.

If you have  **End Early**  enabled, your meetings will end early when no one is in the room for 5 minutes or longer, keeping Outlook current.

If you have  **Force Check-in** enabled, this will occur automatically when users are present in the room.

  
As always, if you have any questions, please reach out to support and let us know. Thanks for reading!
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTEwMzY3MzAzOV19
-->