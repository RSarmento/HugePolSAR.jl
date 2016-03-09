# HugePolSAR.jl

This repository describes a reproducible research script which is an experiment envolving effortless huge imagery processing in the cloud.

## Requeriments

* GNU/Linux (preferably Debian-based distribution)
* [Julia v0.4.3](http://julialang.org/downloads/)
* Julia dependencies: [Images.jl](https://github.com/timholy/Images.jl), [StatsBase.jl](https://github.com/JuliaStats/StatsBase.jl)
* git
* wget
* 56GB+ of Memory RAM

## Usage

1. You need to clone [PolSAR.jl](https://github.com/gsd-ufal/PolSAR.jl.git) and enter to directory:

```
git clone Pkg.clone("https://github.com/gsd-ufal/PolSAR.jl.git") && cd PolSAR.jl/src
```

2. Download experiment script on same folder PolSAR.jl/src:

```
wget url
```

3. Image files download

The images can be downloaded in the following links:

[ASF - Alaska Satellite Facility](https://vertex.daac.asf.alaska.edu/#)

[UAVSAR - Uninhabited Aerial Vehicle Synthetic Aperture Radar](http://uavsar.jpl.nasa.gov/cgi-bin/download.pl)

The following example uses the following image files:

```
ChiVol_29304_14054_007_140429_L090HH_CX_01.slc
ChiVol_29304_14054_007_140429_L090VH_CX_01.slc
ChiVol_29304_14054_007_140429_L090VV_CX_01.slc
```
 
located in the same folder as the code files, but different images with different locations are possible by specifying the location and/or name in `ZoomScript.jl`.

Saving them  on the same folder PolSAR.jl/src. 

4. Finally, still in the same folder:

```
julia HugePolSAR.jl
```

The experiment may take several hours.

Data and images will be generated in the following directories:

```
tests/scenario1
tests/scenario2
tests/imgs
```
