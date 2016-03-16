# HugePolSAR.jl

## About

This repository provides the support materials for reproducing the research presented in the paper **Effortless huge imagery processing in the Cloud**, authored by André Lage-Freitas, Raphael Pereira Ribeiro, Naelson D. C. Oliveira, Alejandro C. Frery (Senior Member, IEEE), and Rivo Leonardo Alves Sarmento. 

All authors are with the Computing Institute at Federal University of Alagoas (UFAL). Research was developed at the LaCCAN lab and this work was supported by Microsoft Azure for Research, Brazilian National Council for Scientific and Technological Development (CNPq), and Alagoas Research Foundation (FAPEAL).

## Requeriments

* GNU/Linux (preferably Debian-based distribution)
* [Julia v0.4.3](http://julialang.org/downloads/)
* Julia dependencies: [Images.jl](https://github.com/timholy/Images.jl), [StatsBase.jl](https://github.com/JuliaStats/StatsBase.jl)
* git
* wget
* 56GB+ of RAM memory

## Usage

* You need to clone [PolSAR.jl](https://github.com/gsd-ufal/PolSAR.jl.git) and enter to directory:

```
$ git clone Pkg.clone("https://github.com/gsd-ufal/PolSAR.jl.git") && cd PolSAR.jl/src
```

* Download experiment script and put it at the same folder PolSAR.jl/src:

```
$ wget https://raw.githubusercontent.com/gsd-ufal/HugePolSAR.jl/master/src/HugePolSAR.jl
```

* Data set files

Images can be downloaded in the following links:

[ASF - Alaska Satellite Facility](https://vertex.daac.asf.alaska.edu/#)

[UAVSAR - Uninhabited Aerial Vehicle Synthetic Aperture Radar](http://uavsar.jpl.nasa.gov/cgi-bin/download.pl)

The image used in the experimetns refers to the following files which can be downloaded at [this Web link](http://uavsar.jpl.nasa.gov/cgi-bin/product.pl?jobName=ChiVol_29304_14054_007_140429_L090_CX_01):

```
ChiVol_29304_14054_007_140429_L090HH_CX_01.slc
ChiVol_29304_14054_007_140429_L090VH_CX_01.slc
ChiVol_29304_14054_007_140429_L090VV_CX_01.slc
```
 
Save these files at the same folder PolSAR.jl/src. 

* Finally, still in the same folder:

```
$ julia HugePolSAR.jl
```

Execution time depends on the image summary size. For instance, an image summary size whose physical size is more than 2GB might take some minutes.

Data output and summaries in PNG will be generated in the following directories:

```
tests/scenario1
tests/scenario2
tests/imgs
```
