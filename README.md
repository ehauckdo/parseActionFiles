### Parsing GVG-AI Action Files 

Python script to parse a list of action files from the [GVG-AI framework](http://www.gvgai.net)  and print a table with results.

### Requirements
* [numpy](http://www.numpy.org/)
* [PrettyTable](https://pypi.python.org/pypi/PrettyTable)

### How to use

```./parseActionFiles [options] inputFolders```

Options:

-m MultiplayerLogs: parse multiplayer execution logs

-i IgnoreDisqualified: victory percentages and score won't be affected by runs in which the controller was disqualified

-c Compare: print a unique table comparing percentage of wins and average score for all controllers found

### Filename Format

For single player games:

```Controller_Game_AnyOtherInfo```

e.g. sampleMCTS_zelda_Run2_lvl3.log

For multiplayer games:

```Controller1_Controller2_Game_AnyOtherInfo```

e.g. sampleMCTS_sampleRandom_zelda_Run2_lvl3.log

### Sample Result

```
user@host:~$ ./parseActionFiles sampleActionFiles
MCTS
+----------------+------------+------------------+----------+----------+--------------+
|      Name      | Victories% |     AvgScore     | MinScore | MaxScore | Disqualified |
+----------------+------------+------------------+----------+----------+--------------+
|     aliens     |    100     |  68.60 ± 15.08   |   40.0   |   81.0   |      0       |
|  boulderdash   |     20     |   12.00 ± 5.93   |   3.0    |   18.0   |      0       |
|  butterflies   |    100     |  28.00 ± 13.91   |   14.0   |   52.0   |      0       |
|     chase      |     0      | -196.00 ± 402.00 | -1000.0  |   8.0    |      1       |
|     frogs      |     40     |   0.40 ± 0.49    |   0.0    |   1.0    |      0       |
| missilecommand |     40     |   3.60 ± 3.67    |   -1.0   |   9.0    |      0       |
|    portals     |     20     |   0.20 ± 0.40    |   0.0    |   1.0    |      0       |
|    sokoban     |     40     |   1.60 ± 1.02    |   0.0    |   3.0    |      0       |
| survivezombies |     0      |   -1.00 ± 0.00   |   -1.0   |   -1.0   |      0       |
|     zelda      |     0      | -397.40 ± 492.02 | -1000.0  |   5.0    |      2       |
+----------------+------------+------------------+----------+----------+--------------+
user@host:~$ ./parseActionFiles sampleActionFiles -mc sampleActionFilesMultiplayer
+----------------+----------------------------+----------------------------+
|      Name      |         sampleMCTS         |        sampleRandom        |
+----------------+----------------------------+----------------------------+
|   asteroids    |  100%     (14.00 ± 8.07)   |    0%     (0.80 ± 2.86)    |
|      tron      |  100%     (1.00 ± 0.00)    |    0%     (0.00 ± 0.00)    |
|  steeplechase  |    0%   (200.00 ± 600.00)  |   10%   (100.10 ± 300.30)  |
|     gotcha     |   50%   (459.50 ± 681.03)  |   50%   (409.90 ± 676.16)  |
|   samaritan    |   60%   (-99.40 ± 300.20)  |   30%     (0.30 ± 0.46)    |
| competesokoban |    0%     (1.10 ± 1.51)    |    0%     (0.10 ± 0.30)    |
|      klax      |  100%     (13.50 ± 9.27)   |    0%     (0.00 ± 0.00)    |
|  copsNrobbers  |   60%     (3.60 ± 1.50)    |    0%     (0.50 ± 0.81)    |
|    akkaarrh    |    0%     (8.30 ± 15.13)   |    0%     (1.30 ± 4.29)    |
|  captureflag   |  100%     (8.50 ± 5.94)    |    0%     (-4.30 ± 3.13)   |
+----------------+----------------------------+----------------------------+
       
```
