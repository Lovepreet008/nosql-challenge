# nosql-challenge
MongoDB

Use no sql method to load the csv and json files. 
Extract the files as per needed, convert into dataframe. 
Display dataframes. 





Table of content:
In setup_starter-
Create instance of Mongoclient
Display databases created
Assign database ('uk_food')
Review Collection and assign it to variable ('establishments')
Add new query using insert_one
update one of the field
Find and delete the dictionaries with particular field in it.
Change the data types of lattitude and longitude fields to decimal type using update_many command
Change the data type of 'Ratingvalue' field to integer type in all the entries. 
Verify if the dataypes are changed and per requirement.


In Analysis starter-
Analyse the json file and get the result with hygine score equal to 20 using command: find(query) 
Convert into dataframe and display it.
Find the establishments with London as the Local Authority and has a RatingValue greater than or equal to 4 using ('$regex')
Convert above results into dataframe and display it.
Find top 5 establishments with 'RatingValue' is 5 and lowest hygiene score nearest to 'Penang Flavous' restaurants.
  Use: results=list(establishments.find(query).sort(*sort).limit(limit))

Convert results into dataframe and display it.

Create a pipeline to match hygiene score of 0 and group by 'LocalAuthorityName' and sort by highest matches to lowest
Use:pipeline = [match_query, group_query, sort_values]
results = list(establishments.aggregate(pipeline))

Create a dataframe from above results and diplay it. 





Installation:
Used below comamnd in command line to import json file:

mongoimport --type json -d uk_food -c establishments --drop --jsonArray "Resources/establishments.json"

Used following libraries:
from pymongo import MongoClient
from pprint import pprint
import pandas as pd

Usage:
This help us understand and learn that we can extract json or csv files without using SQL and process them in similar way using MongoDb which is faster to process the data. 


Contributors:
Myself and big thanks to instructors.


