# Downloading from online-jazz-archive
1. Go to jazz-on-line.com/artists, choose an artist and copy artist's name from the URL
1. Paste the name into `jazz-on-line-scraper/index.js`
1. Run `node jazz-on-line-scraper/index.js` (creates list of URLs with the artist's songs)
1. Run `./downloader.sh jazz-on-line-scraper/list-name` (replace `list-name` with actual list). This downloads the mp3 files where found
1. Create master directory for all songs of the artist
1. Run `./sorter.sh masterdir` and all downloaded mp3 files will be organised in subdirectories of `masterdir`

# Organising with Google Music
1. Like songs that you're interested in
1. Go the the 'Thumbs-up' playlist and use [this script](https://gist.githubusercontent.com/jmiserez/c9a9a0f41e867e5ebb75/raw/2195aa4ec75c12fb1539ec727faa555643107ec5/export_google_music.js) in developer console to get a list of the songs
1. Save the list of songs and regexp away everything except the songs' names (careful with Roy Eldridge's songs from archive.org!)
1. Run `tagger.sh` to tag all the songs from the list as, let's say, Lindy songs
1. Open Mixxx and the tag should appear! If not, select songs and click right > Metadata > Import from file tags

# Using Mixxx
## BPM Analysis
Go to `Analyze` tab, select songs and start analysis (adds BPM info)

## DJ-ing
1. Start Mixxx
1. Ensure HW is channelled properly (Options > Preferences). Generally, use laptop's jack for headphones and external sound card (usb) for speakers
1. Ensure equaliser is set all the way to the left
1. Ensure fading time is set to 0 seconds (or less)
1. Check that Auto DJ contains enough songs (if not, can import entire playlist to Auto DJ)