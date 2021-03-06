# gritttt-rss

*Google Reader Inspired Transplants To Tiny, Tiny rss.*

## What is it?

In late 2011 Google »integrated« several of its Reader's features into GooglePlus. Those features became useless after what we feel was an amputation of vital parts. We mainly missed the sharing goodness and as it happened, we were looking for Google alternatives anyway at that time.

For Google Reader we settled with the open-source feed reader [tiny, tiny rss](http://www.tt-rss.org) (which is neither tiny nor tiny, tiny by the way but rather great). Even though it exceeds Google Reader in some aspects, for us it lacks a few neat features, too. The things we miss and are about to (re-)build are:

* Drive-by-Sharing<br/>
  Share any page you see on the fly through a bookmarklet, even though you're not subscribed to the website's feed (it might not even have one).

* Shared-Widget<br/>
  To show the non-tt-rss-using-world what you share with other tt-rss-users, we wish to provide a widget that adds the latest items from tt-rss' public shared feed to your website.

* Import<br/>
  In order to make the move feel like Google Reader never happened, we want to get your historic starred and/or shared items from Google Reader and display them in tt-rss under starred/shared items.


Thus, on a novemberish afternoon in February 2012, Amsterdam public library saw the birth of gritttt-rss:
`Google Reader Inspired Transplants To Tiny, Tiny rss`


## Installation
  
Here we give an overview which directories contain what and a one-sentence summary of what you need to do.
Please find detailled installation instructions in the subdirectories' README:

* Driveby-sharing<br/>
  Create the dedicated feed. Put the directory on your host that also runs tt-rss, adjust some variables in the contained files, and install a bookmarklet in your browser.

* Shared-widget<br/>
  Put the directory on your host that also runs tt-rss, adjust a path in a file and call the widget on a website of yours.

* Import<br/>
  Export data from Google. Create the dedicated feed. Execute the import script and execute the resulting SQL on your tt-rss database.  

Note that drive-by-sharing and the import feature both require a dedicated feed to be added to the tt-rss database, which you can create by executing the SQL in `create-gritttt-feed.sql`. 
