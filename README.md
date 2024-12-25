# cognifyz-task-04-

Restaurant Data Analysis and Visualization Using Python
This project performs data analysis and visualization on a restaurant dataset using Python. The analysis includes mapping restaurant locations, visualizing city-wise restaurant counts, and analyzing average ratings by locality.

Overview
The program provides the following functionality:

Cleans and preprocesses restaurant data, handling missing values.
Maps restaurant locations using latitude and longitude on an interactive map.
Groups restaurants by cities and localities to analyze metrics like restaurant count and average ratings.
Visualizes top cities with the highest restaurant count.
Creates a heatmap to identify restaurant clusters.

Steps in the Program

Step 1: Import Necessary Libraries
The following libraries are used:

pandas: For data manipulation and aggregation.
matplotlib & seaborn: For plotting and data visualization.
folium: For creating interactive maps.
folium.plugins.HeatMap: For generating a heatmap to visualize restaurant density.

Step 2: Load the Dataset
The dataset is loaded from a CSV file using pd.read_csv().
Input Columns:
Latitude and Longitude: For restaurant location mapping.
Restaurant Name: Used for map markers.
City and Locality: Grouping and aggregation.
Aggregate rating: For analyzing average ratings.

Step 3: Handle Missing Values
Missing values in the Cuisines column are replaced with 'Unknown' using fillna() to maintain data consistency.

Step 4: Map Restaurant Locations
Interactive Map:
Restaurants are plotted on an interactive map using Folium.
The map is centered at the average latitude and longitude of all restaurants.
Each restaurant is represented by a marker, showing the restaurant's name when clicked.
Output:
The map is saved as an HTML file: simple_restaurant_map.html.


folium.Marker(
    location=[row['Latitude'], row['Longitude']],
    popup=row['Restaurant Name']
).add_to(restaurant_map)

Step 5: Grouping by City
City-Wise Analysis:
Restaurants are grouped by City.
Aggregated metrics include:
Restaurant Count: Total number of restaurants in each city.
Average Rating: Mean rating of restaurants in each city.

The top 5 cities by restaurant count are displayed:
mathematica

Top 5 Cities by Restaurant Count:
     City  Restaurant Count  Average Rating
1  Mumbai               200            4.2
2  Delhi                180            4.1

Step 6: Visualize Top Cities by Restaurant Count
Visualization:

A bar chart is plotted to show the top cities with the highest restaurant count.
Library Used: Seaborn.
Chart Features:
x-axis: City names.
y-axis: Number of restaurants.
Title: 'Top 10 Cities by Restaurant Count'.
Example Plot:
(Upload a sample chart to your repo)
Step 7: Analyze Localities
Locality-Wise Analysis:
Restaurants are grouped by Locality.
Aggregated metrics include:
Restaurant Count: Total number of restaurants.
Average Rating: Mean rating for each locality.

The top 5 localities with the highest average rating are displayed:

Top 5 Localities by Average Rating:
     Locality  Restaurant Count  Average Rating
1  Andheri                    50            4.5
2  Connaught Place            45            4.4
Step 8: Heatmap of Restaurant Concentrations
A heatmap is created to visualize clusters of restaurants based on their latitude and longitude.

Library Used: folium.plugins.HeatMap.
Steps:
Extract valid latitude and longitude data.
Generate a heatmap using the HeatMap plugin in Folium.
Save the heatmap as simple_restaurant_heatmap.html.
Output:
The heatmap highlights areas with a high concentration of restaurants.

Step 9: Key Insights
The analysis provides the following insights:

Top Cities:
Cities like Mumbai, Delhi, and Bangalore have the highest restaurant counts.
These cities often have more diverse cuisines and higher ratings.
Top Localities:
Localities with the highest ratings indicate areas with popular or high-quality restaurants.
Heatmap Insights:
The heatmap reveals clusters of restaurants, typically in urban centers or food hubs.

This project demonstrates how data analysis and visualization can reveal valuable insights about restaurant trends, locations, and popularity.
Feel free to contribute by improving the code or extending the functionality!
