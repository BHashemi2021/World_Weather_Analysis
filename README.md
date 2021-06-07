# World Weather Analysis

#### Background
PlanMyTrip app is popular and beta testers love it too. And, as with any new product, they have recommended a few changes to take the app to the next level. Specifically, they recommend adding the weather description to the weather data. Then the beta testers will use input statements to filter the data for their weather preferences, which will be used to identify potential travel destinations and nearby hotels. From the list of potential travel destinations, the beta tester will choose four cities to create a travel itinerary. To make those changes to th app we are going to use the Google Maps Directions API, and create the capabilities to the app that users could use to draw routes between the cities of interest as well as a marker layer map.


#### Purpose: 
PlanMyTrip will use the data to recommend ideal hotels based on clients' weather preferences.
  1- Retrieve Weather Data
  2- Create a Customer Travel Destinations Map
  3- Create a Travel Itinerary Map

## 1: Retrieving the Weather Data
  
Bt generating a set of 2,000 random latitudes and longitudes we were able to get the nearest city to any place of interest. his was done by importing citipy module into jupyter notebook.

Then we registered with [OpenWeatherMap website](https://openweathermap.org/) to get an AIP for the calls we will make to getch information about different places.
We could get the following information from the API calls:

    * Latitude and longitude
    * Maximum temperature
    * Percent humidity
    * Percent cloudiness
    * Wind speed
    * Weather description (for example, clouds, fog, light rain, clear sky)

We then addded the data to a new DataFrame and expoted the data in to WeatherPy_vacation.csv file.

## 2- Creating a Customer Travel Destinations Map
Using the starter jupyter notebook, Vacation_Search.ipynb, we first imported the needed dependencies and API keys both from OpenWeatherMap database and [Google Cloud Platform](https://cloud.google.com/).

Having retrieved the latitude and longitude for 2000 cities and removing the epty rows we made another DataFrame and saved the results into WeatherPy_Database.csv.

Refactoring our previous marker layer map code we created a marker layer map that will have pop-up markers for each city on the map.

![WeatherPy_vacation_map.png]<img src="https://github.com/BHashemi2021/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png" width="750" height="422">


## 3: Creating a Travel Itinerary Map 
Using the Google Directions API we created a travel itinerary that shows the route between four cities chosen from the customer’s possible travel destinations. Then, we created a marker layer map with a pop-up marker for each city on the itinerary.

Refactoring the code through an array of steps we finally created a new marker layer map of the cities on the travel route.

![WeatherPy_travel_map_markers.png](https://github.com/BHashemi2021/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map_markers.png) 

The round-trip travel map between four stops is provided below:

![WeatherPy_travel_map.png](https://github.com/BHashemi2021/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map%20.png)

