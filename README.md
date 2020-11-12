# Agee et al. 2020 Supplementary Model Data
This repository contains model parameterization files used to generate results found in the manuscript authored by Agee et al. Contained herein are model input files for six scenarios of three-dimensional root system structure under two soil hydraulic parameterizations (6 x 2 = 12 possible simulations) for a 1 ha site located in northern Lower Michigan. The modified version of [PFLOTRAN](https://pflotran.org) used for simulations can be found archived [here](http://doi.org/10.5281/zenodo.3540881).

## File structure
### PFLOTRAN_Input_Files
Contains parameter files that define PFLOTRAN material properties for each grid cell within the domain (HDF5); climate forcing including potential transpiration and net precipitation (ASCII text files); and PFLOTRAN input files (ASCII text files) which define the domain, soil hydraulic characteristics, and appropriate simulation settings. There are six folders which represent three scenarios of lateral root extent with two major root architectures (tap and lateral/flat). See sample structure below for the localized (Sc1) lateral spread using the lateral/flat root architecture:

* PFLOTRAN_Input_Files
  + SC1_FLAT
    + Climate_Forcing
    + Root_Structure_Files

### Root_Architectures
Contains tar.gz archived files of all root architectures generated for simulations. Architectures were generated using the RootBox model (Leitner et al., 2010) and were exported to CSV using the standard RSWMS format. An example file header is as follows:

Num, X, Y, Z, connected, order, branchnumber, length, surface, mass, age

Variable      | Description
-----------   | -----------
Num           | Root segment number
X             | X coordinate of segment midpoint
Y             | Y coordinate of segment midpoint
Z             | Z coordinate of segment midpoint
connected     | Root segment number this segment is connected to
branchnumber  | Primary branch number this segment belongs to
length        | Length of segment (m)
surface       | Surface area of segment (m^2)
mass          | Mass of segment (not used, set to 0)
age           | Age of segment (not representative of an actual age)



## References
Agee, E., He L., Bisht, G., Couvreur, V., Shahbaz, P., Meunier, F., Gough, C.M., Matheny, A., Bohrer, G., and Ivanov, V.Y. Root lateral interactions drive water uptake patterns under water limitation 

Agee, E. et al. (2019, November 13). laagee/pflotran-dev-root-system: PFLOTRAN-Root v0.0 (Version v0.0). Zenodo. http://doi.org/10.5281/zenodo.3540881

Leitner, D., Klepsch, S., Bodner, G., & Schnepf, A. (2010). A dynamic root system growth model based on L-Systems. Plant and Soil, 332(1–2), 177–192. https://doi.org/10.1007/s11104-010-0284-7




