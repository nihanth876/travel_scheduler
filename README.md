# Travel Scheduler

The goal of the project "The Travel Scheduler" is to predict the list of locations within the city and create an efficient travel plan and schedule that reduces travel time and expenses. Several data mining techniques are employed in the development of this project, including the Distance matrix, the Traveling Salesman algorithm, and the KNN clustering tool. 

The user enters the name of the city as well as the locations of interest in that city. Once all the tourist places within the city are fetched, the places are filtered and predicted based on the reviews and ratings. The application will generate a CSV file with the list of locations and the scheduled time.


**Initial Setup:**

This project requires some API calls for which we require to generate API keys.Please follow this link for creating the 

https://developers.google.com/maps/documentation/javascript/get-api-key

After the generation of the API key , the below APIs should be activated

![image](https://media.github.iu.edu/user/20972/files/81b87d4f-3527-4b41-81a3-66fded4a3149)

The generated key should be placed in the api_key variable of the ipynb and py file

![image](https://media.github.iu.edu/user/20972/files/05ca94a2-bc8b-42ec-ae40-1de33601fcd2)


**Required packages:**

Make sure that the below packages are installed before running the code

import requests

import pandas

import numpy

import json

from bs4 import BeautifulSoup

import json

import requests

from urllib import request

from sklearn.neighbors import BallTree

from io import StringIO

import ortools


**Running the Code:**

The programs takes 2 inputs from the user

   1. City name
   2. Interested place in the City
   
The program runs and generates a final_schedule.csv file with list of places and time schedule

![image](https://media.github.iu.edu/user/20972/files/0bcc5d87-36d5-4e9c-81d6-8dd780a5b467)




**Dataset:**

We receive a huge JSON data from Google after the API call , however we are uploading the smaller and sample data files in the data folder for easy understanding.

city.json - This file contains information about all the tourist places in the city provided by the user.
https://maps.googleapis.com/maps/api/place/textsearch/json?query=san+diego+city+point+of+interest&language=en&key=


placedetails.json - This contains in detail information about the place. 
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJ2Vb0Z9pU2YARij7i4I-e9u8&key=


nearbysearch.json - This file contains information about nearby good rated shopping malls or resturants from the interested. - 
https://maps.googleapis.com/maps/api/place/nearbysearch/json?location=32.7360353,-117.1509849&radius=50000&type=shopping_mall&key=



datamatrix.json - Contains the distance information between 2 places.
https://maps.googleapis.com/maps/api/distancematrix/json?origins=32.7341479,-117.144553&destinations=32.7341479,-117.144553&key=

**Please append the generated API key at the end of the url to access it**.

for more information about above google APIs please visit below links.

Place search API - https://developers.google.com/maps/documentation/places/web-service/search

Place detail API - https://developers.google.com/maps/documentation/places/web-service/details

Distance Matrix API - https://developers.google.com/maps/documentation/distance-matrix/overview

Geocode API - https://developers.google.com/maps/documentation/geocoding/start

