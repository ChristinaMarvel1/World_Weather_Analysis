# World_Weather_Analysis

## Deliverable 1: Retrieve Weather Data
Generate a set of 2,000 random latitudes and longitudes, retrieve the nearest city, and perform an API call with the OpenWeatherMap. In addition to the city weather data you gathered in this module, use your API skills to retrieve the current weather description for each city. Then, create a new DataFrame containing the updated weather data.

1. Create a folder called Weather_Database.

2. Create a new Jupyter Notebook file to retrieve the weather data, and name it Weather_Database.ipynb.

3. Create a new set of 2,000 random latitudes and longitudes.

4. Get the nearest city using the citipy module.

5. Perform an API call with the OpenWeatherMap.

6. Retrieve the following information from the API call:

 - Latitude and longitude
 - Maximum temperature
 - Percent humidity
 - Percent cloudiness
 - Wind speed
 - Weather description (for example, clouds, fog, light rain, clear sky)
7. Add the data to a new DataFrame.

8. Export the DataFrame as a CSV file, and save it as WeatherPy_Database.csv in the Weather_Database folder.

## Deliverable 2: Create a Customer Travel Destinations Map
Use input statements to retrieve customer weather preferences, then use those preferences to identify potential travel destinations and nearby hotels. Then, show those destinations on a marker layer map with pop-up markers.

1. Create a folder called Vacation_Search.

2. Download the Vacation_Search_starter_code.ipynb file into your Vacation_Search folder, and rename it Vacation_Search.ipynb.

3. In the Vacation_Search.ipynb file, make sure the dependencies and API keys are imported correctly.

4. Use the instructions below to add code where indicated by the numbered-step comments in the starter code file.

5. In Step 1, import the WeatherPy_Database.csv file from your Weather_Database folder from Deliverable 1 as a DataFrame.

6. In Step 2, write two input statements that prompt the user to enter their minimum and maximum temperature criteria for their vacation.

7. In Step 3, use the loc method to filter the city_data_df DataFrame for temperature criteria collected in Step 2, then create a new DataFrame.

8. In Steps 4a-b, determine if there are any empty rows, then drop them if necessary and create a new DataFrame.

9. In Steps 5a-b, use the provided code to create a new DataFrame, hotel_df, that will hold the hotel names from the hotel search in Steps 6a-6f.

10. In Step 6a, we have supplied the search parameters, which are the same as in this module, that you’ll need to use to search for a hotel for each city in Steps 6b-f.

11. In Steps 6b-f, iterate through the hotel_df DataFrame, retrieve the latitude and longitude of each city to find the nearest hotel based on the search parameters from Step 6a, then add the hotel name to the hotel_df DataFrame. If a hotel isn't found, skip to the next city.

12. In Step 7, drop any rows in the hotel_df DataFrame where a hotel name is not found.

13. In Steps 8a-b, create an output file to store the hotel_df DataFrame as WeatherPy_vacation.csv in the Vacation_Search folder.

14. In Step 9, add the city name, the country code, the weather description, and the maximum temperature for the city to the info_box_template format template we have provided.

15. In Step 10a, use the provided list comprehension code to retrieve the city data from each row, which will then be added to the formatting template and saved in the hotel_info list.

16. In Step 10b, use the provided code snippet to retrieve the latitude and longitude from each row and store them in a new DataFrame.

17. In Steps 11a-b, refactor your previous marker layer map code to create a marker layer map that will have pop-up markers for each city on the map.

18. Take a screenshot of your map and save it to the Vacation_Search folder as WeatherPy_vacation_map.png.

## Deliverable 3: Create a Travel Itinerary Map
Use the Google Directions API to create a travel itinerary that shows the route between four cities chosen from the customer’s possible travel destinations. Then, create a marker layer map with a pop-up marker for each city on the itinerary.

1. Enable the "Directions API" in your Google account for your API key.

2. Create a folder called Vacation_Itinerary.

3. Download the Vacation_Itinerary_starter_code.ipynb file into your Vacation_Itinerary folder and rename it Vacation_Itinerary.ipynb.

4. In the Vacation_Itinerary.ipynb file, make sure the dependencies and API keys are imported.

5. Use the instructions below to add code where indicated by the numbered-step comments in the starter code file.

6. In Step 1, import the WeatherPy_vacation.csv file from your Vacation_Search folder from Deliverable 2 as a DataFrame.

7. In Steps 2-4, copy or refactor the code from Steps 11a-b of Deliverable 2 to create a marker layer map of the vacation search results.

8. From the vacation search map, choose four cities that a customer might want to visit. They should be close together and in the same country.

9. In Step 5, use the variables we have provided and the loc method to create separate DataFrames for each city on the travel route.

Hint: You will start and end the route in the same city, so the vacation_start and vacation_end DataFrames will be the same city.

10. In Step 6, use the to_numpy() function and list indexing to write code to retrieve the latitude-longitude pairs as tuples from each city DataFrame.

11. In Step 7, use the gmaps documentation (Links to an external site.) to create a directions layer map using the variables from Step 6, where the starting and ending city are the same city, the waypoints are the three other cities, and the travel_mode is either "DRIVING", "BICYCLING", or "WALKING".

12. Take a screenshot of your map from Step 7 and save it to the Vacation_Itinerary folder as WeatherPy_travel_map.png.

13. In Step 8, use the provided concat() function code snippet to combine the four separate city DataFrames into one DataFrame.

14. In Steps 9-11, refactor the code from Steps 2-4 to create a new marker layer map of the cities on the travel route.

15. Take a screenshot of your map and save it to the Vacation_Itinerary folder as WeatherPy_travel_map_markers.png.

