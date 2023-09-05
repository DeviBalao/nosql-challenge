# nosql-challenge
The Food Standards Agency evaluates various establishments across the country, and gives them a food hygiene rating. The challenge is to evaluate some of the ratings data in order to help the journalists and food critics of a food magazine decide where to focus future articles.

There are **2** files:
1. NoSQL_setup:

This file handles the database setup.  Data is imported from the input JSON file available in Resources folder using the following command:

        mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json"

The details of a new restaurant are added to the database, as mentioned in the Instructions. Datatype of latitude, longitude  are converted to Double from String. Datatype of RatingValues is changed to Integer from String.

2. NoSQL_analysis:

Analysis is done to answer few specific questions. The results are stored and displayed as DataFrames.