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
       
```
