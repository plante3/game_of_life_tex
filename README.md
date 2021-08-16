!!! WARNING BAD CODE !!!
this is the first thing I made in TeX

# Game of Life in TeX
An implementation of the finite state automata *Conway's Game of Life* in the typesetting system TeX.

### Usage:
Download the latest release (`GoL-TeX-V1.22.zip`) and extract the files to a folder. Then run
```
pdftex life.tex
```
Patterns may be input with the `\gameinput` macro taking two arguments. The first is the main input in the [*RLE* format](https://www.conwaylife.com/wiki/Run_Length_Encoded); the second is how many iterations to generate. An optional argument is allowed to control the size of the board (ex. `\gameinput[10,20]{...}{...}` initializes a game with width `10` and height `20`). Attributes such as the name and author are set automatically, if provided by #-lines before the header.

The rule can be set in the header lines using B/S notation and defaults to B3/S23 if not specified.

Sample inputs are given below (as well as being provided with source).
```tex
\gameinput{
    x = 36, y = 9, rule = B3/S23
    24bo11b$22bobo11b$12b2o6b2o12b2o$11bo3bo4b2o12b2o$2o8bo5bo3b2o14b$2o8b
    o3bob2o4bobo11b$10bo5bo7bo11b$11bo3bo20b$12b2o!
}{50}

%% A replicator in the Highlife rule B36/S23.
\gameinput{
    #N Replicator
    #O Nathan Thompson
    #C A replicator for the HighLife rule.
    x = 5, y = 5, rule = B36/S23
    2b3o$bo2bo$o3bo$o2bob$3o!
}{50}
```
Sample `.pdf` and `.log` files are given for reference.

#### How do I view the output?
Press page down repeatedly.
