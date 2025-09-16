Air Quality Bristol API ETL & Visualization Project

A Python-based ETL pipeline that extracts air quality monitoring data from the official Bristol City Council API, processes and transforms the data, and loads the results into a PostgreSQL database using Apache Spark. The project also includes data normalization, geospatial coordinate handling, and visualization of monitoring locations across the city of Bristol.

Project Overview

This project demonstrates a complete data engineering and analytics workflow:

Extract: Data is collected from an online public API in GeoJSON format.

Transform:

Geospatial data is processed using GeoPandas.

Coordinates are normalized using MinMaxScaler.

Cleaned and transformed data is stored in both CSV and PostgreSQL database formats.

Load: The processed data is loaded into a PostgreSQL database via Apache Spark.

Visualize: Monitor site locations are visualized using Matplotlib on a normalized coordinate grid.

Technologies Used

Python 3.x

GeoPandas

Pandas

Scikit-learn

Matplotlib

Apache Spark (PySpark)

PostgreSQL

JDBC Connector

Shapely

Data Source

Source: Bristol City Council Air Quality API

Format: GeoJSON containing monitoring station data for Bristol City.

Project Workflow

API Call: Fetches live air quality data in GeoJSON format.

Read & Parse GeoJSON: Loads data into a GeoPandas DataFrame.

Coordinate Normalization: Scales longitude and latitude values between 0 and 1.

Data Transformation:

Adds normalized coordinates.

Updates geometry points.

Selects and renames relevant columns.

Export to CSV: Saves the transformed dataset.

Load into PostgreSQL via Apache Spark: Ingests final data into a database table.

Visualization: Plots normalized monitoring locations on a scatter plot.

Summary Statistics: Counts unique monitoring locations in the dataset.

Example Visualization

A scatter plot showing the distribution of air quality monitoring stations in Bristol, using normalized coordinate values.

How to Run

Install required Python libraries:

bash
Copy
Edit
pip install pandas geopandas scikit-learn matplotlib pyspark psycopg2-binary
Set up your PostgreSQL database and update the connection credentials in the script.

Run the Python script to execute the complete ETL pipeline and generate the visual output.

Key Skills Demonstrated

API Integration & Data Extraction

GeoJSON Data Handling

Geospatial Data Normalization

Apache Spark Data Processing

PostgreSQL Data Ingestion via JDBC

Data Visualization

End-to-End ETL Workflow

