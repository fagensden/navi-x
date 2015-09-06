**Issue:** What is a Processor?

**Explanation:** A processor is a web script, hosted on a web server that acts as an intermediary by resolving the final destinations of URLs for multimedia items hosted on a Navi-X playlist.

Here is the explanation from the developer of the Navi-X API (NIPL) himself, Turner3D:

The purpose of the processor is to function as an online plugin for Navi-X which produces media playback parameters for a single item, normally starting with only the URL of the web page which contains the item. In other words, if a web page has a flash player embedded in it, the processor teaches Navi-X how to emulate that site's flash player to get the media in the page to play in XBMC.

In order to create a processor, you will need three main skills.
•The ability to manually figure out final media URLs and other parameters by hand from the site you're trying to create a processor for
•Writing and understanding regular expressions
•Programming in a “web language” - PHP, Perl, ASP, etc (Not necessary for most processors)

Please note that this is not meant to serve as a tutorial for any of the above skills. If it were, it would be WAY too big, not to mention that it would take WAY too long to write. :)

> A processor is nothing more than a plain text set of instructions in the form of “Navi-X Instructional Processor Language”, also known as “NIPL script” (pronounced “nipple”, of course). This can normally be stored as a plain text file unless there is processing that needs to be done which is beyond the scope of NIPL.

NIPL came into existence with Navi-X [r3](https://code.google.com/p/navi-x/source/detail?r=3).1 and is a major improvement in both speed and flexibility over the previous processing system. While the previous system is still supported and its documentation is still online, authoring new processors in NIPL is highly recommended.

If you would like NIPL API documentation, you can go here for more details: http://www.navixtreme.com/proc_docs/

