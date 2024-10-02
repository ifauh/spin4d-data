# SPIn4D Data Release 1 Exploration

This notebook is provided to familiarize the user with data artifacts produced by the *Critical Early DKIST Science: Spectropolarimetric Inversion in Four Dimensions with Deep Learning (SPIN4D)* project (funded by NSF#2008344).

This notebook contains a series of sections covering:

1.    **Running the Notebook**
1.    **Project Overview**
1.    **Data Description**
1.    **Data Access**
1.    **Data Exploration**
    1. MURaM cubes
    1. Stokes profiles
1.    **Data Visualization**
    1. MURaM cubes
    1. Stokes profiles

# Running the Notebook

This notebook has the following dependencies:
-    os   (operating system functions)
-    numpy (numerical python library)
-    h5py (H5Py file format)
-    matplotlib (standard Python plotting library)

Of course, there is a dependency on the **SPIn4D-DR1** data. This notebook uses a 33GB sample of the 13TB [SPIN4D-DR1 dataset](http://dtn-itc.ifa.hawaii.edu/spin4d/DR1/).

# Project Overview

The SPIn4D project was performed by a group of researchers at the Institute for Astronomy, University of Hawai‘i, Manoa; National Solar Observatory; High Altitude Observatory, NSF National Center for Atmospheric Research led by PI Xudong Sun.
Simulations of the small-scale dynamo actions that are prevalent in quiet-Sun and plage regions were performed at the NCAR-Wyoming Supercomputing Center (NWSC) using Matthias Rempel's 2014 version of the Max-Planck University-of-Chicago Radiative MHD code (MURaM). For a complete description of the simulation and data read the [paper](https://arxiv.org/pdf/2407.20309).

## Project members
-    Institute for Astronomy, University of Hawai‘i at Manoa
    - KAI E. YANG (杨凯)
    - S. CURT DODDS
    - IAN CUNNYNGHAM
    - JIAYI LIU (刘嘉奕)
    - XUDONG SUN (孙旭东) (PI)
-    High Altitude Observatory, NSF National Center for Atmospheric Research
    -    MATTHIAS REMPEL
-    National Solar Observatory
    -    LUCAS A. TARR
    -    SARAH A. JAEGGLI
    -    THOMAS A. SCHAD
-    Department of Information and Computer Sciences, University of Hawai‘i at Manoa
    -    PETER SADOWSKI
    -    YANNIK GLASER


## Simulation Cases
Six simulation cases with different mean magnetic fields were conducted. Each case covers six solar-hours with output snapshots stored at a 40s cadence. A detailed description of each case is given in the **Data Description** below.

##  Spatial Dimension
The volume and spatial resolution of the first 5 cases are **25x25x8Mm** with **16x16x12km** spatial resolution, extending from the upper convection zone up to the temperature minimum region. The volume of the sixth case (SPIN4D_SSD_Large) is **50x50x8Mm** with the same **16x16x12km** spatial resolution.

## Stokes Profiles
For each case we synthesized Stokes profiles for two sets of Fe I lines at 630 and 1565 nm for snapshots at 12 minute intervals with two opposite magnetic field orientations (due to the inherent LOS ambiguity). The Stokes profile files were created using our modification of Andrés Asensio Ramos' [3d_sir code](https://github.com/aasensio/3d_sir) that is available on Github [here](https://github.com/ifauh/par-sir).
