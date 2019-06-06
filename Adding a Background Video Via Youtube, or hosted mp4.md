# Adding a Background Video

Via Youtube, or hosted mp4

This article aims to resolve frequently asked questions or simple issues around video playback, embedding, looping, and hosting.

## Youtube

If you would like to embed youtube videos as animated backgrounds, generally the following applies:

1.  Your video must allow embedding. Also, it can be unlisted, but it cannot be private.
2.  For looping, autoplaying video, the following URL format works best:  `https://www.youtube.com/embed/<VIDEO-ID>?rel=0&controls=0&showinfo=0&autoplay=1&loop=1&playlist=<VIDEO-ID>`

For example, if your video URL was  `https://www.youtube.com/watch?v=ZcBw06UbAws`  , your video ID would be:  `ZcBw06UbAws`  , and your animated background URL would be:  `https://www.youtube.com/embed/ZcBw06UbAws?rel=0&controls=0&showinfo=0&autoplay=1&loop=1&playlist=ZcBw06UbAws`  

## MP4 Video

You can self-host video files as well, and enter the full URL to the video as your animated background URL. However, at this time, only .mp4 video is supported. This is because each device supports a different set of video formats, the common one being mp4.  

## Bitrate and Encoding

You should not have to worry about this if hosting via Youtube embed. However, there are additional flags you can use in your URL. For example, you can add  `&vq=small`  to the end for low quality (if you have bandwidth issues), or  `&vq=medium`  . Other attributes available are  `large`  ,  `hd720`  , and  `hd1080`  .
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTI1ODEzMzUyM119
-->