# rssread
Python program to read and parse RSS feeds from command line (CLI).

# CLI

```
rssread.py --help
usage: rssread.py [-h] [-d] [-v] -f FEED [FEED ...] [-o] [-t] [-y] [-n NUMBER]

This program reads news from an RSS feed.

optional arguments:
  -h, --help            show this help message and exit
  -d, --debug           Print debug information
  -v, --verbose         Print verbose output
  -f FEED [FEED ...], --feed FEED [FEED ...]
                        Specify RSS feed URL. E.g. --feed https://hnrss.org/frontpage
  -o, --tor             Use Tor, go through Tor Socks5 proxy
  -t, --today           Get today's entries from RSS feed
  -y, --yesterday       Get yesterday's entries from RSS feed
  -n NUMBER, --number NUMBER
                        Number of last entries to get from from RSS feed. Default is 3.

```

# Examples

```
# get the post from today
rssread.py --feed "https://hnrss.org/frontpage" --today
# get the post from yesterday
rssread.py --feed "https://hnrss.org/frontpage" --yesterday
# get last 3 posts
rssread.py -feed "https://hnrss.org/frontpage" --number 3
# get multiple feeds example: 
rssread.py -feed https://feed1.io https://feed2.com --today -n 10
```
