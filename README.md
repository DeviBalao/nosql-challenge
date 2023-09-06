# nosql-challenge
The Food Standards Agency evaluates various establishments across the country, and gives them a food hygiene rating. The challenge is to evaluate some of the ratings data in order to help the journalists and food critics of a food magazine decide where to focus future articles.

Pre-requisites:
-
The following are required:

* pymongo - Run the following in the appropriate Conda environment: 

                conda install pymongo, or pip install pymongo.  

* MongoDB - To install on Windows, follow the instructions in the following link:
        
                https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-windows/

        Note: Installing it as a service is recommended.

* Mongo compass - This has UI to manage the Databases. Reccommended

                https://www.mongodb.com/products/tools/compass

mongosh - To install on Windows, follow the instructions in the following link:

                https://www.mongodb.com/docs/mongodb-shell/install/

        Make sure to add the path of mongosh.exe binary file to PATH environment variable.

* mongoimport -  To install on Windows, follow the instructions in the following link:

                https://www.mongodb.com/docs/database-tools/installation/installation-windows/

        Use MongoDB Command Line Database Tools Download from the list of available MSIs. Make sure to add the path of mongoimport.exe binary file to your PATH environment variable. Once done this allows to import json and csv files using mongoimport with the command line.
-------------------

There are **2** files for this challenge:
1. NoSQL_setup:

This file handles the database setup.  Data is imported from the input JSON file available in Resources folder using the following command:

        mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json"

The details of a new restaurant are added to the database, as mentioned in the Instructions. Datatype of latitude, longitude  are converted to Double from String. Datatype of RatingValues is changed to Integer from String.

2. NoSQL_analysis:

Analysis is done to answer few specific questions. The results are stored and displayed as DataFrames.