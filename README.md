# Foosball world ranking based on ITSF tournament results
This is an attempt to build an world ranking based on scraped tournament results from https://www.tablesoccer.org/.

There has been some recent criticism on the official [ITSF world ranking](https://www.tablesoccer.org/page/rankings) on the aspect that it would be measuring frequency of participation in ITSF more than the results that players obtain within those tournaments.

Our attempt at building a world ranking aims to counteract this by:
- Using all the tournament data from 2004 to mid 2023 into a single ranking. A drawback of this is of course that we do not account for a player's improvement in skill level over time. But the benefit is that there is substantially more match data available to estimate the skill level of a player.
- We use the [Bradley-Terry model](https://en.wikipedia.org/wiki/Bradley%E2%80%93Terry_model) to estimate the skill level / ability of players based on tournaments results of both singles and doubles tournaments. This is a well-known mathematical model aimed at learning player's skill levels that enable the estimation of accurate win probabilities of the foosball match data that we feed it. The well-known [ELO rating](https://en.wikipedia.org/wiki/Elo_rating_system) used in chess is an example of a Bradley-Terry model too. ELO, unlike our Bradley-Terry model, does not handle doubles matches.


## Limitations
- Limited ability to assess the relative strength between the men and the women in the ranking. This is because matches across genders mostly occurr in mixed doubles, and singles matches between players of different gender are very rare. We nonetheless present a mixed gender world ranking, with the known limitation that we do not really know how to position the men and the women in this ranking relative to each other.
- Does not account for table type. All players are ranked in a single ranking, regardless of table type.
- Limited results for US players. The ranking only contains ITSF tournaments and no IFP tournaments. Because many US-based players mostly (or even only) play IFP tournaments, this results in limited visibility into the ability of many US-based players. I would love to extend this to additionally include IFP one day, if I have time.

## Top 50

|   rank | player                          |
|-------:|:--------------------------------|
|      1 | Frédéric COLLIGNON (BEL)        |
|      2 | Tony SPREDEMAN (USA)            |
|      3 | Kevin HUNDSTORFER (AUT)         |
|      4 | Ekaterina ATANASOVA (BGR)       |
|      5 | Stefan BURMETLER (AUT)          |
|      6 | Marina TABAKOVIC (AUT)          |
|      7 | Cinderella POIDEVIN (FRA)       |
|      8 | Cindy KUBIATOWICZ (CHE)         |
|      9 | Miguel DOS SANTOS LOTE (FRA)    |
|     10 | Amalie BREMER (DNK)             |
|     11 | Ryan MOORE (USA)                |
|     12 | Stanislav GEORGIEV (BGR)        |
|     13 | Hannes WALLIMANN (CHE)          |
|     14 | Ulrich STOEPEL (DEU)            |
|     15 | Andrés LOZANO (PER)             |
|     16 | Verena ROHRER (AUT)             |
|     17 | Sven WONSYLD (DNK)              |
|     18 | Martin DOUSA (CZE)              |
|     19 | Tokuya KOJIMA (JPN)             |
|     20 | Estelle JACQUOT (FRA)           |
|     21 | Géza KISS (HUN)                 |
|     22 | Ladislav KREPELA (CZE)          |
|     23 | Yannick CORREIA (PRT)           |
|     24 | Sárka HOLOMOUCKÁ (CZE)          |
|     25 | Hervé DOS SANTOS LOTE (FRA)     |
|     26 | Alexander MARKIN (ROC)          |
|     27 | Daniel BURMETLER (AUT)          |
|     28 | Benjamin WILLFORT (AUT)         |
|     29 | Giuliano BENTIVOGLIO (BEL)      |
|     30 | Laurent PAQUIN-MARCOTTE (CAN)   |
|     31 | Erik BRUSTEINS (DEU)            |
|     32 | Blagovesta HOFFMANN (BGR)       |
|     33 | Arturo CARLETTA (BEL)           |
|     34 | Thomas HAAS (DEU)               |
|     35 | Robert ATHA (GBR)               |
|     36 | Gábor ROZSOS (HUN)              |
|     37 | David DETRE (HUN)               |
|     38 | Jamal ALLALOU (DEU)             |
|     39 | Sébastien MECKES (FRA)          |
|     40 | Agata CWIAKALA (POL)            |
|     41 | Šimon VÁROŠ (SVK)               |
|     42 | Tiffany MOORE (USA)             |
|     43 | Ecaterina SARBULESCU (ROU)      |
|     44 | Christophe ARCELIN (FRA)        |
|     45 | Adel YOUSFI (FRA)               |
|     46 | Benjamin STRUTH (DEU)           |
|     47 | Jorge CHAVEZ AEDO (PER)         |
|     48 | Olivier COVOS (FRA)             |
|     49 | Adam TOURMENTE (FRA)            |
|     50 | Cihan AN (TUR)                  |
