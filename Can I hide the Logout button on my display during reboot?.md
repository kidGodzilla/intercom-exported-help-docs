# Can I hide the Logout button on my display during reboot?

Each time the tablet display starts, a small Logout button along with the display key is presented, in case you need to log out of the application, clear the application's cache, or join it to your admin portal.

[![](https://downloads.intercomcdn.com/i/o/76468287/d7ec91a656fa96ac9874e00b/Screen+Shot+2018-09-14+at+6.58.00+PM.png)](https://downloads.intercomcdn.com/i/o/76468287/d7ec91a656fa96ac9874e00b/Screen+Shot+2018-09-14+at+6.58.00+PM.png)

If you would like to hide the logout button and display key from appearing, you can use the following code, as a custom style override:

.bottom.left {  
display: none !important;  
}
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTg3ODI3Njk0XX0=
-->