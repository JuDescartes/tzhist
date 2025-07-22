readme.md	

created 5-sep-2018

last update 22-jul-25

## About tzhist repository

The public TZ data system maintains time zones only for areas
after 1 January 1970.

If the time zone history of two reagions differs before 1970, they
are represented in TZ by a single zone file.

Only for the cities which are the basis of a zone file name the history
goes further back.

This situation is not satisfying for the needs of astrology, which
need correct timezone information also before 1970, for all places on Earth.

Astrological software companies like Astro Computing Services, San Diego
and Astrodienst AG in Zollikon/Zürich Switzerland have since a long time
created and maintained private databases with extended timezone history data.

Numerous researchers have researched the time zone history of many countries
and published their work.


### The current and historical information on time zones and daylight saving times comes from
- the public domain database TZ, see <a href="https://en.wikipedia.org/wiki/Tz_database" target="new">Wikipedia TZ Database</a>, especially for data from 1970 onwards.
- the public <a href="https://lists.iana.org/hyperkitty/list/tz@iana.org/latest" target="new">TZ Mailing List Archive</a>, going back to 1986.
- reference books by American astrologer Doris Chase Doane
  - *Time Changes in the U.S.A* (1966, revised 1980),
  - *Time Changes in Canada and Mexico* (1968, revised 1986), 
  - *Time Changes in the World* (1971, revised 1982).
- books by Thomas Shanks published by Astro Communications Inc., an important source for the irregular use of daylight saving time in various Canadian and US states before its national standardization.
  - *The American Atlas*, 5th edition (1999),
  - *The International Atlas*, 6th edition (2006),

- *Traité de l'heure dans le monde*, by Gabriel (1990),
- *Régimes Horaires pour l'Europe et l'Afrique*, by Henri Le Corré (1982), 
- *L'astrologie confrontée aux régimes des zones occupied en France de 1914 à 1945*, Guy Mayeres (2006),
- *Новый справочник астролога. Координаты городов и временные поправки (A new astrologer's reference*
*book. Coordinates of cities and time corrections)*, Zaitsev A., Kutalev D. (2015),
- and other books or data inside books.
- Research and data collection by Alois Treindl since the founding of Astrodienst in 1980, some of which have also been included in the public TZ database. The most important primary sources for research are newspaper archives, old airport data, and train timetables.

### How to use
- You should download the latest TZ code and data release from https://www.iana.org/time-zones 
and unpack it into a directory, for example /home/tz.

- Download the files with suffix .txt and the shell script mk_zones.public into the same directory.

- Make sure to have write permission in directory /usr/share/zoneinfo and all its content.

- run the command: ./mk_zones.public
It will compile all the TZ source files and the extra tzhist files and install the binary files.
