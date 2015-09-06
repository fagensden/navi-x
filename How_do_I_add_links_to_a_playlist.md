**Issue:** How do I add links to a playlist

**Explanation:**
**Static URL’s vs. Dynamic URL’s - Understanding the basics** -
Adding links to a playlist in Navi-X is a fairly straightforward process, but keep in mind that technical issues can prevent playback of media content when added to a playlist for many different reasons. If for some reason, your media is not adding or working properly in Navi-X, head over to http://www.navixtreme.com/forums and make a forum post about it, give us the link you are trying to make work in Navi-X and we can provide you with an explanation of what it will take to make the media you want to play in your media center from Navi-X. Don’t just give up on making something work in Navi-X… let us help you figure out why your media player will not play it.

There are typically two kinds of links on the internet… Static links and Dynamic links. Static links are those that link directly to a file with the file extension included in the URL itself. Dynamic links are basically links that point to a media item indirectly and typically do not have a file extension in the body of the URL.

Static links typically look like this:
http://www.whatever.com/myfavoritemovie.mp4 ...
Or .avi, .mp3, .ogg… basically a “dot” and three letter file extension of the file type... located at the very end of the URL, indicating the file type, as well as the fact it is a direct static link.

Dynamic links look like ANYTHING OTHER than static links, meaning there is no three letter file extension directly in the body of the URL. Here are a couple of examples I grabbed for “The Lorax” movie…
http://www.vidxden.com/7wgczt27o9qe/12907.flv.html
http://www.novamov.com/video/p78l6b0begulo

In the examples for dynamic links, you can see these URL’s link directly to webpages only and not to the actual URL of the file name that gets played in the media player directly.

Normally, computer experts would use what is called a “port sniffer” to “sniff” out URL’s that are being run through your computers browsers, through your media player within the browser and your computers network card as you load webpages from the internet. A catch list would then intercept and notate these for you in a running list. Port sniffing is a complicated endeavor and should not be taken up by those who are not capable of researching and figuring out themselves how to do this. It is not rocket science, but it does require you to independently learn how to do this yourself. A tutorial will be developed on this subject later to attempt to explain how this works.

Essentially, what happens when someone clicks on a link in a browsers media player is that the actual URL of the file being stored on a server somewhere is secretly handed to your video player when a site verifies your ip address, typically. Your player then loads the true location of the video hosted on their servers and begins to play on your java player in the browser… in general, content providers and broadcasters do not want you to have these links because they do not want users just linking to the files directly and sharing them with whoever. Content providers essentially then lose control over who is seeing what on your website as well as sometimes circumventing the injecting of ads they love to give us all the time. This is why we don’t get direct links to these files from service providers.

These are how dynamic URL’s work and as such, a “processor” or web script to resolve the true URL’s to your player directly are developed to make these types of links work. People volunteer to create, host and continuously maintain these scripts and as such can stop at anytime they wish. A complete list of currently active processors can be found here so you know which ones you can just link to web pages from: http://www.navixtreme.com/proc_list

If you know how to do some web scripting, write regular expressions and can figure out how to resolve a dynamic URL to make a “processor”, then check out this section to learn how to develop processors for your favorite website: http://www.navixtreme.com/proc_docs/

The reason you need to know the differences between static links and dynamic links is most folks are under the impression that you can just add links you get from wherever into a Navi-X playlist and it will simply work… THIS IS NOT CORRECT! Now that you know the difference between the two, you are ready to start finding links to content on the internet!

**How Do I Add Links To Navi-X from the Navi-Xtreme Website?**
To add links to Navi-X from NaviXtreme.com, you need to go to the site and then click on “create an account” before you can start making playlists and adding links to Navi-X.

**Registration Note:
I highly suggest before doing this, you go into Internet Explorer and hit “Tools” (or the gear icon) and “Internet Options” and delete your “Temporary Internet Files” before trying to register on our site.  If you use Mac, you will want to do this in Safari and if you use Linux, you will want to do this in Firefox to ensure the folder is cleared. Make sure you restart the browser and try registering again if your registration does not go through. Failure to not do this may prevent your registration from registering on our site due to technical issues. There is no other fix for this… only doing this correctly will fix registration issues.**

Once you have created your free playlist hosting account, click on “My Playlists” to go to the Navi-X Playlist Creator.
![http://i1061.photobucket.com/albums/t461/billdaly111/nx1.jpg](http://i1061.photobucket.com/albums/t461/billdaly111/nx1.jpg)




Once you are in this menu, you will want to click on “Create new playlist” to begin creating your first playlist.
![http://i1061.photobucket.com/albums/t461/billdaly111/nx2.jpg](http://i1061.photobucket.com/albums/t461/billdaly111/nx2.jpg)




Once you clicked on creating a new playlist, you will be presented with the main playlist editor options. In here, you can begin editing the properties of your playlist, including the name or “Title”, description of the playlist, link to a background image, a logo and custom playlist icon for your playlist. If your playlist contains adult content, please mark it as such. You can then decide if you want the playlist to show up for everyone or just your devices.

Once you have edited your playlist properties, you can click on “Create” to start adding links to your playlist. Hit “Add new entry” to begin adding links to content on the internet.
![http://i1061.photobucket.com/albums/t461/billdaly111/nx3.jpg](http://i1061.photobucket.com/albums/t461/billdaly111/nx3.jpg)



When adding an item entry into a playlist, you are given several properties to fill in. The only required properties for a link in Navi-X are “Type”, “Name” and “URL”. “Type” is referring to what kind of media item are you trying to add… a video, audio, rss podcast, a web page or html (boxee only via browser), etc. “Name” is what you would like the link referenced to be called and URL is the static or dynamic link of the media entry. You optionally can add a link to a thumbnail picture that will show next to the item when you highlight it in the list in Navi-X, as well as offer a description of what the item is. In Boxee, you hit right twice to view this when the item is highlighted… you press right only once in XBMC to view this.

“Player” can be used to force either mplayer or dvdplayer in XBMC for those who want the option and “Insert at” is used for placement of the media entry in the playlist… either the very top or very bottom of the playlist. Once you have entered all the data you wish to on a media entry, click on Save to add it to your playlist. The media entry instantly becomes available on your playlist in Navi-X. You will have to refresh the playlist if you are currently in it by backing out of your list and re-entering it again.
![http://i1061.photobucket.com/albums/t461/billdaly111/nx4.jpg](http://i1061.photobucket.com/albums/t461/billdaly111/nx4.jpg)



On the right side of each entry are several other options for playlists or media item entries… Edit, Delete, Recheck and Move. “Edit” allows you to edit the current items properties. “Delete” will remove the media entries off of your current playlist. “Recheck” will check your link to see if it is active and valid. This is one of the great advantages is that Navi-Xtreme checks playlists to see if items are good or not and if it is discovered through playback that the links have stopped working, they are hidden in your playlist so people do not click on them. Results may vary. “Move” allows you to move the position of the media entry in your playlist.
![http://i1061.photobucket.com/albums/t461/billdaly111/nx5.jpg](http://i1061.photobucket.com/albums/t461/billdaly111/nx5.jpg)



**Other Notes Regarding Adding Links To A Playlist**
Live streams in particular are a very hard media entry to add if you do not know how to do this thoroughly. Many times, when you try to capture a live stream media entry, the stream itself may not be working, thus the link you are grabbing will not work in Navi-X. RTMP streams require more than 1 parameter in the body of the URL to make work and if you do not know how to do this, you should read up more about rtmp streams before attempting to add them to Navi-X. Most RTMP and MMS streams will currently only work on XBMC. Boxee has broken support for these in their app. MMS streams work fine in Navi-X, however they must use port 80 in order to work.

**RSS Feeds, XML Feeds and YouTube Playlists**
In Navi-X, there is a fully customize RSS and XML parser built in to read and render a feed as a Navi-X playlist. **Not ALL feeds will work out of the box when added to a Navi-X playlist.** Sometimes we need to examine an rss feed and update Navi-X to make it work. If you have an RSS feed that does not work, please let us know at http://www.navixtreme.com/forums and as for YouTube playlists... from time to time the parser for this breaks down. Report it to us at http://www.navixtreme.com/forums and we will take a look at it for you. Normally it should work, but it does break at times due to changes from YouTube's end of web workings.

If anyone would like me to expand on certain areas of this tutorial, please let me know at xironbillx@gmail.com at anytime and I will include them in here.