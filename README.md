# Bischoff and Ratcliff's Instance Sets

This repository contains the instances of the paper of Bischoff and Ratcliff 1995 (see the reference section).

## Source of the Data

The data has not been generated, it was downloaded from the page of Professor J. E. Beasley (see the reference section).

## Description of the Original Data

There are 10 data files: `set_1.txt, ..., set_10.txt`. The procedure used to create these test problems is presented in the paper.

These problems are Single Knapsack Problems (according to the typology of G. Wäscher, Heike Haußner, H. Schumann), the objective being to maximise the volume of the container used.

Each data file contains `P` test problems, being `P` specified as the first number in the file. For each problem `p (p=1,...,P)` the data has the format shown in the following example:

Example:

```plain
 60 2508405    # the problem number p, seed number used in the paper
 587 233 220   # container length, width, height
 10            # number of box types n
 1  78 1 72 1 58 1 14
 2  107 1 57 1 57 1 11      # where there is one line for each box type
 3 ...
 etc for n lines
```

The line for each box type contains 8 numbers:

1. box type `i`
2. box length,
3. 0/1 indicator
4. box width
5. 0/1 indicator
6. box height
7. 0/1 indicator
8. number of boxes of type `i`

After each box dimension, the 0/1 indicates whether placement in the vertical orientation is permissible (=1) or not (=0).

## Input File Format

The [Input File Format](https://github.com/lucasguesserts/packing-visualizer/blob/3d1e9ec4fb880e3e90978562218c40c4bd7c6f49/src/file_format/input/0_0_0.json) is specified using [json-schema](https://json-schema.org/). All its versions can be found in the [packing-visualizer repository](https://github.com/lucasguesserts/packing-visualizer).

The original data has been converted to such format. Each instance must be specified in its own file, so the instances of each set are in its own directory. Besides, there is a file containing the data of all instances (so one can load a single file instead of many ones).

[This is the directory with the data](./data) and [this is the single file version](./data/data.json).

## Tools

There are tools used to convert the files from their original format to the Input File Format. They can be found in the [tool directory](./tools).

## References

1. [Page of Professor J. E. Beasley with the data and description of the instances](http://people.brunel.ac.uk/~mastjjb/jeb/orlib/thpackinfo.html)
2. [Bischoff, Eberhard E. and M. S. W. Ratcliff. “Issues in the development of approaches to container loading.” Omega-international Journal of Management Science 23 (1995): 377-390.](https://doi.org/10.1016/0305-0483%2895%2900015-G).
    ```bibtex
    @article{bib:bischoff-and-ratcliff-1995,
        title   = {Issues in the development of approaches to container loading},
        author  = {Eberhard E. Bischoff and M. S. W. Ratcliff},
        journal = {Omega-international Journal of Management Science},
        year    = {1995},
        volume  = {23},
        pages   = {377-390}
    }
    ```
3. [Wäscher, Gerhard et al. “An improved typology of cutting and packing problems.” Eur. J. Oper. Res. 183 (2007): 1109-1130.](https://doi.org/10.1016/j.ejor.2005.12.047)
    ```bibtex
    @article{bib:wascher-and-haussner-and-schumann-2007,
        title   = {An improved typology of cutting and packing problems},
        author  = {Gerhard W{\"a}scher and Heike Hau{\ss}ner and Holger Schumann},
        journal = {Eur. J. Oper. Res.},
        year    = {2007},
        volume  = {183},
        pages   = {1109-1130}
    }
    ```