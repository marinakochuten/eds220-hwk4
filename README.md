# 2017 Thomas Fire Scar Visualization

This repository contains Jupyter Notebooks for my analysis and visualization of the [2017 Thomas Fire](https://en.wikipedia.org/wiki/Thomas_Fire) burn scars. This fire burned about 281,893 acres, making it the 8th largest fire in California's history. 

![thomas fire](https://ca-times.brightspotcdn.com/dims4/default/7aca077/2147483647/strip/true/crop/2048x1365+0+0/resize/1440x960!/format/webp/quality/75/?url=https%3A%2F%2Fcalifornia-times-brightspot.s3.amazonaws.com%2Fe3%2F17%2F6803239007424db677d324a459ac%2Fla-me-thomas-fire-photos-010)
Image credits: [Michael Owen Baker / For the LA Times](https://www.latimes.com/local/lanow/la-me-thomas-fire-photos-photogallery.html)


## Repository content and structure

```
eds220-hwk4
│   README.md
│   hwk4-task2-fire-perimeter-YOURLASTNAME.ipynb
│   hwk4-task2-false-color-YOURLASTNAME.ipynb
│   .gitignore
│
└───data
    ├── california_fire_perimeters
    │   ├── california_fire_perimeters.cpg
    │   ├── california_fire_perimeters.dbf
    │   ├── california_fire_perimeters.prj
    │   ├── california_fire_perimeters.shp
    │   ├── california_fire_perimeters.shp.xml
    │   └── california_fire_perimeters.shx
    └─── thomas_fire_boundary.geojson
```

- hwk4-task2-fire-perimeter-kochuten.ipynb contains the code for wrangling historic, open-source fire perimeter data to a geospatial file containing only the boundary for the 2017 Thomas Fire.
- hwk4-task2-false-color-kochuten.ipynb contains the code for the false color imagery and burn scar visualization.
    
## Data details

**Fire perimeters:** I use California Fire Perimeter data from the State of California's Data Catalog to create thomas_fire_boundary.geojson. The dataset is updated annually and includes fire perimeters dating back to 1878. 
- **Source:** State of California Data Catalog (2024), *California Fire Perimeters (all)* [Data set] Available from: https://catalog.data.gov/dataset/california-fire-perimeters-all-b3436. Access date: November 18, 2024.

**Landsat imagery:** I use a simplified collection of bands (red, green, blue, near-infrared and shortwave infrared) from the Landsat Collection 2 Level-2 atmosperically corrected surface reflectance data, collected by the Landsat 8 satellite. The data was retrieved from the Microsof Planetary Computer data catalogue and pre-processed by Dr. Carmen Galaz García to remove data outside land and coarsen the spatial resolution. 
- **Source:** Microsof Planetary Computer data catalogue (2024), *Landsat Collection 2 Level-2 (simplified)* [Data set] Available from: https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2. Access date: November 18, 2024.

## Acknowledgements

This repository was created as an assignment for the graduate course EDS 220: Working with Environmental Datasets in the [Masters of Environmental Data Science (MEDS) program](https://bren.ucsb.edu/masters-programs/master-environmental-data-science), taught by [Dr. Carmen Galaz García](https://github.com/carmengg).


