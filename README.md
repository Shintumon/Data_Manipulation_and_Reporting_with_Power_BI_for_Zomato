# Data Manipulation and Reporting with Power BI for Zomato

## Project Description

This project is focused on creating an interactive and consolidated Power BI dashboard for **Zomato**, a restaurant aggregation and meal delivery service based in India. Zomato operates across the globe and provides detailed information about numerous eateries and customer reviews. The goal of this project is to analyze the data and deliver meaningful insights that allow Zomato's stakeholders to make data-driven decisions.

The dataset used in this project includes information about restaurants from various continents, countries, and cities, and was provided in Excel format.

### Key Objectives

The Power BI report allows Zomato to:

1. Derive data on the total number of restaurants globally, including continents, countries, and cities.
2. View data at a global scale with drill-down capabilities.
3. Identify restaurants with the highest average customer ratings.
4. Discover restaurants with the lowest average costs.
5. Filter and view restaurants based on:
   - Geographical dimensions (continent, country, city).
   - The services they provide (online ordering or reservation services).
   - Average rating color slabs.
6. Highlight restaurants offering the most cuisines.
7. Present data in a user-friendly, multi-page report aligned with Zomato's theme.
8. Make the report accessible from both web browsers and mobile devices.

---

## Implementation Steps

### Data Transformation

1. **Data Import**: Import data from multiple Excel files containing regional restaurant information.
2. **Data Cleaning**:
   - Correct city names for consistency (e.g., `Sí£o Paulo` → `São Paulo`).
   - Remove ambiguity in city names (e.g., `Cedar Rapids/Iowa City` → `Cedar Rapids`).
   - Remove unnecessary columns (e.g., `Locality`, `Locality Verbose`).
3. **Column Enhancements**:
   - Create separate columns for `Restaurant Name` and `Restaurant Address` by splitting relevant data fields.
4. **Cuisine Table**:
   - Generate a separate table listing cuisines for each restaurant by splitting data and removing duplicates.
5. **Country-Code Table**:
   - Ensure the `Country-Code` dimension table contains only unique, non-blank values.
6. **Relationships**:
   - Establish relationships between tables in the Power BI model view for better data connectivity.

---

### DAX Calculations

1. **Rating Color Column**:
   - Add a `Rating Color` column based on the following rules:
     - Aggregate Rating > 4.5 → Dark Green
     - Aggregate Rating between 4.0 and 4.4 → Green

2. **Key Measures**:
   - `Restaurant Count`: Total count of restaurants.
   - `Average Cost`: Average cost for two people.
   - `Average Rating`: Average customer rating.
   - `Cuisine Count`: Total distinct cuisines served.

3. **Continent Mapping**:
   - Add a `Continent` column to the `Country-Code` table using the following mapping:
     - `Africa`: South Africa
     - `Europe`: Countries in Europe
     - `NAM`: North America
     - `SAM`: South America
     - `Oceania`: Australia, New Zealand
     - `Asia`: Countries in Asia

---

## Dashboard Features

1. **Global View**:
   - Display the total number of restaurants worldwide, segmented by continent, country, and city.
2. **Drill-Down Functionality**:
   - Users can navigate from a global overview to specific country or city-level details.
3. **Insights on Ratings**:
   - Highlight restaurants with the highest and lowest average ratings.
   - Use rating colors (Dark Green/Green) for easy visualization.
4. **Cuisines Analysis**:
   - Identify restaurants offering the widest variety of cuisines.
5. **Cost Analysis**:
   - Discover restaurants with the lowest average costs for meals.
6. **Interactive Filters**:
   - Apply filters based on geographical data, service types, and rating slabs.

---

## Result

The finalized Power BI report meets the project goals and provides:

- A multi-page, theme-aligned dashboard for Zomato.
- Seamless navigation across sections.
- Compatibility for web browsers and mobile devices.
- Drill-through and filtering capabilities for granular data analysis.

![Global Analysis](images/Global%20Analysis.png)

![Performance Details](images/Performance%20Details.png)

![Restaurant Details](images/Restaurant%20Details.png)

---

## Key Learnings

- Data preparation and transformation in Power BI.
- Efficient use of DAX to create calculated columns and measures.
- Designing intuitive, interactive dashboards.
- Ensuring compatibility and accessibility for diverse platforms.

---
