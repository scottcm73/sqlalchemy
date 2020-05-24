# Surfs Up!

## Step 1 - Climate Analysis and Exploration

Python and SQLAlchemy were used to do basic climate analysis and data exploration a climate database. All of the following analysis was completed using SQLAlchemy ORM queries, Pandas, and Matplotlib.

* The starter notebook (climate_starter.ipynb) and [hawaii.sqlite](Resources/hawaii.sqlite) files were utilized to complete the climate analysis and data exploration.

Based on an arbitrary start date and end date for your trip was chosen to be about 3-15 days total.

SQLAlchemy `create_engine` connects to the sqlite database.

* SQLAlchemy `automap_base()` makes the tables into classes and saves a reference to those classes called `Station` and `Measurement`.

### Precipitation Analysis

* A query retrieves the last 12 months of precipitation data, the `date` and `prcp` values.

* Loading the query results into a dataframe was done with Pandas and the index was set to the date column.

* The DataFrame values were sorted by `date`.

* Results were plotted using the DataFrame `plot` method.

* Pandas.description() printed the summary statistics for the precipitation data.

### Station Analysis

* One query calculates the total number of stations.

* Another query finds the most active stations.

  * The stations and observation counts are listed in descending order.

## Step 2 - Climate App

After completing the initial analysis, a Flask API was created based on the queries.


* Joining the station and measurement tables was required for some of the analysis queries.

* Flask `jsonify` converted the API data into a valid JSON response object.

