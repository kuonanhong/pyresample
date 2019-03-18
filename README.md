[![Build Status](https://travis-ci.org/pytroll/pyresample.svg?branch=master)](https://travis-ci.org/pytroll/pyresample)
[![Build status](https://ci.appveyor.com/api/projects/status/a34o4utf8dqjsob1/branch/master?svg=true)](https://ci.appveyor.com/project/pytroll/pyresample/branch/master)
[![codebeat badge](https://codebeat.co/badges/2b9f14bc-758c-4fe1-967d-85b11e934983)](https://codebeat.co/projects/github-com-pytroll-pyresample-master)

Pyresample
----------

Pyresample is a python package for resampling geospatial image data. It is the
primary method for resampling in the [SatPy](https://github.com/pytroll/satpy)
library, but can also be used as a standalone library. Resampling or
reprojection is the process of mapping input geolocated data points to a
new target geographic projection and area.

Pyresample can operate on both fixed grids of data and geolocated swath data.
To describe these data Pyresample use various "geometry" objects include the
`AreaDefinition` and `SwathDefinition` classes.

Pyresample offers multiple resampling algorithms including:

- Nearest Neighbor
- Elliptical Weighted Average (EWA)
- Bilinear

For nearest neighbor and bilinear interpolation pyresample uses a kd-tree
approach by using the fast KDTree implementation provided by the 
[pykdtree](https://github.com/storpipfugl/pykdtree) library.
Pyresample works with numpy arrays and numpy masked arrays. Interfaces to
XArray objects (including dask array support) are provided in separate
Resampler class interfaces and are in active development.
Utility functions are available to easily plot data using Cartopy.

Pyresample is tested with Python 2.7 and 3.6, but should additionally work
on Python 3.4+. Pyresample will drop Python 2.7 at the end of 2019.

[Documentation](https://pyresample.readthedocs.org/en/latest/)
Look at [pytroll.github.io](http://pytroll.github.io/) for more information.
