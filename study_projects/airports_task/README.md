# Airport Data Analysis

This project analyzes airport data to address several tasks related to airport operations, focusing on flight statistics, data quality checks, and geospatial visualizations. The analysis covers the 10 largest airports in the world based on the number of takeoffs and landings, the identification of problematic data, and the enrichment of the dataset with continent information.

## Tasks Overview

### Task 1: Top 10 Airports by Takeoffs and Landings
The goal is to find the 10 largest airports worldwide based on the sum of takeoffs and landings. The result should be presented as a Pandas DataFrame, sorted from the largest to the smallest sum of takeoffs and landings. The DataFrame should have the following structure:
- **Index Level 1**: Country
- **Index Level 2**: Airport Name
- **Columns**: 
  - Takeoffs
  - Landings
  - Sum of Takeoffs/Landings

### Task 2: Data Quality Check
This task focuses on identifying problematic data, including erroneous or inconsistent entries. The results should be grouped by the types of identified issues. These issues may include:
- Missing values
- Duplicate entries
- Incorrect or inconsistent formatting

The findings should be explained using markdown, providing context for each type of error and how it affects the dataset.

### Task 3: Add Continent Column to the DataFrame
We need to enrich the airport dataset by adding a new column that indicates the continent for each airport. The continents are:
- Europe
- Asia
- Africa
- North America
- South America
- Australia/Oceania
- Antarctica

#### Task 3.1: Geospatial Visualization
Once the continent column is added, the next step is to visualize the airports on a world map. For each continent, we will plot the airports that belong to that continent using their IATA codes. This task will create 7 separate maps (one for each continent), which can be displayed interactively using either **Bokeh** or **Plotly**.

## Libraries and Tools Used
- **Pandas**: For data manipulation and analysis.
- **Matplotlib**: For static plotting and basic visualization.
- **Plotly / Bokeh**: For interactive visualizations.
- **Geopandas**: For geospatial analysis and handling geographic data.
- **IATA Codes**: To map airport locations and categorize by continent.

## Data Requirements
The dataset must contain the following columns for each airport:
- **Country**: The country where the airport is located.
- **Airport Name**: The name of the airport.
- **Takeoffs**: The number of takeoffs at the airport.
- **Landings**: The number of landings at the airport.

Additionally, the dataset will need to include IATA codes for the airports to plot their locations on the map.

## Expected Output
- **Task 1**: A DataFrame displaying the top 10 airports based on the sum of takeoffs and landings, sorted in descending order.
- **Task 2**: A markdown report highlighting problematic data with grouped error types.
- **Task 3**: The original DataFrame enriched with the continent column.
- **Task 3.1**: Interactive maps for each continent, showing airport locations.

