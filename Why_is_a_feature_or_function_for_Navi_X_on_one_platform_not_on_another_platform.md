**Issue:** Why is a feature or function for Navi-X on one platform not on another platform?

**Explanation:** Not all platforms are created the same. Even slight differences can throw off functionality completely between one media center app and another. At this time we are currently working on implementing all functions from XBMCs version of Navi-X to Boxee's version and others, but this will take some time. Remember, Navi-X was originally an XBMC exclusive app only, now it is a multi-platform app and we are working to extend all functions to all platforms in time.

**Notes:**

Not all menus in Navi-X are accessible on another platform.

Boxee has a built in web browser than can be utilized with Navi-X links...
Navi-X on XBMC does not.

Navi-X on XBMC has a download feature...
Navi-X on Boxee does not.

Navi-X on XBMC supports RTMP and MMS Live Streams...
Navi-X on Boxee does not.

Navi-X on XBMC or Boxee supports Navi-X "processors"...
Navi-X on WiiMC does not.

This means any links that are not DIRECTLY linking to a file on the internet will not work. (example: http://www.whateversite.com/vids/blahblah/nameofthemovie.mkv... or .avi, .mp4... so if you do not see a file extension on the end of the link, the link will not work in WiiMC.

This is due to the lack of a python interpreter in WiiMC. Porting the processors to C+ would make them work, but no programmer has stepped up to take on the task in 2 years of searching.

Playstation support via Channel Plugin for Playstation Media Server and Showtime also have similar limitations and are not as aggresively developed as XBMC and Boxee ports.