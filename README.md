# stemgraphic


# Overview

John Tukey’s stem-and-leaf plot first appeared in 1970. Although very useful back then, it cannot handle 
more than 300 data points and is completely text-based. Stemgraphic is a very easy to use python package 
providing a solution to these limitations.

A typical stem_graphic output:

  [stem_graphic example](https://github.com/fdion/stemgraphic/raw/master/png/test_rosetta.png)

For an in depth look at the algorithms and the design of stemgraphic, see

  [Stemgraphic: A Stem-and-Leaf Plot for the Age of Big Data](https://github.com/fdion/stemgraphic/raw/master/doc/stemgraphic%20A%20Stem-and-Leaf%20Plot%20for%20the%20Age%20of%20Big%20Data.pdf)

Documentation is available as pdf [stemgraphic.pdf](http://stemgraphic.org/doc/stemgraphic.pdf)
and [online](http://stemgraphic.org/doc/) html.

The official website of stemgraphic is: http://stemgraphic.org



# Installation

Stemgraphic requires docopt, matplotlib and pandas. Optionally, having Scipy installed will give you secondary plots 
and Dask (see requirements_dev.txt for all needed to run all the functional tests) will allow for out of core, big data
visualization.

Installation is simple:

    pip3 install -U stemgraphic  

or from this cloned repository, in the package root:

    python3 setup.py install


# Latest changes

## Version 0.5.0

Major new release.

- All 0.4.0 private changes were merged
- new module stemgraphic.alpha:
  - n-gram support
  - stem_graphic supporting categorical
  - stem_graphic supporting text
  - stem_text supporting categorical
  - stem_text supporting text
  - stem command line supporting categorical when column specified
  - heatmap for n-grams
  - heatmap grid to compare multiple text sources
  - Frobenius norm on diff matrices
  - radar plot with Levenshtein distance
  - frequency plot (bar, barh, hist, area, pie)
  - sunburst char
  - interactive charts with cufflinks
- new module stemgraphic.num to match .alpha
- stop word dictionaries for English, Spanish and French
- Massively improved documentation of modules and functions
- Improved HTML documentation
- Improved PDF documentation

## Version 0.4.0

Internal release for customer.

- Added Heatmap

- Basic PDF documentation

- Quickstart notebook

## Version 0.3.7

Matploblib 2.0 compatibility

## Version 0.3.6

- Persist sample from command line tool (-k filename.pkl or -k filename.csv).

- Windows compatible bat file wrapper (stem.bat).

- Added full command line access to dask distributed server (-d, -s, use file in '' when using glob / wildcard).

- For operations with dask, performance has been increased by 25% in this latest release, by doing a compute
once of min, max and count all at once. Count replaces len(x).


Added the companion PDF as it will be presented at PyData Carolinas 2016.


# TODO

Plenty... but to start:

- back to back and scale calculation
- multivariate support
- provide support for secondary plots with dask
- automatic dense layout
- add a way to provide an alternate function to the sampling
- support for spark rdds and/or sparkling pandas
- create a bokeh version. Ideally rbokeh too.
- interactive version based on the above
- add unit tests
- add feather, hdf5 etc support, particularly on sample persistence
