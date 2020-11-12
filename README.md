# Agee et al. 2020 Supplementary Model Data
This repository contains model parameterization files used to generate results found in the manuscript authored by Agee et al. Contained herein are model input files for six scenarios of three-dimensional root system structure under two soil hydraulic parameterizations (6 x 2 = 12 possible simulations) for a 1 ha site located in northern Lower Michigan (Figure). The modified version of [PFLOTRAN](https://pflotran.org) (Hammond et al., 2014) used for simulations can be found archived [here](http://doi.org/10.5281/zenodo.3540881).

![](https://github.com/laagee/Agee_et_al_2020_RWU/blob/main/Scenario_Explanation.png?raw=true)

**Figure**. (a) Three scenarios of lateral spread with an increasing degree of interactions from left to right. Black filled circles mark stem locations with marker size proportional to DBH and black circles denote individual lateral spread. Representative individuals are marked in red. Figure depicts a subset of the simulation domain for clarity; see SM of manuscript for full simulation domain. (b) Relationship between DBH and root lateral spread as determined by site allometry. (c) Root architectures generated with the RootBox model (flat and tap root archetypes) for lateral spreads of 1m and 20m, with fixed maximum rooting depth of approximately 80cm (fourth and fifth branching order roots are not shown). 

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

Hammond, G. E., Lichtner, P. C., & Mills, R. T. (2014). Evaluating the performance of parallel subsurface simulators: An illustrative example with PFLOTRAN: Evaluating the Parallel Performance of Pflotran. Water Resources Research, 50(1), 208–228. https://doi.org/10.1002/2012WR013483

Leitner, D., Klepsch, S., Bodner, G., & Schnepf, A. (2010). A dynamic root system growth model based on L-Systems. Plant and Soil, 332(1–2), 177–192. https://doi.org/10.1007/s11104-010-0284-7




