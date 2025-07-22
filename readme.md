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

### tzhist mailign list and discussion group
There is an associated discussion group for timezone history work.

https://groups.google.com/g/tzdata-history

Anyone can join this Google group.


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

### What is missing
Boundary definitions for all the zones are missing. While they exist to some extent for the official TZ zones,
no boundary lines have yet been defined for the non-official zones from the tzhist files.

Alternatively, instead of boundary lines you could use lists of place names with coordinates and the zone name
to be used with each place. Again, such lists exist in the Geonames project, but only with references to the official TZ
zones, not to the extra zones defined in the tzhist files.

Astrodienst has also defined a system of 'Astrodienst Zone Numbers' (AZN) with a distinct number for each zone.
That simplifies the maintenance of such places lists, because official zone names sometimes change.

### Where tzhist is incomplete
Canadian states: NS Nova Scotia(25), ON Ontario(100), PE Prince Edward Island(3), QU Quebec(60), SK Saskatchewan(40).

US states: AK(8), AL(7), AZ(3), CO(3), CT(5), DC(1), DE(20), GA(20), IA(25), ID(20), IL(110), IN(300),
KS(5), KY(70), LA(2), MD(30), ME(50), MI(100), MO(5), MO(40), MS(2), MT(10), NC(5), ND(10), NE(5),
NH(15), NJ(15), NM(2), NY(200), OH(100), OK(3), OR(15), PA(120), RI(1), SC(1), SD(3), TN(70), UT(2),
VA(25), VT(50), WA(50), WI(5), WV (1)(30), WY (1).

The number in (parenthesis) indicates how many zones are approximately required for each state.
The numbers are so high, because until the Uniform Timezone Act of 1967, in many states towns or counties could
decide on the local level whether to follow daylight saving time in a particular year.
