# Biodiversity Intactness of Phoenix

Biodiversity intactness is a measure of how much the original biodiversity of an area has been retained from its original state. In this repository I used BII data accessed through the Microsoft STAC catalog as well a TIGER shapefile (for Phoenix boundary) to find the changes in biodiversity between the years 2017 and 2020. Biodiversity intactness is an important measure of healthy and resilient ecosystems, and is particularly interesting to explore in an urbanized area such as Phoenix.

This analysis relies on the `xarray`,`geopandas`, and `numpy` Python libraries to perform raster operations. It was completed a part of the [final project](https://meds-eds-220.github.io/MEDS-eds-220-course/assignments/final-project.html) for EDS220 of the MEDS program (course information below).

## Repository Structure
```
├── .gitignore
      └── data
│        └── tl_2020_04_cousub
│           ├── tl_2020_04_cousub.cpg
│           ├── tl_2020_04_cousub.dbf
│           ├── tl_2020_04_cousub.prj
│           ├── tl_2020_04_cousub.shp
│           ├── tl_2020_04_cousub.shp.ea.iso.xml
│           ├── tl_2020_04_cousub.shp.iso.xml
│           └── tl_2020_04_cousub.shx
├── phoenix_bii.ipynb
└── README.md
```

## Data and Access

**Biodiversity Intactness Index:** 

The Biodiversity Intactness Index estimates how much of a region’s natural, undisturbed biodiversity is still left. It is represented as a percentage, from 0 to 100, with 100 being perfectly natural and undisturbed area. BII data is accessed through the [Microsoft Planetary Computer STAC catalog](https://planetarycomputer.microsoft.com/dataset/io-biodiversity). Rasters from the years 2017 and 2020 area accessed, then cropped to the Phoenix area. Accessing this data should take no more than running the code in the included notebook (no download necessary).

**Phoenix Subdivision:** 

Phoenix geometry (vector) data is sourced from the [TIGER/Line shapefiles](https://catalog.data.gov/dataset/tiger-line-shapefile-current-state-arizona-county-subdivision), from the U.S. Census Bureau. The files used correspond to Arizona counties and subdivisions from 2024. Data can easily be downloaded from the provided link to be placed in a 'data' folder. Filtering for the Phoenix subdivision is completed as part of this repository's analysis.

**Base Map:**

For one of our outputs, we plot the Phoenix subdivision onto a cropped map of Arizona. For this we accessed a geotile from the `contextily` package, which is a small Python package that retrieves tile maps from the internet. It is loaded in with the rest of the required libraries at the start of the notebook.

## References

Arribas-Bel, D. (2025). contextily (version 1.6.2) [Software]. https://github.com/geopandas/contextily

Microsoft. (n.d.). io-biodiversity [Dataset]. Microsoft Planetary Computer. Accessed December 6, 20205. https://planetarycomputer.microsoft.com/dataset/io-biodiversity

U.S. Census Bureau, U.S. Department of Commerce. (2025). TIGER/Line Shapefile, Current, State, Arizona, County Subdivision [Dataset]. data.gov. Accessed December 6, 2025. https://catalog.data.gov/dataset/tiger-line-shapefile-current-state-arizona-county-subdivision

## Course Information

-   **Course Title:** [EDS 220 - Working with Environmental Datasets](https://meds-eds-220.github.io/MEDS-eds-220-course/)
-   **Term:** Fall 2025
-   **Program:** [UCSB Masters in Environmental Data Science](https://bren.ucsb.edu/masters-programs/master-environmental-data-science).

Teaching Team:

-   **Instructor:** [Carmen Galaz García](https://github.com/carmengg)
-   **Co-Instructor:** [Annie Adams](https://github.com/annieradams)
