**Issue:** How do I add RTMP live streams to a playlist?

**Explanation:** Adding RTMP parameters to a live stream URL for playback in Navi-X is not an easy task and should only be taken up by those skilled in "port sniffing" and deciphering relevent data from GET/POST results delivered in a data sniffing program like WireShark. NO TUTORIAL WILL BE PROVIDED ON HOW TO USE AND DECIPHER CODE IN THIS PROGRAM. PLEASE GOOGLE SEARCH INFORMATION ON HOW TO DO THIS. ALSO, PLEASE READ THE WIKI ARTICLE HERE ON "WHAT IS A PLAYLIST" IF YOU ARE UNFAMILIAR WITH THE MANUAL EDITTING OF NAVI-X PLAYLISTS AS THIS IS REQUIRED TO CREATE RTMP COMPATIBLE MEDIA ITEMS AND IMPORT THE PLAYLIST TO NAVI-XTREME AFTERWARDS.

RTMP Media Item Entry Example:

```
type=video
name=BBC News
URL=http://livestation.com/bbcnews
playpath=bbcnews_en_high.sdp
swfUrl=http://www.livestation.com/flash/player/5.4/player.swf
swfVfy=true
live=true
```

You may also use the traditional URL formatting in a single line like this...

```
type=video
name=BBC News
URL=http://livestation.com/bbcnews playpath=bbcnews_en_high.sdp swfUrl=http://www.livestation.com/flash/player/5.4/player.swf swfVfy=true live=true
```

**Note: This used to be a working example and is no more. This live stream has since stopped working because the user broadcasting this channel is no longer broadcasting it. Don't try plugging it in a playlist as it will not work! This is strictly for an example of what tags must be included in a working stream.**

**Boxee Users: Boxee 1.5.x versions DO NOT SUPPORT LIVE STREAMING via RTMP, RTMPe or any other variation of RTMP. When Boxee does start supporting this, this notice will be removed! Thanks!**

**If you find live streams using the traditional URL formatting in a single line (long-string rtmp entries) on the internet somewhere, you should be able to add them to a playlist and then just set the item type as video to add them to a playlist.**

In an RTMP media entry, there are several playback parameters that have to be configured in order to get a live stream via rtmp to playback in Navi-X.

While working manually with playlists, you may already be familiar with the "type", "name" and "URL" tags, but in addition to these necessary entries, for live streams their needs to be the addition of several additional parameters to the media entry in order to make it work successfully in Navi-X:

"Playpath", "swfUrl", "swfVfy" and "live" are these tags. Sometimes there will be additional, undocumented variables to handle due to the nature of how RTMP functions... these may need to be added to the RTMP entry as well... Only those who understand how to decipher GET/POST results would know how to do this. When you go to decipher the GET/POST data you are receiving via a port sniffing program, you will get these variables in your data... the primary handling variables need to be added in order to make the stream work... plain and simple.

The trick is getting the correct data to plug into these variables so that the video will play back. If you can successfully figure out and extract these and add them to your media item, the live stream via RTMP will work in Navi-X. Typically, when reading GET/POST results, this should read out in text and be pretty easy to figure what part in the results you need included in the RTMP entry.