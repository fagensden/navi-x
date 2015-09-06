**Issue:** How do I add MMS live streams to a playlist?

**Explanation:** MMS live streams can be added and used in Navi-X from all kinds of sources. Some sources however, add authentication measures to their live streams many times and make it hard to add a live stream to Navi-X, without a web script processor to resolve url's for users.

You should have a thorough understanding of how to use a "port sniffer" or data sniffer to read incoming media url's to your network card. If not, please read up about how to use these on Google search. For the sake of argument, I am going to discuss URL Snooper 2 as my basis for capturing an MMS link.

So, let's say I want to capture a live stream from a website so I can put this in Navi-X... I would start URL Snooper 2 and hit start to start port sniffing. Once it began, I would open a web browser and go to the website with the live stream I want to add to Navi-X. Once I bring up the actual page with the live streaming video on it, URL Snooper 2 should automatically capture the URL for the live stream in it's capture results. When I view the list, I look for either rtmp://, rtmpe:// or mms:// prefixes in the links listed in the captured results list.

RTMP and RTMPE require a different way of adding these to a playlist in order to make them work. Please refer to http://code.google.com/p/navi-x/wiki/How_do_I_add_RTMP_parameters_to_a_media_item_in_a_playlist  for instructions on how to make these live streams work.

If I find an mms:// link, I will examine the link itself to see if some sort of authentication has been included for the video stream itself. This is typically indicated when you look at the URL you captured and somewhere in the URL itself, you will possibly see something like "...?token=G8BG67B8OUTV7ITB7I6R8OI7" OR "...ipaddress=x.x.x.x..."

IF YOU SEE THIS OR SOMETHING THAT APPEARS TO BE A METHOD OF AUTHENTICATION IN THE BODY OF THE URL, YOU CANNOT DIRECTLY ADD THESE TO NAVI-X WITHOUT CREATING A PROCESSOR FIRST TO RESOLVE URLS ON THE FLY FOR USERS ACCESSING THE CONTENT. Directions for this can be found here: http://code.google.com/p/navi-x/wiki/What_is_a_Processor

If you get an address however similar to mms://www.whatever.com/bbcnews/1.wmv, where you don't see any authentication methods being written into the body of the URL, these can typically be added to Navi-X without further work. Simply copy and paste the mms:// link into a Navi-X playlist and set the type as video and give the item a name... that's it! Sometimes you have to use http:// instead of mms:// in order to make it work, but either way should add the link successfully to the playlist for playback. Once the link is on a playlist, click it to enjoy playback.