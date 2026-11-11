# Global Retail Outlet Mapping & Intelligence

**Tools:** Python, Jupyter Notebook, Pandas, Requests, REST API, JSON, Folium, Matplotlib

## Project Overview

This project explores the collection, cleaning and geographic analysis of business-related location data within a selected area of Abuja, Nigeria.

Using the OpenStreetMap Overpass API, I retrieved location records covering shops, pharmacies, restaurants, cafés and fast-food outlets. The extracted data was processed with Python and Pandas, assessed for quality and visualised using an interactive geographic map.

## Project Objectives

- Extract business-related location data through a public REST API.
- Convert raw JSON responses into a structured dataset.
- Assess missing values, repeated names and inconsistent categories.
- Standardise business categories and validate geographic coordinates.
- Analyse business-category distribution and geographic concentration.
- Build an interactive map for exploring business locations.

## Data Source and Collection

**Source:** OpenStreetMap  
**API:** Overpass API  
**Geographic coverage:** Selected pilot bounding box around central Abuja, Nigeria.

The query retrieved OpenStreetMap elements tagged with `shop` and selected `amenity` categories.

The geographic bounding box used was:

- South: 8.8
- West: 7.2
- North: 9.2
- East: 7.6

## Data Processing

The extraction returned 433 OpenStreetMap elements in JSON format.

The data was transformed into a Pandas DataFrame containing 15 attributes, including:

- Business name and brand
- Shop and amenity categories
- Phone number and email
- Website and opening hours
- Street, city and postcode
- Latitude and longitude

Data quality checks included missing-value assessment, repeated business-name investigation, category standardisation and coordinate validation.

## Key Findings

- 433 OpenStreetMap elements were retrieved.
- 389 records (89.8%) had identifiable business categories.
- 44 records (10.2%) remained unclassified.
- Restaurants were the most frequently represented category, with 87 records.
- Supermarkets, malls and pharmacies were also prominent categories.
- The two most populated geographic grid cells contained approximately 65.8% of all extracted records.
- All extracted coordinates fell within the selected bounding box.

## Interactive Map

An interactive map was developed using Folium. It supports geographic exploration through category-based layers, including restaurants, supermarkets, malls, pharmacies, fast-food outlets, cafés, other classified categories and unclassified records.

## Project Deliverables

- `Global_Retail_Outlet_Mapping.ipynb` – data collection, cleaning and analysis notebook.
- `abuja_retail_businesses_raw.json` – original API response.
- `abuja_retail_businesses_cleaned.csv` – cleaned and structured dataset.
- `abuja_retail_business_map.html` – interactive geographic map.

## Limitations

- OpenStreetMap data may be incomplete or outdated.
- Not all business records contain contact or address information.
- Repeated business names do not necessarily indicate duplicate outlets.
- The study covers a selected pilot area, not all of Abuja or the FCT.
- Extracted map elements should not be interpreted as a verified count of active businesses.

## Technologies Used

- Python
- Jupyter Notebook
- Requests
- Pandas
- JSON
- Matplotlib
- Folium
- OpenStreetMap Overpass API

## Reproducibility

Install the required packages:

```bash
pip install requests pandas matplotlib folium
```

Run the notebook cells in order to retrieve, process, analyse and visualise the data.

## Data Attribution and Licence

Location data was obtained from OpenStreetMap contributors.

© OpenStreetMap contributors. Data is available under the Open Database License (ODbL).

https://www.openstreetmap.org/copyright

The Overpass API is a community-provided service. Users should respect its usage policies and avoid excessive requests.
