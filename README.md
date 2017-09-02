### Parsing GVG-AI Action Files 

Python script to parse a list of action files from the [GVG-AI framework](http://www.gvgai.net)  and print a table with results.

### Requirements
* [numpy](http://www.numpy.org/)
* [PrettyTable](https://pypi.python.org/pypi/PrettyTable)

### How to use

```./parseActionFiles [-m] sampleActionFiles```

Simple run the script and pass the directory with action files. The directory must be in the same folder as of the script.

Additionaly, you can use the parameter -m for multiplayer games.

### Filename Format

For single player games:

```Controller_Game_AnyOtherInfo```

e.g. sampleMCTS_zelda_Run2_lvl3.log

For multiplayer games:

```Controller1_Controller2_Game_AnyOtherInfo```

e.g. sampleMCTS_sampleRandom_zelda_Run2_lvl3.log

### Sample Result

(Single player run)

Name|Victories%|AvgScore|MinScore|MaxScore|Disqualified 
---|---|---|---|---|---
aliens        |     98     |56.03 +/- 10.90 |   40.0   |   76.0   |      1       
boulderdash   |     0      | 3.85 +/- 3.61  |   -1.0   |   14.0   |      17     
butterflies   |     80     |31.30 +/- 14.28 |   14.0   |   72.0   |      1       
chase         |     0      | 1.18 +/- 1.72  |   0.0    |   8.0    |      1       
frogs         |     12     | 0.12 +/- 0.33  |   0.0    |   1.0    |      1       
missilecommand|     62     | 4.32 +/- 5.70  |   -3.0   |   16.0   |      2       
portals       |     20     | 0.20 +/- 0.40  |   0.0    |   1.0    |      1       
sokoban       |     5      | 0.29 +/- 0.63  |   0.0    |   2.0    |      45      
survivezombies|     25     | 0.20 +/- 3.12  |   -6.0   |   8.0    |      5       
zelda         |     10     | 3.61 +/- 2.19  |   -1.0   |   8.0    |      1       

(Multi player run)


Name|Victories%_P1|Victories%_P2|AvgScore_P1|AvgScore_P2|MinScore|MaxScore|Disqualified|
---|---|---|---|---|---|---|---
akkaarrh    |       10      |       10      |   9.30 +/- 8.70   |   9.90 +/- 9.68   |   -1.0   |   23.0   |      0       
asteroids   |       50      |       30      |  81.50 +/- 71.83  |  74.10 +/- 67.76  |   -2.0   |  178.0   |      0       
captureflag |       90      |       10      |   10.90 +/- 9.87  |   1.60 +/- 3.14   |   -1.0   |   26.0   |      0       
copsNrobbers|       60      |       0       |   4.20 +/- 1.25   |   0.00 +/- 0.00   |   2.0    |   6.0    |      0       
gotcha      |       0       |      100      | 683.20 +/- 691.81 |   1.00 +/- 0.00   |   12.0   |  1936.0  |      0       
klax        |       20      |       90      |   8.50 +/- 5.64   |  18.10 +/- 13.11  |   1.0    |   20.0   |      0       
samaritan   |      100      |       0       |   1.00 +/- 0.00   |   0.00 +/- 0.00   |   1.0    |   1.0    |      0       
sokoban     |       0       |       0       |   0.07 +/- 0.25   |   0.08 +/- 0.27   |   0.0    |   1.0    |      0       
steeplechase|       0       |       10      | 222.22 +/- 415.74 | 100.10 +/- 300.30 |   0.0    |  1000.0  |      10      
tron        |       50      |       50      |   0.60 +/- 0.49   |   0.50 +/- 0.50   |   0.0    |   1.0    |      0       
