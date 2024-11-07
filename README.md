# Geospatial Data Extraction and Integration for Correlation Analysis in Tucson, Arizona

## Objective: 
Develop an efficient extraction and integration workflow for geospatial datasets, including LANDSAT imagery analysis to obtain derived indices (NDVI, SAVI, NBDI, MNDWI), SRTM elevation data, and land cover information. This dataset supported advanced correlation analysis with machine learning, focusing on environmental variables to urban planning and sustainability studies.

## Workflow
This project workflow integrates geospatial data from various sources and prepares it for correlation analysis. The process leverages ArcGIS and Python’s ArcPy library to extract, calculate, and compile datasets for machine learning applications. Below is a step-by-step breakdown:

### Define Study Area:

- Extract by Mask Tool: To focus analysis on a specific area, this tool extracts the study region from larger raster datasets, setting a defined geographic boundary for all data layers. This helps streamline processing and ensures consistency across datasets.

### Index Calculation:

- Raster Calculator with ArcPy: Using Raster Calculator in ArcPy, indices like SAVI (Soil-Adjusted Vegetation Index), NDVI (Normalized Difference Vegetation Index), NDBI (Normalized Difference Built-up Index), and MNDWI (Modified Normalized Difference Water Index) are calculated from LANDSAT imagery. This step allows us to derive valuable environmental indicators, capturing variations in vegetation, built-up areas, and water presence.

### Topographic Processing:

- Slope Tool: For the Digital Elevation Model (DEM), the Slope tool is used to calculate the slope gradient. This topographic layer is essential for understanding terrain variation and its potential influence on environmental variables.

### Land Cover Classification:

- Reclassify Tool: To simplify analysis, the land cover dataset is reclassified to group different land types into broader, more manageable categories (e.g., forest, urban, water). This aids in focusing on relevant environmental variables.

### Data Integration:

- Extract Multi-Values to Points Tool: This final step consolidates all processed data layers into a single spatial point dataset. By extracting pixel values from each raster layer (indices, slope, land cover) and assigning them to corresponding points, a unified database is created, with each point containing all necessary environmental attributes.
