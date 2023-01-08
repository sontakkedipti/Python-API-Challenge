Python API - What's the Weather Like?

Background
Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. I used Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

Equator

Part I - WeatherPy
In part-I, a Python script was created to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, I utilized a simple Python library, the OpenWeatherMap API, to create a representative model of weather across world cities.

I created a series of scatter plots to showcase the following relationships:

Temperature (F) vs. Latitude
Humidity (%) vs. Latitude
Cloudiness (%) vs. Latitude
Wind Speed (mph) vs. Latitude
Note: a written analysis is provided after each plot.

Then a linear regression analysis was performed to determined each relationship, only this time, separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

Northern Hemisphere - Temperature (F) vs. Latitude
Southern Hemisphere - Temperature (F) vs. Latitude
Northern Hemisphere - Humidity (%) vs. Latitude
Southern Hemisphere - Humidity (%) vs. Latitude
Northern Hemisphere - Cloudiness (%) vs. Latitude
Southern Hemisphere - Cloudiness (%) vs. Latitude
Northern Hemisphere - Wind Speed (mph) vs. Latitude
Southern Hemisphere - Wind Speed (mph) vs. Latitude
After each pair of plots, an explanation of what the linear regression is modeling, such as any relationships or associations, and any other analysis.

Part II - VacationPy
In part-II, the weather data outputted in part-I was used to plan future vacations using a jupyter-gmaps and the Google Places API.

A heat map displaying the humidity for every city from the part-I was created.

heatmap

The DataFrame to find ideal weather conditions was narrowed down. For example:

A max temperature lower than 80 degrees but higher than 70.

Wind speed less than 10 mph.

Zero cloudiness.

The Google Places API was used to find the first hotel for each city located within 5000 meters of the coordinates.

The hotels were plotted on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.

hotel map
