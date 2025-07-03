# Real Estate Data Transformation Project

Welcome to the **Real Estate Data Transformation Project** – a robust data engineering solution designed to transform raw, inconsistent real estate listings into **clean, standardised, and business-ready datasets** using the **Medallion Architecture**.

---

## Project Overview

Real estate data is often messy: unstructured text, inconsistent formats, currency issues, duplicates, and missing values can make analysis impossible. This project builds a **powerful end-to-end data transformation pipeline** that solves these challenges by:
- Cleaning and standardising real estate listings.
- Structuring property features for powerful analytics.
- Enabling accurate market insights and buyer-friendly dashboards.

---

## Architecture: Medallion Layers

We leverage the **Medallion Architecture** to progressively refine the data:

### Bronze Layer: Raw Data
- Stores unprocessed listings from multiple sources.
- Handles inconsistencies, duplicates, and missing values.
- Raw data saved as `bronze_layer_real_estate.parquet`.

### Silver Layer: Cleaned & Enriched Data
- Standardises currencies, areas, and categorical features.
- Imputes missing values intelligently using multi-column context.
- Prepares data for complex business transformations.

### Gold Layer: Business-Optimised Data
- Adds unique property IDs, location extraction, and property types (BHK, Villas, Apartments).
- Computes key features like `price_per_sqft` and `price_per_sqft_category` (Budget, Mid-Range, Luxury).
- Fully optimised for dashboards, search, filtering, and business analytics.

---

## Key Business Benefits
- **Consistent Property Listings:** Accurate filtering and selection.
- **Reliable Pricing Insights:** Supports buyer and investor decisions.
- **Enhanced Analytics and Dashboards:** For marketing, sales, and reporting.
- **Segmented Market Analysis:** Pricing categories, locations, and property types.

---

## Gold Layer Data Model

| Feature                | Description                                      |
|----------------------- |--------------------------------------------------|
| `property_id`          | Unique property identifier                       |
| `property_name`        | Standardised listing name                        |
| `location`             | Extracted locality and city                      |
| `square_feet`          | Numeric property size                            |
| `area_type`            | Carpet Area or Super Area                        |
| `transaction`          | New or Resale                                    |
| `status`               | Ready to Move or Under Construction              |
| `floor_number`         | Extracted floor number                           |
| `total_floors`         | Total building floors                            |
| `furnishing`           | Unfurnished, Semi-Furnished, Fully Furnished      |
| `facing`               | Standardised property direction                  |
| `price_per_sqft`       | Numeric price per square foot                    |
| `price`                | Standardised total price (INR)                   |
| `price_per_sqft_category` | Budget, Mid-Range, Luxury                     |
| `bhk`                  | Number of bedrooms                               |
| `property_type`        | Apartment, Villa, Plot                           |

---

## Tech Stack
- **Data Processing:** `pandas`, `numpy`, `re`, `uuid`
- **Visualization:** `matplotlib`, `seaborn`, `plotly`, `missingno`
- **Feature Engineering:** `sklearn.preprocessing`, `scipy.stats`, `statsmodels`
- **Machine Learning:** `sklearn.ensemble.GradientBoostingRegressor`
- **Statistical Transformations:** `boxcox`, `PowerTransformer`, `RobustScaler`, `MinMaxScaler`
- **Utility:** `tabulate`, `time`
