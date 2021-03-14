# World_Weather_Analysis

## Overview
The World Weather Analysis provides a good scenario not only to pratice function such as "random", "enumerate", "requests", ".loc", "iterrows","to_numpy" but also to use "Weather Map API","Google's nearby API",and "gmaps." In the challenge, it required to generate three scripts, export two csv files, and implement several gmaps with markers.

## Weather Database
1.Create a city list. First, use random.uniform function to create 2000 sets of random latitude and longitude combinations. Then, use nearest_city function which will look for the city near the coordinate to generate a city list.

2.Create a list of dictionaries to include weather information. Look up every city in city list by using Weather Map API. Retrieve every city's weather information in JSON format by using requests function. Then, convert JSON information into assigned variables and append every city's weather information into the list of dictionaries. 

3.Convert the list of dictionaries into a Pandas DataFrame and export the data into a CSV file, named WeatherPy_Database.csv

## Vacation Search
1.Use input statements' to create Max and Min temperature criteria and use .loc function to filter out cities fufill the temperature criteria in Weather Database created previously. Drop null columns and convert the selected data into a new DataFrame, clean_df.

2.Copy "City", "Country", "Max Temp", "Current Description", "Lat", "Lng" from clean_df and create a new DataFrame, name hotel_df. Additioanlly, add a new column, Hotel Name.

3.Apply Google's nearby API to search nearby hotel around the city in hotel_df by using requests function. After retrieving hotel JSON format, save hotel information into Hotel Name column in DataFrame by .loc function.

4.Export the result into a CSV file, named WeatherPy_vacation.csv after droping na row.

5.Display the result by applying gmaps function. Add marker to show information of city name, the country code, the weather description and maximum temperature for each hotel. 

## Vacation Itinerary
1.Create DataFrame by using .loc function after selecting 4 cities form Vacation Search result.

2.Use to_numpy function to retrieve latitude-longitude from DataFrame.

3.Display the route by applying Directions API by using latitude-longitude previously.

4.Display the selected cities makers to information of city name, the country code, the weather description and maximum temperature for each hotel by applying gmaps function.
