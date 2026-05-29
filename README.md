# Climate and Cost: A Data-Driven Look at California Housing Markets

An end-to-end data analytics project that investigates how climate, geography, and location influence housing prices across California. The project combines real estate listing data, geospatial information, and weather data to uncover patterns in property pricing and market trends.

---

## Project Overview

This project builds a multi-stage ETL (Extract, Transform, Load) pipeline that:

* Collects California housing listings from Redfin
* Extracts property-level information
* Enriches listings with geographic coordinates using Google Maps Geocoding API
* Integrates climate data using OpenWeather API
* Merges multiple datasets into a unified analytical dataset
* Performs exploratory data analysis and visualization to identify pricing trends

---

## Research Questions

This project explores the following questions:

1. How do climatic conditions correlate with housing prices per square foot?
2. Are coastal properties significantly more expensive than inland properties?
3. Does climate variability influence property values?
4. How does latitude impact housing prices across California?

---

## Tech Stack

**Languages & Libraries**

* Python
* Pandas
* NumPy
* Requests
* BeautifulSoup

**APIs**

* Google Maps Geocoding API
* OpenWeather API

**Visualization**

* Matplotlib
* Seaborn

**Environment**

* Jupyter Notebook

---

## Data Pipeline

1. Scrape California property URLs from Redfin sitemap pages
2. Generate `filtered_redfin_links.tsv`
3. Extract property details into `redfin_property_details.csv`
4. Geocode addresses into `redfin_property_locations.csv`
5. Retrieve weather information into `redfin_property_weather_data.csv`
6. Merge datasets into `final_dataset_redfins.csv`
7. Perform exploratory data analysis and visualization
```

### Step 1: Collect Property Links

Scrape California property listing URLs from Redfin sitemap pages and store them for processing.

### Step 2: Extract Property Information

Retrieve property-level details including:

* Property Address
* Listing Price
* Bedrooms
* Bathrooms
* Square Footage

### Step 3: Geocode Addresses

Use the Google Maps Geocoding API to convert property addresses into:

* Latitude
* Longitude

### Step 4: Retrieve Climate Data

Use the OpenWeather API to collect weather information for each property location, including:

* Temperature
* Humidity
* Wind Speed

### Step 5: Build Final Dataset

Merge housing, geospatial, and climate datasets into a single analytical dataset.

### Step 6: Analysis & Visualization

Perform exploratory analysis to identify relationships between housing prices, climate variables, and geographic factors.

---

## Generated Files

The following files are automatically generated during execution of the notebook:

| File                             | Description                               |
| -------------------------------- | ----------------------------------------- |
| filtered_redfin_links.tsv        | Filtered California property listing URLs |
| redfin_property_details.csv      | Extracted property information            |
| redfin_property_locations.csv    | Latitude and longitude data               |
| redfin_property_weather_data.csv | Weather information for each property     |
| final_dataset_redfins.csv        | Final merged dataset used for analysis    |

These files act as intermediate outputs within the ETL pipeline and are consumed by subsequent stages of the workflow.

---

## Key Findings

### Coastal Premium

Properties located near California's coastline exhibited significantly higher prices per square foot compared to inland properties.

### Housing Prices and Climate

Climate variables such as temperature, humidity, and wind speed showed relatively weak direct correlations with property prices.

### Geographic Influence

Location-based factors had a stronger influence on property values than climate metrics alone.

### Latitude Analysis

Latitude demonstrated only a weak relationship with housing prices, suggesting that local economic and geographic factors drive pricing more significantly.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/ATHISH-RAJ-MOHAN/Climate-and-Cost---A-Data-Driven-Look-at-California-Housing.git
cd Climate-and-Cost---A-Data-Driven-Look-at-California-Housing
```

Install required packages:

```bash
pip install pandas numpy requests beautifulsoup4 matplotlib seaborn
```

---

## API Configuration

This project requires API keys for:

### Google Maps Geocoding API

Used for converting property addresses into geographic coordinates.

### OpenWeather API

Used for collecting weather and climate data for each property location.

Add your API keys within the notebook before execution:

```python
GOOGLE_MAPS_API_KEY = "YOUR_API_KEY"
OPENWEATHER_API_KEY = "YOUR_API_KEY"
```

---

## Running the Project

1. Open `California_Housing_Markets.ipynb`
2. Configure API keys
3. Execute the notebook sequentially
4. Generated datasets will be created automatically
5. Review visualizations and analytical findings

---

## Future Improvements

* Expand dataset coverage across additional states
* Incorporate demographic and economic indicators
* Build predictive machine learning models for property valuation
* Develop an interactive dashboard for real-time exploration
* Automate data refresh and pipeline scheduling

---
