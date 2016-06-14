Axel's Zits RSS Generator
=========================

This is a Perl written replacement for the
[no more comics containing RSS feed](http://zitscomics.com/feed/) of
the daily webcomic [Zits](http://zitscomics.com/).

Their RSS feed no more contains comics since 19th of February 2015.

Usage
-----

By default it generates an RSS feed for the past 7 days and fetches
all according pages from the website to find the right image URL.

### Plugin for Liferea and Snownews

The script can be used as command-type source in
[Liferea](http://liferea.sf.net/), as
['Execurl'](http://snownews.kcore.de/snowscripts/) type plugin in
[Snownews](http://snownews.kcore.de/), or in any other RSS feed reader
with the capability to call an feed-generating program instead of an
URL.

Actually it was written for exactly that purpose. I use it with Liferea.

Options
-------

* `-n`: Don't download anything from the Sinfest website, just generate
  a feed with dummy titles.
  
* `-d <number>`: Generate a feed for the past _<number>_ days.

  Setting this value high enough for one run may give you all feed
  entries you missed since 19th of February 2015.

  But remember to do this only once as it fetches every page for every
  day since then per run to get the comic title for that day. You may
  get banned if you do that too often.

Requirements
------------

Besides modules from the Perl core distribution, the following Perl
module are required. They can be found on e.g.
[CPAN](https://metacpan.org/) or as packages in e.g.
[Debian](https://www.debian.org/).

* [POSIX::strftime::Compiler](https://metacpan.org/release/POSIX-strftime-Compiler)
* [Date::Calc](https://metacpan.org/release/Date-Calc)
* [LWP::UserAgent](https://metacpan.org/pod/LWP::UserAgent) from the
  [libwww-perl](https://metacpan.org/release/libwww-perl) distribution

License
-------

Copyright (C) 2016 Axel Beckert

Licensed under the _DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE_. See
the file [LICENSE](LICENSE) or http://www.wtfpl.net/txt/copying/ for the full
license text.

Ideas
-----

* It maybe a nice feature to also support a CGI mode. If so, it should
  be possible to run it without CGI.pm installed.

History
-------

Based on my
[Sinfest RSS Generator](https://github.com/xtaran/sinfest-gen-rss).
