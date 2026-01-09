# covid19germany

Repository for AGILE 2026 submission *Analysis of the spatial and temporal pattern of COVID-19 incidence rate across Germany*

The repository provides the R-code used to produce the results presented in the submitted manuscript. For the readers convenience, the data has already been preprocessed and is available as .RData files that are loaded by the respective RMarkdown files. In addition, the `data_preprocessng.Rmd` document contains the code used for the preprocessing of the original data files.

## Overview

- `data_preprocessing.Rmd` (not required to be executed) contains the code to preprocess the data
- `data_analysis.Rmd` contains the regression modelling part of the analysis as well as the mapping of the spatial eigenvectors, spatially varying regression coefficients and the hierarchical clustering
- `SAC.Rmd` handles the calculation of the spatial autocorrelation timeseries and the related plot

## Requirements

To run the code the following software is required:

- R (https://cran.r-project.org/), version 4.4.1 has been used during the analysis
- RStudio (https://posit.co/download/rstudio-desktop/) , version 2026.01.0+392 "Apple Blossom" has been used
- R packages:
  - rmdformats 1.04 - templates for the creation of static HTML files from the RMarkdown code in RStudio (`knit`)
  - tidyverse 2.0.0- data processing and pipe operator
  - ggplot2 4.0.0 - plotting
  - GGally 2.4.0 - plotting
  - ggpubr 0.6.1 - plotting
  - spatialreg 1.4.2- spatial regression including spatial eigenvector mapping
  - lubridate 1.9.3 - working with time and date objects
  - sf 1.0-21- simple features/working with vector data
  - spdep 1.4.1 - defining and working with spatial relationships (neighborhood, spatial weight matrix), spatial autocorrelation
  - tmap 4.2 - thematic maps (tmap v4 syntax is used)
  - readODS 2.3.2 - reading/writing ods documents

The R packages can be installed inside R/Rstudio via the GUI or by the command 
`install.packages("rmdformats", "tidyverse", "GGally", "ggpubr", "spatialreg", "lubridate", "sf", "spdep", "tmap", "readODS")` (`ggplot2`is part of the base installation of R)
Depending packages and external libaries should be automatically installed in addition by that step. This includes GDAL (>= 2.0.1), GEOS (>= 3.4.0), PROJ (>= 4.8.0), sqlite3 required by `sf`.

The RMarkdown code assumes that all data is stored in a `data` subfolder and that images are saved in an `img` subfolder.



