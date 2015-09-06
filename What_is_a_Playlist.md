**Issue:** What is a Playlist?

**Explanation:** When we refer to a playlist in Navi-X, we are discussing a list of multimedia items and menu selections that appears in Navi-X while browsing the heirarchichal menu structure.

A playlist is a catalogued list of multimedia items in a single list for browsing and playback of multimedia content. It is similar to a music playlist, in which you can arrange items in a list and play them back sequentially. The idea of a playlist is to create a sorted or unsorted arrangement of multimedia links so that others may share their findings on the internet with others or catalogue their findings for personal use.

Playlists are typically created and maintained at http://www.navixtreme.com when you create a free account for hosting your playlists. You can then use the playlist editor and begin creating, arranging or importing playlists into your very own playlist arrangement for sharing or personal viewing. More details on how to use the playlist editor on Navi-Xtreme will be covered in a later article.

Playlists are created manually in a text editor or by using the playlist editor hosted on Navi-Xtreme. You can save the playlists as a .txt or .plx (basically Navi-X playlist just saved in a text as .plx)

Here is an example of what a playlist looks like in a text editor:

```
version=1
background=http://1.bp.blogspot.com/-Hfy8FQyFhYE/TpLDD5efp0I/AAAAAAAAAZI/Vp6glf1Wpc8/s1600/thanksgiving-wallpaper-5.jpg
title=iRoNBiLL's Playlist
logo=http://www.fileden.com/files/2010/8/4/2932808/newlogo3.png
description=Check out brand new episodes of Aqua Teen Hunger Force season 10 in it's new show titled, Aqua Unit Patrol Squad 1!!! Available in my Adult Swim playlist now!!  - iRoNBiLL/description

type=video
name=The Greatest Speech Ever Made by Charlie Chaplin
thumb=http://img.youtube.com/vi/pK2WJd5bXFg/default.jpg
URL=http://youtube.com/v/pK2WJd5bXFg.swf
processor=http://navix.turner3d.net/proc/youtube
player=default
rating=-1.00

type=playlist
name=Latest Favorite Show - Sons of Anarchy
thumb=http://upload.wikimedia.org/wikipedia/en/thumb/c/ca/Soaintertitle#jpg/250px-Soaintertitle.jpg
URL=http://navix.turner3d.net/playlist/search/sons%20of%20anarchy
player=default
rating=-1.00

type=playlist
name=Adult Swim
thumb=http://images.sodahead.com/polls/001170413/large_Adult_Swim_Logo_#answer_2_xlarge.jpeg
URL=http://navix.turner3d.net/playlist/19201/adult_swim.plx
player=default
rating=-1.00
description=A catalogue of Adult Swim shows and episodes. Enjoy! - iRoNBiLL/description

type=playlist
name=Music Videos
thumb=http://www.fileden.com/files/2010/8/4/2932808/newlogo3.png
URL=http://navix.turner3d.net/playlist/36339/music_videos.plx
player=default
rating=-1.00

type=playlist
name=Mixtapes
thumb=http://www.fileden.com/files/2010/8/4/2932808/newlogo3.png
URL=http://navix.turner3d.net/playlist/36078/mixtapes.plx
player=default
rating=-1.00

type=playlist
name=Shoutcast Radio Stations
thumb=http://www.fileden.com/files/2010/8/4/2932808/newlogo3.png
URL=http://navix.turner3d.net/playlist/55239/shoutcast_radio_stations.p#x
player=default
rating=-1.00

type=playlist
name=Websites (Boxee Box Only)
thumb=http://www.fileden.com/files/2010/8/4/2932808/newlogo3.png
URL=http://navix.turner3d.net/playlist/49533/websites_#boxee_box_only).plx
player=default
rating=-1.00

type=playlist
name=Podcasts
thumb=http://www.fileden.com/files/2010/8/4/2932808/newlogo3.png
RL=http://navix.turner3d.net/playlist/19196/podcasts.plx
player=default
rating=-1.00
description=Podcasts for those on the go.../description

type=audio
name=Weslochan Global Recordings Show - Show 5 - September 28, 2011
thumb=http://weslochanrecordings.podbean.com/mf/web/jfuqwg/weslochanminimalsessions5.jpg
URL=http://weslochanrecordings.podbean.com/mf/web/8wkrqu/episode5.mp3
player=default
rating=-1.00

type=video
name=24 Hours of Neon (Las Vegas, Time-lapse)
thumb=http://blog.galavantier.com/wp-content/themes/Yen/timthumb.php?src=http://blog.galavantier.com/wp-content/uploads/2011/06/24hoursofneon-1024x664.png&w=580&zc=1
URL=http://vimeo.com/23413966
processor=http://navix.turner3d.net/proc/vimeo
player=default
rating=-1.00
description=by Philip Bloom/description

type=rss:
name=Twitter Feed
thumb=http://website.navi-x.org/networks/logos/twitter_logo.png
URL=http://twitter.com/statuses/user_timeline/46805533.rss
background=http://img.wallpapermenu.com/only-blue-wallpapers_7167_1280x1024.jpg
player=default
rating=-1.00
```

Here is the breakdown of our playlists... each playlist has a header to identify key aspects of a playlist, like a predominant logo, background and title for the playlist like the example above.

In this playlist example, the header consists of the following:

```
version=1
background=http://1.bp.blogspot.com/-Hfy8FQyFhYE/TpLDD5efp0I/AAAAAAAAAZI/Vp6glf1Wpc8/s1600/thanksgiving-wallpaper-5.jpg
title=iRoNBiLL's Playlist
logo=http://www.fileden.com/files/2010/8/4/2932808/newlogo3.png
description=Check out brand new episodes of Aqua Teen Hunger Force season 10 in it's new show titled, Aqua Unit Patrol Squad 1!!! Available in my Adult Swim playlist now!!  - iRoNBiLL/description
```

"Version" is technically not really used anymore and has been phased out of newer versions of Navi-X. It used to be important during earlier versions for determining playlist revision compatibility.

"Background" references a link to an image file you would like to use for a background for the playlist.

"Title" refers to the title name of a playlist.

"Logo" references a link to an image file you would like to use as a logo for items in the playlist. When you do not assign a thumb to a media item, this image will be placed where the thumb for a media item would appear.

"Description" is for inputting a custom text description and introduction for your playlist. You can access descriptions in playlists for XBMC by pressing right twice on your keyboard or remote.

"View" is a fairly new variable not listed in this header, but can be used to choose a default viewing layout for the playlist. Adding "view=thumbnails" will display your playlist in large icons for selection while"view=default" or "view=list" will display the playlist in a heirarchical layout.

The remainder of the playlist should be pretty self explanatory in terms of what it means. You can almost read the playlist verbatim in english. Each variable in the media items in the playlist is self explanatory, except for rating, which is a variable used in Navi-Xtreme when people rank your playlist, the rating is reflected here.

You can also check out our old manual for Navi-X on pages 13 and 14 for more details about how to manually create playlists.

**Old Navi-X Manual**
http://www.box.com/shared/g452jas3ck