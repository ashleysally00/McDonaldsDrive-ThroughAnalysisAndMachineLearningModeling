# McDonald's Data Project: Heat Map, Bar Graph, Drive-Through Analysis, and Machine Learning Modeling

## 1. Dataset Acquisition and Setup
- I downloaded the dataset containing information about McDonald's locations from an online source (the exact website is not specified).
- I imported this dataset into Visual Studio Code (VSC) within a Jupyter notebook for analysis. The dataset includes various columns such as `store_brand`, `store_id`, `city`, `state_code`, `open_hours_drive_through`, etc.

## 2. Data Filtering and Preparation
- **Filtering for California**:
  - I used **Data Filtering** with pandas to select rows where the `state_code` or `state_name` matched "CA" or "California". This was achieved using pandas DataFrame operations (e.g., `df[df['state_code'] == 'CA']`).
- **Identifying Drive-Through Locations**:
  - I used **Boolean Indexing** to filter the dataset to include only locations with drive-through information by checking the `open_hours_drive_through` column. I applied a boolean mask to select rows where this column indicated the presence of a drive-through.
- **Filtering for Specific Hours**:
  - I further filtered the data to identify drive-throughs open at 3 AM by using **Conditional Statements**. I checked if the `open_hours_drive_through` column contained information indicating that the drive-through was open at 3 AM (e.g., `df[df['open_hours_drive_through'].str.contains('03:00')]`).

## 3. Creating the Heat Map
- I used **Folium** to create a heat map to visualize the density of McDonald's locations in California.
- I applied **Geospatial Techniques** to generate the heat map. This involved converting the filtered data into latitude and longitude coordinates and using Folium’s `HeatMap` function to display areas with higher concentrations of McDonald's locations.

## 4. Creating the Bar Graph
- I created a bar graph to visualize the distribution of McDonald's locations across different regions or states.
- I used **Pandas and Matplotlib** for this task. I aggregated the number of McDonald's locations by region or state using pandas’ grouping and aggregation functions, then plotted this data using Matplotlib’s bar plot functions.

## 5. Machine Learning Analysis
- In a separate Jupyter notebook, I applied machine learning techniques using the same McDonald's dataset.
- I explored various machine learning models to analyze and predict patterns in the data. This included tasks such as:
  - **Data Preprocessing**: Cleaning and preparing the data for machine learning models.
  - **Feature Selection**: Identifying relevant features for model training.
  - **Model Training**: Training models to predict aspects such as the presence of drive-throughs, location density, or other relevant metrics.
  - **Model Evaluation**: Assessing the performance of the models using metrics such as accuracy, precision, recall, and F1-score.

## 6. HTML Integration
- I added the generated map, heat map, and bar graph to an `index.html` file.
- I ensured that the titles of the maps and graphs were properly aligned above the corresponding visualizations to maintain a clean layout.

## 7. Deployment
- I deployed the HTML file displaying the map on a webpage through Netlify, making the interactive map accessible online. This webpage focused on McDonald's locations.

