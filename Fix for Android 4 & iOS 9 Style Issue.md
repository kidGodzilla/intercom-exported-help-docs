# Fix for Android 4 & iOS 9 Style Issue

Issue: Some meeting room items get cut off on the right edge

[![](https://downloads.intercomcdn.com/i/o/64199867/061d70c218452ef9b363bd35/android-4-issue.jpg)](https://downloads.intercomcdn.com/i/o/64199867/061d70c218452ef9b363bd35/android-4-issue.jpg)

As you see in the image above, some items are cut off on the right edge.

[![](https://downloads.intercomcdn.com/i/o/64200068/67dbbb6f0dbd2e8acd2fc8d2/fix.jpg)](https://downloads.intercomcdn.com/i/o/64200068/67dbbb6f0dbd2e8acd2fc8d2/fix.jpg)

# Hardware

This issue has been reported on  **Android 4**,  **iOS 9**, and some  **proprietary**  tablet devices (Samsung, Crestron).  

# Solution

The solution is quite easy, and can be applied as a custom display style.

/* Android 4 / iOS 9 Fix */  
.meetings {  
  top: initial;  
  left: initial;  
  right: initial;  
  bottom: initial;  
  padding-top: initial;  
  overflow-y: initial;  
  width: initial;  
  height: initial;  
}  
.meetings {  
  top: 0;  
}  
.meetings.in {  
  left: 50px;  
  right: initial;  
}

  
Let us know if you have any issues!
<!--stackedit_data:
eyJoaXN0b3J5IjpbNzU4MDIwMTRdfQ==
-->