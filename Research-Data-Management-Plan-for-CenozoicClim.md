# Research Data Management Plan for project: "Mechanisms of major climate system reorganisations in the Cenozoic"

## Summary statement

In this project a lot of effort is put in making the initial files for the coupled model CESM and ocean only model POP. Normally these models are defined on a domain that represents a present day topography but for this project we need a Pliocene, Miocene and Eocene topography. Especially CESM requires dozens of initial files. 
IMAU developed a procedure for creating these files that makes use of several scripts (fortran, shell, IDL etc). these scripts will all be stored and documented on github in the repository [CenozoicClim github page](https://github.com/IMAU-oceans/CenozoicClim). 

The created initial data itself consists mostly of netcdf files that are too big to store on github and will be stored on [YODA](https://yoda.uu.nl/yoda-uu-nl/what-is-yoda/index.html) a datamanagement system at Utrecht University. 

The output of the model runs is mostly netcdf data that is in the order of TBs. During (and also a part after) the runs this data will be stored on the scratch filesystem of Cartesius. When the runs are done it will be stored on the archive filesystem of Cartesius, both at [SURFsara](https://www.surf.nl/). 

Each sub-project (e.g. PhD chapter, MSc thesis, Bsc thesis) will require a new repository on the [CenozoicClim github page](https://github.com/IMAU-oceans/CenozoicClim). Initially, this repository will be private, only accessible to Team Members within the CenozoicClim team. 

Most importantly, the project repository will at the end contain the python or jupyter scripts to recreate all the Figures used in the manuscript/chapter/thesis, as well as any information on the data required as input for these scripts. This ensures full reproducibility and transparency of at a minimum the creation of the Figures. 



## Data Storage and Back-up

All of the scripts required to analyse and plot output fields and that is used for papers and theses will need to be version controlled within the appropriate project repository on the [CenozoicClim github account](https://github.com/IMAU-oceans/CenozoicClim).

These scripts almost require an intermediate file as input data. With this we mean for instance one file containing all the yearly means of the field Sea Surface Temperature instead of all the outputfiles together also containing all the other variables. The researchers will store these intermediate inputfiles on YODA with help of this [tutorial](https://github.com/IMAU-oceans/data_management/blob/master/yoda.md) 

Each CenozoicClimate python script and jupyter notebook should clearly state the source of these NetCDF files (ideally as a DOI if known, or otherwise as a web archive). Even if the data is already stored locally, it is still better to give, as a comment, the original source of the NetCDF files.


## Data Access and Security

Every team member will have access to the output of the model runs at supercomputer SURFsara and also to all the private repositories on the CenozoicClimate github account with the goal to facilitate sharing of code between team members. Anna von der Heydt has responsibility for granting and revoking of team member status.


## Data Preservation and Archiving

Once a manuscript or thesis is published, the goal is for the repository associated with that paper to be made public. This is good practice in Open Science, and only in specific cases and with good reason can this be changed. Each repository containing code (scripts and notebooks) will then also be archived on [zenodo](zenodo.org), so that it obtains a permanent DOI.

## Data Sharing and Reuse

Since the scripts used to generate all the Figures and other analysis of each published paper/thesis in principle is open to the public, data sharing is a matter of pointing interested parties to the appropriate github or zenodo page.

All code will in principle fall under the same MIT license as the Parcels license (see https://github.com/OceanParcels/parcels/blob/master/LICENSE.md). Exceptions to this rule can be made (and should be made when external code is sued that is published under a different license), in discussion with the project leader.


