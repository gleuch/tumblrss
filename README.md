 _                   _     _              
| |_ _   _ _ __ ___ | |__ | |_ __ ___ ___ 
| __| | | | '_ ` _ \| '_ \| | '__/ __/ __|
| |_| |_| | | | | | | |_) | | |  \__ \__ \
 \__|\__,_|_| |_| |_|_.__/|_|_|  |___/___/
                                          

##################################################################

Feed feeds into Tumblr.


A simple PHP script to port your feeds into Tumblr, with the 
ability to create filters for custom feed items (by source).


Written by Greg Leuch <http://www.halvfet.com>.

##################################################################


UPCOMING FEATURES/FIXES

  - Adding RSS support
  - Adding in more Tumblr post types
  - Adding in filtering by element's attribute values


##################################################################


INSTALLATION

1. Download script.
2. Rename config.inc.php.blank to config.inc.php.
3. Enter in your Tumblr username and password into config.inc.php.
4. Add the feed(s) to be read.
5. Create a CRON job to execute script, and vola!


##################################################################


CUSTOMIZATION

Currently, tumblrss supports filtering for photos. Specify the key
of the filter as the domain name (i.e. google.com), enter in the
type ('photo'), and the filtering paths for the photo (required)
and link (optional).

Filtering is done by matching the element order in which to seek.
The formatting is tag_name[attribute](integer). Attributes can 
only be specified as the last child element. If no attribute is
specified, it will return the contents of the child element.

For instance, the photo source in this code:

<p>
 <a href="http://www.google.com">
  <img src="http://www.google.com/favicon.png" />
 </a>
</p>

would be found by:

p(0),a(0),img[src](0)



##################################################################

Tumblrss makes use of the Tumblr API <http://www.tumblr.com/api>.


Copyfree, suckers!
