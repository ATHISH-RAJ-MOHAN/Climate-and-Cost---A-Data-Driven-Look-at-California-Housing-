# Climate and Cost: A Data-Driven Look at California Housing Markets

An end-to-end data analysis project that explores how housing prices in California relate to geography and climate.  
This project collects property listings from Redfin, enriches them with geolocation and weather data, and analyzes how climate variables, coastal proximity, and latitude relate to price per square foot.

## Project Overview

This notebook builds a multi-stage data pipeline:

1. Scrape California property listing links from Redfin sitemap pages
2. Extract property details such as price, beds, baths, sqft, and address
3. Geocode each property address using the Google Maps Geocoding API
4. Fetch weather data for each property using the OpenWeather API
5. Merge all datasets into one final analysis-ready dataset
6. Perform exploratory analysis on housing prices, climate, and location patterns

## Key Questions Explored

- How do climatic conditions correlate with property prices per square foot in California?
- Are homes in coastal cities more expensive than inland areas?
- Does climate variability influence home prices or housing demand?
- Does latitude influence property prices after controlling for climate variables?

## Tech Stack

- **Python**
- **Pandas**
- **Requests**
- **BeautifulSoup**
- **Google Maps Geocoding API**
- **OpenWeather API**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

## Features

- Web scraping of California Redfin sitemap pages
- Property-level data extraction from listing pages
- Geocoding of addresses into latitude and longitude
- Weather enrichment using location-based climate data
- Dataset merging across multiple sources
- Correlation heatmaps, bar charts, and scatter plots
- Analysis of coastal vs inland pricing patterns
- Latitude band analysis for geographic pricing trends

## Workflow

### 1. Scrape Redfin Property Links
The notebook first scrapes Redfin sitemap pages for California home links and filters the URLs to keep only California property pages.

### 2. Extract Property Details
For each listing, the notebook extracts:
- Address
- Price
- Bedrooms
- Bathrooms
- Square footage

### 3. Geocode Property Addresses
Using the Google Maps Geocoding API, each address is converted into:
- Latitude
- Longitude

### 4. Fetch Weather Data
Using the OpenWeather API, the notebook fetches climate variables such as:
- Average temperature
- Wind speed
- Humidity

### 5. Merge All Datasets
The extracted datasets are merged into one final dataset for analysis.

### 6. Analyze Housing Patterns
The notebook examines:
- Climate vs price per square foot
- Coastal vs inland price differences
- Extreme climate conditions
- Latitude bands and price variation

## Key Findings

- Climate variables such as temperature, windspeed, and humidity show weak correlation with price per square foot.
- Coastal cities tend to have much higher median prices per square foot than inland cities.
- Extreme climate conditions may have some effect on pricing, but other factors appear more important overall.
- Latitude alone has a very weak correlation with price, suggesting that local economic and geographic factors matter more.

## Repository Structure

```text
.
├── California_Housing_Markets.ipynb
├── README.md
└── data/
    ├── filtered_redfin_links.tsv
    ├── redfin_property_details.csv
    ├── redfin_property_locations.csv
    ├── redfin_property_weather_data.csv
    └── final_dataset_redfins.csv
