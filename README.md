# Price-Crawler--Tracking-Price-Inflation
This project was finished in three weeks while enrolled in the Insight Data Engineering Program (New York, 20B Session). This research aims to determine inflation rates from the ground up. Thus, the price of products and services purchased online will be used to calculate the rate of inflation.

In order to determine inflation rates for this project, I created a pipleine that uses petabytes of online page data from the Common Crawl, an archive of web page content. The findings can be applied to improve investing methods or help firms choose how much to charge for their goods. The inflation rate for 2019 has been calculated using internet laptop costs ($500–$800), and it is found to be 4.8%, more than double the yearly inflation rate of 2.3%.

Pipeline information 
1 - Utilizing HTTP header information from indexed WARC Files, AWS Athena
2- Scan 100 GB of data rather than PB.
3 - Keys to interesting web pages kept in parquet files on S3, with distributed processing over O(10 GB) of data per task using Parquet + WARC input to Spark
4 - Utilizing Pandas in Python to clean, filter, and aggregate Product and Price tables
5 - Utilizing Dash to plot and monitor price trends

Languages and technologies used 
Bash
Python 3.7
Pandas


Spark
AWS Athena
Dash/Plotly
Third-Party Libraries

AWS CLI

Contents of Files in the repo-  

Athena-  instruction set on how to use AWS Athena to query typical crawl data.

Spark - Includes the main.py spark script, which is used to initiate spark jobs using the results of an athena query.

Spark submit ./spark/main.py -in walmart_laptops_2018 -o walmart_parquet_2018
./pandas/contains python script to clean the output from spark and provide csv file to dashapp/app.py

python3 pandas/cleaner.py
./dashapp/ contains a dash app to visualize trends in online prices in laptops across time

python3 dashapp/price_tracker.py
