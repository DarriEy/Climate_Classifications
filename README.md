# Climate Classifications

A collection of Python notebooks and scripts for classifying global climate scenarios using different climate classification systems:

- Holdridge Life Zones
- Köppen-Geiger Climate Classification 
- Thornthwaite Climate Classification

## Overview

This project uses NASA's GDDP-CMIP6 climate data through Google Earth Engine to classify global climates. It includes implementations of multiple classification systems to analyze both historical and future climate scenarios.

## Prerequisites

- Python 3.11+
- Google Earth Engine account and authentication
- Required Python packages:
  ```
  earthengine-api
  pandas
  matplotlib
  ```

## Project Structure

```
.
├── Holdridge.ipynb          # Holdridge life zones classification
├── Koppen_Geiger.ipynb      # Köppen-Geiger climate classification
├── Thornthwaite.ipynb      # Thornthwaite climate classification
├── holdridge.py            # Helper functions for Holdridge classification
├── 1a_regional_stats.ipynb # Analysis of regional classification data
└── README.md
```

## Setup

1. Install required packages:
   ```bash
   pip install earthengine-api pandas matplotlib
   ```

2. Authenticate with Google Earth Engine:
   ```python
   import ee
   ee.Authenticate()
   ee.Initialize(project='your-project-name')
   ```

## Data Sources

- Climate Data: NASA-GDDP CMIP6 dataset via Google Earth Engine
- Elevation Data: USGS GTOPO30 Digital Elevation Model
- Regional Boundaries: USDOS LSIB Simple 2017

## Usage

Each classification system is implemented in its own Jupyter notebook:

1. **Holdridge Life Zones**
   - Uses biotemperature, precipitation, and potential evapotranspiration ratio
   - Includes both altitudinal and latitudinal classifications

2. **Köppen-Geiger**
   - Uses temperature and precipitation thresholds
   - Classifies into main climate groups and subtypes

3. **Thornthwaite**
   - Based on potential evapotranspiration
   - Considers moisture and thermal indices

Regional statistics can be analyzed using `1a_regional_stats.ipynb`.

## Output

The classification results are provided as:
- Earth Engine image layers
- Regional statistics in CSV format
- Visualizations using custom color palettes

## Contributing

Feel free to open issues or submit pull requests with improvements.

## License

This project is licensed under the GNU General Public License v3.0 

## Contact

Darri Eythorsson, University of Calgary

darri.eythorsson@ucalgary.ca
