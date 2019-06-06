# Using IFTTT to trigger a Hardware Action based on Meeting Room Status

### Turn on or change the color of a light when a meeting room becomes occupied or available

![](https://downloads.intercomcdn.com/i/o/120721133/4211205e051eddd5920a321f/1%2AamfVeTYuBy2fAwR4lDfGiw.png)

We've added IFTTT support to Meeting Room 365, which now gives you the ability to quickly configure hundreds of smart devices to interact with your meeting room displays. In this example, we'll configure a Phillips Hue bulb, based on our current Meeting Room status.

![](https://downloads.intercomcdn.com/i/o/120721134/21ba5fb9c4a2029fd0f52099/1%2ADiieKR-42m5QyJnNCH7kzg.png)

#### Trigger an action based on Meeting Room Status

Below are some very basic instructions for connecting a Meeting Room 365 Display with external hardware via IFTTT.

#### Applet Template

For this example, your IFTTT applet will listen for an event sent from a Meeting Room 365 display, updating your lighting status when the event is received. Below is the completed applet template.

You can pick any event names you like, however, you must supply us with the event names, one when the display becomes **“available”**, and one when the display becomes **“occupied”**. Keep in mind, these may be fired more than once.

![](https://downloads.intercomcdn.com/i/o/120721136/5645fd3c8d9d00fd76e7e2a1/1%2ACa_HOfkkFWgyKVSwgE6ZnA.png)

Before you begin
----------------

Before you begin, you will need to create two keys, which can be anything you like. These do not need to be secret, they're just a string used for an event name.

The first key will be unique to your meeting room, and will be fired each time your meeting room becomes available (and possibly multiple times while it is still available). In our example, I came up with `meeting_room_1_available`.  
  
The second key will be similar, but it will be fired when the meeting room is occupied. I chose `meeting_room_1_occupied`. You can choose whatever you like. 

You will need to create a new key for each meeting room you wish to configure.

You will also need to sign up for an IFTTT account, and have your hardware ready to test.  

Steps in IFTTT
--------------

The following steps are completed in IFTTT, which manages your hardware integrations:

#### Create a New Applet

![](https://downloads.intercomcdn.com/i/o/120721137/6e8cb6e85885739623a33d25/1%2At4OGI748iKcSc6haw0RwAw.jpeg)

**Choose the Webhooks service**

![](https://downloads.intercomcdn.com/i/o/120721138/f10ff49ccb027e562eb6993b/1%2AEkqzgK5Wg0Kev94szcRUMg.jpeg)

**Choose a Trigger**

![](https://downloads.intercomcdn.com/i/o/120721140/2621a363002b1c9f9b90b158/1%2AsuOm0w6pdbPgPY_lMRBR5Q.jpeg)

**Enter your trigger key name**

![](https://downloads.intercomcdn.com/i/o/120721141/b377f1d628fd9fd78d5ceaa8/1%2AWL938z1cfWUtD-Tn-PfYXw.jpeg)

**Create an action**

![](https://downloads.intercomcdn.com/i/o/120721142/fb69e1c857a4738faa9bacf2/1%2A852y3zgJ7MIggScce1f3Xw.jpeg)

**Configure an action (result) of meeting room status changes**

\*This will depend on your hardware. See IFTTT documentation for more details. 

![](https://downloads.intercomcdn.com/i/o/120721143/bfc1205e5c4f0d2cdb5b5bff/1%2AvuUdTCc_Xz0tubmgBi0Bbg.jpeg)

![](https://downloads.intercomcdn.com/i/o/120721144/42071fe2b7fe29b44b1a7ac5/1%2ArLoNLPCsiYL3-adidQQbog.jpeg)

![](https://downloads.intercomcdn.com/i/o/120721146/00441984e17396cb9bf9281e/1%2AaULw7eCzaZhk2HowS3YCnw.jpeg)

#### Congratulations! You've set up your first action.  

You will need to repeat this for your `occupied` event, and any other rooms you wish to enable.

  
Get your IFTTT Maker Key for Webhooks  
Next, you'll need to get a key which Meeting Room 365 uses to push webhooks to IFTTT. You can find that here: [https://ifttt.com/services/maker\_webhooks/settings](https://ifttt.com/services/maker_webhooks/settings)

You'll need to copy the section of the URL we've blurred to your Meeting Room 365 configuration. Since you will need to do this for each display, you might want to document this along with your meeting room names and the keys you chose.  
  

![](https://downloads.intercomcdn.com/i/o/120721018/de2fd354044528a1edd4983c/Artboard.jpg)

Update your Meeting Room configuration in Meeting Room 365
----------------------------------------------------------

Next, you will update your meeting room configuration in Meeting Room 365.

  
**Click to enable IFTTT events to be sent**

![](https://downloads.intercomcdn.com/i/o/120721036/3b76d8edcd8dc7758624496b/Screen+Shot+2019-05-12+at+2.31.52+PM.png)

**Enter your IFTTT Webhook key, and your event keys**

![](https://downloads.intercomcdn.com/i/o/120721074/b05f3af31774973ac86ae4b8/Screen+Shot+2019-05-12+at+2.32.14+PM.png)

That's it! You can now test your lights by making an instant reservation, and see their status change.

You can verify that your event fired in IFTTT from the IFTTT admin portal.
<!--stackedit_data:
eyJoaXN0b3J5IjpbNzM4NTA4OTczXX0=
-->