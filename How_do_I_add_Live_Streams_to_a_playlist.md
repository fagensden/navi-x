**Issue:** How do I add Live Streams to a playlist?

**Explanation:**
This instructional guide is meant to serve as a general informational guide to successfully adding live streams from the internet to Navi-X… it is not meant to serve as a fully instructional guide for telling you about each and every individual detail regarding expectations of data sniffing… unexpected things happen all the time when “sniffing” out live stream links and you are expected to have a good understanding or interpretation of how your browser works from a processing standpoint, what it is you are seeing on screen when using data sniffing tools and what it all means, as well as how to search for and find video playback variables needed for Navi-X to emulate a java-based video player. It is advised you become familiar with data sniffing, what it is, how to do it and what it is you are reading from a “data sniff”. There are plenty of articles on Google to instruct you on how to perform these “sniffs”… please read additional materials if you have troubles understanding any part of this guide. You would search for terms like this on Google… data sniffing, how to get links using wireshark, how to get video links, url snooper. Two articles have also been written in addition to this document explaining how to go about this...

http://code.google.com/p/navi-x/wiki/How_do_I_add_MMS_live_streams_to_a_playlist

http://code.google.com/p/navi-x/wiki/How_do_I_add_RTMP_parameters_to_a_media_item_in_a_playlist

**What you need to have to installed on your computer to perform this task:**
1. A web browser. Any browser will do.
2. A data sniffing program. Currently, WireShark is the suggested program of choice as it works very well at getting all variables for RTMP and RTMPe playback.
3. A working internet connection.
4. A text editor like Notepad, WordPad, or Microsoft Word.

For those who don’t know, RTMP is Real Time Messaging Protocol (RTMP) and is a proprietary protocol developed by Adobe for streaming audio, video and data over the Internet, between a Flash player and a server. There are different types of streams on the internet as well like MMS streams and other proprietary streams on the internet that will work in XBMC or Boxee, but you will want to check the supported codec formats for each media center to confirm it will work for you. Primarily, the two most common types of live streams there are are RTMP and MMS streams. Getting working links out for both of these types is done differently.

**How to get links for RTMP streams:**
The RTMP protocol has multiple variations:
1. The "plain" RTMP protocol which works on top of TCP and uses port number 1935 by default.
2. RTMPS which is RTMP over a secure SSL connection using HTTPS.
3. RTMPE which is RTMP encrypted using Adobe's own security mechanism. While the details of the implementation are proprietary, the mechanism uses industry standard cryptography primitives. Unfortunately the design of RTMPE is fundamentally flawed and provides no actual security in itself.
4. RTMPT which is encapsulated within HTTP requests to traverse firewalls. RTMPT is frequently found utilizing cleartext requests on TCP ports 80 and 443 to bypass most
corporate traffic filtering. The encapsulated session may carry plain RTMP, RTMPS, or RTMPE packets within.

If you would like more information on RTMP and how it works, check out this link. http://en.wikipedia.org/wiki/Real_Time_Messaging_Protocol

**So here is a run down of how a data sniffing program works:** typically, you install and open the program and search for a “Start” button or something similar to that function. The “Start” button begins the sniffing of your ethernet ports data traffic for http header and body data… particularly URLs or links to external resources on the internet like pictures, video files and rtmp streams. As each resource is requested through your web browser by a website for example like Adult Swim, the links are picked up on the data sniffing program for all types of media and aggregated to a list within the data sniffing program. When an RTMP stream is loaded, this will be indicated in the list of links with rtmp:// or rtmpe:// at the very front of the link. You can generally just browse up and down the list and check for these pre-fixes to the links. These are the stream links you are looking for.
In addition to getting the actual streaming link for the source, you need to establish a handshake between the server and your device in order for the stream to become active and working for your device… this is where the RTMP variables come into play.

There are numerous different RTMP variables for video playback. These are normally handled by the java-based media player on a website and they automatically establish the handshake to enable the stream to your ip address for you when you click on the link from the broadcaster’s website. The problem is live stream broadcasters usually are very particular about controlling who and how you get to their video streams because it costs money to stream live streams. Using RTMP prevents people from just grabbing the link and their bandwidth usage from going out of control by controlling who has the “keys” to access it. These are the RTMP parameters.

**Here is an old example of a Navi-X playlist entry for an RTMP live stream:**
```
type=video 
name=BBC News 
URL=http://livestation.com/bbcnews 
playpath=bbcnews_en_high.sdp 
swfUrl=http://www.livestation.com/flash/player/5.4/player.swf 
swfVfy=true 
live=true
```

**In this case, the RTMP parameters are as follows:**
```
playpath=bbcnews_en_high.sdp 
swfUrl=http://www.livestation.com/flash/player/5.4/player.swf 
swfVfy=true 
live=true
```

**Here is how I got the RTMP parameters for this live stream:**
1. Open the data sniffing program and hit “Start” to start sniffing ethernet ports.
2. Opened a web browser and went to livestation.com
3. Browsed to the news section > BBC Live and opened the webpage to begin the live stream.
4. Wireshark intercepts the data coming in from the live stream and shows the GET/POST header of the file accessed via the page request caused when you click on a link to a live stream.
5. In the list of collected links, I clicked on the one found starting with “rtmp://” and read the GET/POST data collected from the clicked link.
6. In the GET/POST results, I found the different rtmp parameters followed behind the rtmp link… it included “playpath, swfUrl, swfVfy and live” parameters. Keep in mind, because people can assign their own player variables, there may be more or less per stream sniffed.
7. I added the parameters to each new line in the playlist entry and manually uploaded my playlist on a file server.
8. I browse to my playlist and hit the link and the live  stream played.


---


**How to get links for MMS streams:**
For those who don’t know, Microsoft Media Server (MMS) is the name of Microsoft's proprietary network streaming protocol used to transfer unicast data in Windows Media Services (previously called NetShow Services). MMS can be transported via UDP or TCP/IP. The MMS default port is UDP/TCP 1755.

MMS streams are a toss up… sometimes they require authentication tokens for content delivery, sometimes just adding the link directly to the MMS link is enough to get the stream to work… you typically won’t know until you sniff for the link to find out what type of output your website being sniffed is producing.
For example, I went to the Knive and Gun Show website and captured a link with authentication tokens required for playback… the link is mms://stream.netro.ca/thebroadcastchannel

It does not have a token request in the body of the link, therefore I can add this link to a playlist no problems and it will play. Select type as video and that’s it!

However, most other websites use security authentication directly in the body of the URL that allows the stream for only 1 user (ip address tagged) and within a short amount of time for that user to access the link generated. For example, I went to a website and tried to grab a stream link and it was like this… mms://somevideowebsite.com/bbcnews/1.asf?token=adf897vhw08efv7

These types of links would require a “processor” or web script for resolving URL’s accordingly. The tokens are generated using a webscript from their servers… if you can successfully decompile the java-based media player on their website after locating it and get the algorithm they are using to generate tokens, you can then write a processor of your own to generate the tokens for you on the fly using scrapers and processors in Navi-X. Information on this can be found elsewhere on Navi-Xtreme or the wiki section. We do not provide information on how to decompile java-based media players here… you would have to read up on this yourself and have a decent understanding of how to write and calculate regular expressions for java. This information is also not being discussed here… you will need to look it up on Google or elsewhere to figure that out.

**Article Notes:**

1. The reason many things are not being discussed here is because there are numerous articles elsewhere on the subjects discussed and we do not intend on re-writing a comprehensive tutorial on decompiling java players or writing regular expressions… use a search engine to learn how to do this stuff.
2. This article is written for advanced computer users only. If you are a general user, without a lot of reading and learning, you will pretty much never get live streams added correctly in Navi-X… that’s just the way it is. You need to have a lot of self ambition to understand how this stuff works and we are not going to spoon feed it to you… it is a very in depth and complicated endeavor to understand and will require you to do a lot of self learning in order to add live streams if you are not familiar with how to do so.
3. Please do not ask me to explain the article further… from this point, you need to ask Uncle Google your questions and do some reading… good luck!

Written by:
iRoNBiLL