# World Weather Analysis

#### Background
Jack loves the PlanMyTrip app. Beta testers love it too. And, as with any new product, they’ve recommended a few changes to take the app to the next level. Specifically, they recommend adding the weather description to the weather data you’ve already retrieved in this module. Then, you'll have the beta testers use input statements to filter the data for their weather preferences, which will be used to identify potential travel destinations and nearby hotels. From the list of potential travel destinations, the beta tester will choose four cities to create a travel itinerary. Finally, using the Google Maps Directions API, you will create a travel route between the four cities as well as a marker layer map.


#### Purpose: 
PlanMyTrip will use the data to recommend ideal hotels based on clients' weather preferences.
  1- Retrieve Weather Data
  2- Create a Customer Travel Destinations Map
  3- Create a Travel Itinerary Map



## 1: Retrieving the Weather Data
  
1- Generate a set of 2,000 random latitudes and longitudes.

2- Get the nearest city using the citipy module.

3- Perform an API call with the OpenWeatherMap.

4- Retrieve the following information from the API call:

    Latitude and longitude
    Maximum temperature
    Percent humidity
    Percent cloudiness
    Wind speed
    Weather description (for example, clouds, fog, light rain, clear sky)

Add the data to a new DataFrame.

In Steps 8a-b, create an output file to store the hotel_df DataFrame as WeatherPy_vacation.csv in the Vacation_Search folder.


## 2- Create a Customer Travel Destinations Map
Create a folder called Vacation_Search.

Download the Vacation_Search_starter_code.ipynb file into your Vacation_Search folder, and rename it Vacation_Search.ipynb.

In the Vacation_Search.ipynb file, make sure the dependencies and API keys are imported correctly.

Use the instructions below to add code where indicated by the numbered-step comments in the starter code file.

In Step 1, import the WeatherPy_Database.csv file from your Weather_Database folder from Deliverable 1 as a DataFrame.

In Step 2, write two input statements that prompt the user to enter their minimum and maximum temperature criteria for their vacation.

In Step 3, use the loc method to filter the city_data_df DataFrame for temperature criteria collected in Step 2, then create a new DataFrame.

In Steps 4a-b, determine if there are any empty rows, then drop them if necessary and create a new DataFrame.

In Steps 5a-b, use the provided code to create a new DataFrame, hotel_df, that will hold the hotel names from the hotel search in Steps 6a-6f.

In Step 6a, we have supplied the search parameters, which are the same as in this module, that you’ll need to use to search for a hotel for each city in Steps 6b-f.

In Steps 6b-f, iterate through the hotel_df DataFrame, retrieve the latitude and longitude of each city to find the nearest hotel based on the search parameters from Step 6a, then add the hotel name to the hotel_df DataFrame. If a hotel isn't found, skip to the next city.

In Step 7, drop any rows in the hotel_df DataFrame where a hotel name is not found.

In Steps 8a-b, create an output file to store the hotel_df DataFrame as WeatherPy_vacation.csv in the Vacation_Search folder.

In Step 9, add the city name, the country code, the weather description, and the maximum temperature for the city to the info_box_template format template we have provided.

In Step 10a, use the provided list comprehension code to retrieve the city data from each row, which will then be added to the formatting template and saved in the hotel_info list.

In Step 10b, use the provided code snippet to retrieve the latitude and longitude from each row and store them in a new DataFrame.

In Steps 11a-b, refactor your previous marker layer map code to create a marker layer map that will have pop-up markers for each city on the map.

Take a screenshot of your map and save it to the Vacation_Search folder as WeatherPy_vacation_map.png.


## 3: Create a Travel Itinerary Map 
Use the Google Directions API to create a travel itinerary that shows the route between four cities chosen from the customer’s possible travel destinations. Then, create a marker layer map with a pop-up marker for each city on the itinerary.

1- Enable the "Directions API" in your Google account for your API key.

2- Create a folder called Vacation_Itinerary.

Download the Vacation_Itinerary_starter_code.ipynb file into your Vacation_Itinerary folder and rename it Vacation_Itinerary.ipynb.

In the Vacation_Itinerary.ipynb file, make sure the dependencies and API keys are imported.

Use the instructions below to add code where indicated by the numbered-step comments in the starter code file.

In Step 1, import the WeatherPy_vacation.csv file from your Vacation_Search folder from Deliverable 2 as a DataFrame.

In Steps 2-4, copy or refactor the code from Steps 11a-b of Deliverable 2 to create a marker layer map of the vacation search results.

From the vacation search map, choose four cities that a customer might want to visit. They should be close together and in the same country.

You may have to refine your search with different weather criteria to get cities that are close together.
In Step 5, use the variables we have provided and the loc method to create separate DataFrames for each city on the travel route.

Hint: You will start and end the route in the same city, so the vacation_start and vacation_end DataFrames will be the same city.

In Step 6, use the to_numpy() function and list indexing to write code to retrieve the latitude-longitude pairs as tuples from each city DataFrame.
If you’d like a hint on using the to_numpy() function with list indexing, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.

In Step 7, use the gmaps documentation (Links to an external site.) to create a directions layer map using the variables from Step 6, where the starting and ending city are the same city, the waypoints are the three other cities, and the travel_mode is either "DRIVING", "BICYCLING", or "WALKING".

Take a screenshot of your map from Step 7 and save it to the Vacation_Itinerary folder as WeatherPy_travel_map.png.

In Step 8, use the provided concat() function code snippet to combine the four separate city DataFrames into one DataFrame.
If you’d like a hint on combining DataFrames into one DataFrame using the concat() function, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.

In Steps 9-11, refactor the code from Steps 2-4 to create a new marker layer map of the cities on the travel route.

Take a screenshot of your map and save it to the Vacation_Itinerary folder as WeatherPy_travel_map_markers.png.
