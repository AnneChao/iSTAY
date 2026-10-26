# iSTAY

**iSTAY: Information-Based Stability and Synchrony Measures**

This repository provides the R package `iSTAY` for computing information-based measures of temporal stability and synchrony, as described in the manuscript "A continuum of information-based temporal stability measures and their decomposition across hierarchical levels" by Chao et al. (2026).

The package provides functions for analyzing the temporal stability of populations, communities, and ecosystems, as well as synchrony among multiple time series. The measures are based on Hill numbers and parameterized by an order q greater than zero. The package also supports analyses of biodiversity–stability and biodiversity–synchrony relationships.

## Main functions

The `iSTAY` package provides the following main functions:

1. **`iSTAY_Single()`:** Computes information-based temporal stability measures for individual time series.
2. **`iSTAY_Multiple()`:** Computes gamma, alpha, and beta stability, as well as synchrony, for multiple time series. Both equal-weighting and biomass-weighting schemes are supported.
3. **`iSTAY_Hier()`:** Computes stability and synchrony measures across hierarchical levels.
4. **`ggiSTAY_qprofile()`:** Generates stability and synchrony profiles across different orders q.
5. **`ggiSTAY_analysis()`:** Generates graphical analyses of biodiversity–stability and biodiversity–synchrony relationships.

## Data

The analyses and examples are based on biomass time-series data from the Jena Experiment. The package includes the following datasets:

### Data_Jena_20_metacommunities

Biomass time-series data from 2003 to 2024 (22 years) for the constituent communities within each of the 20 metacommunities in the Jena Experiment. The dataset contains a list of 20 data frames, each with plots (communities) as rows and time points as columns.

All 76 plots (communities) are grouped into 20 metacommunities according to block identity and species-richness level. Each metacommunity consists of three or four plots with the same species richness but different species compositions.

### Data_Jena_462_populations

Biomass time-series data for 462 populations across 76 plots from 2003 to 2024 (21 years, excluding 2004). The dataset is a population-by-time data frame with 462 rows and 21 columns. Each row represents a population, and each column represents one year of biomass data.

### Data_Jena_76_community_populations

Biomass time-series data for 76 communities in the Jena Experiment. Each community dataset contains the 21-year biomass time-series data for all species sown within each plot. Because the number of species sown per plot ranges from 1 to 16, the number of populations within a community also ranges from 1 to 16.

This dataset contains the same data as `Data_Jena_462_populations`, but is organized for analytical convenience into a list of 76 communities, each containing a population-by-time biomass data frame for its constituent populations.

### Data_Jena_hierarchical_structure

A dataset included in the package for demonstrating stability and synchrony analyses across hierarchical levels.

The datasets can be loaded directly from the R package using `data()`.

## Installation

The `iSTAY` package is available from CRAN and can be installed using:

```r
install.packages("iSTAY")
library(iSTAY)
```

## Requirements

The package requires R version 4.1.0 or later. Required package dependencies are installed automatically when installing `iSTAY` from CRAN.

## Access information

The `iSTAY` package is available from [CRAN](https://cran.r-project.org/package=iSTAY).

An online version is also available at the [iSTAY Shiny App](https://chao.shinyapps.io/iSTAY/).

Detailed descriptions of the functions and examples are provided in the [iSTAY User's Guide](https://cran.r-project.org/package=iSTAY) and the package reference manual.

The biomass data from 2003 to 2023 were retrieved from [Jena Experiment Data (2003–2023)](https://jexis.idiv.de/ddm/Data/ShowData/624), while the 2024 data were obtained from [Jena Experiment Data (2024)](https://jexis.idiv.de/ddm/Data/ShowData/695).

## Related research

The theoretical framework and methodological details are described in Chao et al. (2026), "A continuum of information-based temporal stability measures and their decomposition across hierarchical levels."

The datasets and R source code used to reproduce the figures in the manuscript are also provided in the separate `MS_iSTAY` repository.