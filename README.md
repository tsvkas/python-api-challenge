# Weather Analysis

The `WeatherPy` directory contains 2 Jupyter Source Files `WeatherPy.ipynb` and `VacationPy.ipynb` which request relevant data from 2 API providers **OpenWeatherMap** and **Geoapify** for over 500 cities within the desired coordinates, and a repo `output_data` which contains the output images generated from `WeatherPy.ipynb`. 

The two Jupyter Source Files utilize Pandas library to create DataFrame for each dataset. Matplotlib library was imported to create series of scatter plots based on different variables. Scipy and linregress were also imported to help with statistical computation and generate linear regresssion line for the data points. Citipy was imported to generate list of cities with the coordinates, hvplot was imported for interactive data visualization, and geoviews is imported to explore and visualize data geographically.

## WeatherPy

**Temperature vs. Latitude**
* In the Northern Hemisphere there is a considerable negative correlation -0.7677311259957496 between temperature and latitude. In the Southern Hemisphere, there is a significant positive correlation 0.7736297170006914 between temperature and latitude.
  
  ![image](https://github.com/tsvkas/python-api-challenge/blob/main/WeatherPy/output_data/temp-v-lat-1.png)

  ![image](https://github.com/tsvkas/python-api-challenge/blob/main/WeatherPy/output_data/temp-v-lat-2.png)

**Humidity vs. Latitude**
* Both Northern and Southern hemispheres have a very low positive correlation between himidity and latitude

  ![image](https://github.com/tsvkas/python-api-challenge/blob/main/WeatherPy/output_data/hum-v-lat-1.png)

  ![image](https://github.com/tsvkas/python-api-challenge/blob/main/WeatherPy/output_data/hum-v-lat-2.png)

**Cloudiness vs. Latitude**
* Here we can see a very weak correlation between cloudiness and latitude in both hemispheres

  ![image](https://github.com/tsvkas/python-api-challenge/blob/main/WeatherPy/output_data/clo-v-lat-1.png)

  ![image](https://github.com/tsvkas/python-api-challenge/blob/main/WeatherPy/output_data/clo-v-lat-2.png)

**Wind Speed vs. Latitude**
* There is a very weak postivie correlation between wind speed and latitude in the northern hemisphere (0.06019854786785686) and a negative one in the southern hemisphere (-0.17875756558069295)

  ![image](https://github.com/tsvkas/python-api-challenge/blob/main/WeatherPy/output_data/wind-v-lat-1.png)

  ![image](https://github.com/tsvkas/python-api-challenge/blob/main/WeatherPy/output_data/wind-v-lat-2.png)

## VacationPy

* Create `city map` that displays a point for every city in the `city_data_df` DataFrame using data in `output_data/cities.csv`. The size of the point is determined by the humidity level in each city.

  <img width="599" alt="image" src="https://github.com/tsvkas/python-api-challenge/blob/main/WeatherPy/output_data/vac1.png">

* Narrow down cities that fit the criteria and drop any results with null values, the criteria are listed below:
  1. temperature to be between 24 and 36 degrees
  2. the windspeed less than 6 m/s
  3. cloudiness less than 2

* Add the hotel name and the country as additional information in the hover message for each city in `hotel map`
  <img width="477" alt="image" src="https://github.com/tsvkas/python-api-challenge/blob/main/WeatherPy/output_data/vac2.png">

