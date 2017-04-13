### Parsing GVG-AI Action Files 

Python script to parse a list of action files from the [GVG-AI framework](http://www.gvgai.net)  and print a table with results.

### How to use

```./parseActionFiles sampleActionFiles```

Simple run the script and pass the directory with action files. The directory must be in the same folder as of the script.

### Sample Result

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
