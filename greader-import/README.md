This allows you to import your shared and starred items from your Google Reader account to your tt-rss database.

# Preparation

1. First, make sure you have a backup of your current tt-rss database.
It probably is also a good idea to stop feed updates while you
are doing this. I am not responsible for data loss or corruption.

2. You need to export your shared/starred items from your Google account.
Go to `Google Reader -> settings`, and export the shared/starred items in Google's 
custom json format. Store the export in this directory. The files should be 
called `shared-items.json` or `starred-items.json`.

3. Make sure a dedicted feed exists in your tt-rss. You can insert it via executing 
the SQL in the file `create-tt-unifeed.sql`, which you can find in the 
main directory. Take note of the ID this feed has in the table `ttrss_feeds`
(You'll need that to create imports).

# Importing

1. Execute the `import.py` script (tell it your user Id & the feed ID when
it asks for them). You should now have a file called `tt-import.sql` in this directory.

2. Import the resulting SQL in `tt-import-sql` into your tt-rss database
(via some import functionality, e.g. with myphpadmin).