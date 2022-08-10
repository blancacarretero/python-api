# Python Weather APIs 	:cloud_with_rain:

## Background

Whether financial, political, or social&mdash;data's true power rests in its ability to answer questions definitively. Python requests, APIs, and JSON may answer a fundamental question: "What's the weather like as we approach the equator?"

<img src="https://cdn.ioos.noaa.gov/attachments/2018/09/GOES-Florence_Isaac_Helene_web-banner.jpg" width="1000">


## Part 1: WeatherPy

Created a Python script to visualize the weather of 500+ cities of varying distance from the equator using a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and problem-solving skills to create a representative model of weather across cities.

#### I. Created a series of scatter plots to showcase the following relationships:

<b>Temperature (F) vs. Latitude</b>

<img src="https://github.com/blancacarretero/python-api/blob/main/images/latitude_vs_temperature.png?raw=true" width="350" title="Temperature vs. Latitude">
-  As expected, temperatures across cities get warmer are you get closer to the ecuator. Similarly, temperatures get colder as you move away from the ecuator in both northern and southern hemispheres.

&nbsp;
  
<b>Humidity (%) vs. Latitude</b>

<img src="https://github.com/blancacarretero/python-api/blob/main/images/latitude_vs_humidity.png?raw=true" width="350" title="Humidity vs. Latitude">
-  For the most part, humidity stays in at higher levels closer to the ecuator. 

&nbsp;

<b>Cloudiness (%) vs. Latitude</b>

<img src="https://github.com/blancacarretero/python-api/blob/main/images/latitude_vs_cloudiness.png?raw=true" width="350" title="Cloudiness vs. Latitude">
-  Cloudiness is mostly at a 100% closer to the ecuator.

&nbsp;

<b>Wind Speed (mph) vs. Latitude</b>

<img src="https://github.com/blancacarretero/python-api/blob/main/images/latitude_vs_wind_speed.png?raw=true" width="350" title="Wind Speed vs. Latitude">
-  Wind speed gets lower as you move away from the ecuator.

&nbsp;

#### II. Computed the linear regression for each relationship. Separated the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

### Part 2: VacationPy

Worked with weather data to plan future vacations. Used Jupyter-gmaps and the Google Places API.

#### I. Created a heat map that displays the humidity for every city from Part 1:

<img src="https://github.com/blancacarretero/python-api/blob/main/images/humidity_heatmap.png?raw=true" width="900" title="humidity heatmap">
  

#### II. Narrowed down the DataFrame to find ideal weather conditions:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Droped any rows that don't satisfy all three conditions.
 
  
#### III. Used Google Places API to find the first hotel for each city located within 5,000 meters of coordinates.

<img src="https://github.com/blancacarretero/python-api/blob/main/images/locations_and_hotels.png?raw=true" width="500" title="ideal weather conditions">

#### IV. Plotted the hotels on top of the humidity heatmap, with each pin containing the **Hotel Name**, **City**, and **Country**:

<img src="https://github.com/blancacarretero/python-api/blob/main/images/hotel_data_heatmap.png?raw=true" width="900" title="hotel info">
