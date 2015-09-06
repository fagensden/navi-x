**Error:** Playlist Playback Aborted Too Many Consecutive Failed Items.

**Explanation:**
This issue happens when the media center's player and/or code libraries fail to operate properly due to an exception it could not handle that was thrown at it by Navi-X.

This can be due to several possibilities. Typically, the player was not able to handle a particular aspect of a video, audio or image file it attempted to playback or display. Either the format of the file was unsupported, an unspecified encoding property of the file could not be handled by the player, the media center API's or libs failed (example: XBMC's python interpreter) or the file is corrupted.

**To Fix This Issue:**
Try to restart the media center application you are using, then open Navi-X and find the item in question and try to play it back again. If the file fails to playback, this is likely due to the file not being supported by your media center, an unspecified encoding property of the file could not be handled by the player or the file is corrupted or missing from the file server.

It is recommended you either file a bug request with the support site for your media center or wait for your media center developers to address playback issues with common files during their regularly schedule maintenance updates.