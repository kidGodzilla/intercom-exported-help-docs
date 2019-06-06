# Customizing your Status Board Display


Right now, you can customize the logo, title, and brand color (which all appear at the top of the display).

[![](https://downloads.intercomcdn.com/i/o/120717505/6c840ec2aa626ff058fa554f/tv-h-plus.jpg)](https://downloads.intercomcdn.com/i/o/120717505/6c840ec2aa626ff058fa554f/tv-h-plus.jpg)

Additionally, you can choose between a light and dark theme (for the meeting room spaces themselves), and customize the display with custom CSS and translation files (a bit like the meeting room displays).  
  
We also have some options around sorting (either alphabetical or pushing available rooms to the top), and what happens when there are too many rooms to display at once (by default it scrolls through the rooms every few seconds).

Most of these options are available today in the admin portal, and can be configured using a GUI. However, during development, many of these features are implemented first via a URL change. So, I will document those here as well for beta users:  

demo=1  
Shows dummy data for demonstration purposes  
  
brandColor=ffaa00   
Lets you set the brand color via URL param. This is an RGB hex code (similar to what is used on the web). This can also be set in the admin portal.  
  
logo=[https://mydomain.com/logo.png](https://mydomain.com/logo.png)   
Lets you set the URL to your logo. This can also be set in the admin portal.  
  
locationKey=mainoffice   
This lets you set a location key, similar to a room finder key, which limits the number of rooms which will appear on your status board  
  
rotate=-90   
This allows you to rotate the entire display either 90, -90, or 180 degrees, so that you can mount your display in any position you like, regardless of whether your display allows for rotation (many older monitors make great status board displays but do not support rotation).  
  
sortby=status   
This sorts all rooms by status (useful if you don't have many rooms), instead of just alphabetically by room name.  
  
theme=light or theme=dark   
This lets you swap out light and dark themes  
  
scroll=no   
This allows you to disable scrolling / pagination of rooms, if you have too many to display at one time.  
  
descriptions=0   
This allows you to disable the room description column, which may look better, depending on your display size

  
An example of a  [URL](https://meetingroom365.com/statusboard/?demo=1&domain=demo&brandcolor=ffaa00&logo=https://meetingroom365.com/mr365-hb-w@2x.png&sortby=status&scroll=no)  with multiple parameters set via URL:

[https://meetingroom365.com/statusboard/?demo=1&domain=demo&brandcolor=ffaa00&logo=https://meetingroom365.com/mr365-hb-w@2x.png&sortby=status&scroll=no](https://meetingroom365.com/statusboard/?demo=1&domain=demo&brandcolor=ffaa00&logo=https://meetingroom365.com/mr365-hb-w@2x.png&sortby=status&scroll=no)

(For demonstration purposes only. You will set a  `key`  instead of setting  `demo`  and  `domain`.  
  
If you have any questions, please reach out and contact support!
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTY3MTYyOTE0Ml19
-->