# Identifying Utility Outages Using Social Media:

## Problem Statement: 

Uising social media, can we identify and analyze power outage events in the DC Metro Area? Utility Outage Management Systems have been rolling out new smart grid technologies to supplement traditional methods for detecting and reporting on power outages. However, the new technologies will not be completely rolled out until 2030. While this new technology is implemented, supplemental efforts will be needed to help identify and provide social context on power outages.

## Executive Summary:
This project is an effort to spatially and temporally understand social media surrounding power outage events. We assess Twitter to be the most viable means of analyzing power outage events using social media. We couple sentiment analysis with spatial and temporal analaysis in an interactive dashboard to provide insight into power outage events. Our methods, findings, and recommendations are detailed below. 

#### Data and Methodology:
We scraped and examined 18,000 tweets using the GetOldTweets3 API. We pulled these tweets from January, July and October 2019 by searching for tweets containing the phrase "power outage".

Techniques included Standard Exploratory Data Analysis (EDA). UTF-8 characters and emojis were removed, leaving only the text of tweets and several other metadata fields. See the EDA and Data Collection notebooks for furter details. The sampled data was not temporally consistent due the limitations of the API.

The most prominent issue of feature engineering was the lack of true geocoordinates, which hampered the ability to create a vialbe proof of concept. We generated synthetic geometries inside of the WMA (approximately 5500 sq miles), and joined these geometries to the 18,000 tweets. This issue can be mitigated with premium Twitter API access.

#### Our recommendations are as follows:
1. Purchase Premium Twitter API (Access starts at $100/month, up to $2,500/month)
	- Scrape twitter with given parameters for outages every X minutes
	- Connect Tableau dashboard to the the dynamic data, once pulled
2. Display the data dynamically on local Tableau instance or Tableau server: 
	- Tableau is dynamic, easy to use, and ubiquitous in terms of software solutions.
3. Automate this process with the Premium API and an Extract, Transform, Load (ETL) process:
	- Premium access will allow the script to run more frequently (near real-time).
	- Write the data to a database instead of a CSV.
	- Point the Tableau connection to that database instead of a CSV.
	- Publish the Tableau dashboard to the web.
    
#### Next steps of analysis include:
- Identifying true spatial clusters within data. This could provide insight into repeatedly problematic areas, ultimately better-serving customers.
- Refine sentiment analysis and consider larger query list for relevant terms related to power outage and investigate cosine similarity of these terms uising Word2Vec Python Library.
- Compare the data from this analysis to actual utility grid-outage data and investigate discrepencies.

## Project Directory:

## File Directory: 
- 01_data_collection
   - twitter-eric.ipynb   
- 02_eda
   - EDA-Client-Project-5.ipynb
   - EDA-for-Client-Project.ipynb
- 03_fearure_engineering
   - feature_engineering.ipynb
- 04_modeling
   - sentiment_analysis.ipynb
- 05_images
   - Image 5-15-20 at 5.26 PM.jpeg
- 06_slides
   - Analyzing Power Outages with Social Media.pdf
- data
   - clean
      - clean.csv
   - initial test scrape
      - outage-5k-tweets.csv
      - power outage-5k-tweets copy.csv
      - power outage-5k-tweets.csv
      - power outage-10k-tweets.csv
   - january
      - january-early_after_tweets.csv
      - january-end_before_tweets.csv
      - january-mid_during_tweets.csv
   - july
     - july-early_after_tweets.csv
     - july-end_before_tweets.csv
     - july-mid_during_tweets.csv
   - merged 
      - merged_data_unclean.csv
      - tweets_geom_unclean.csv
      - tweets_sa_unclean.csv
      - clean.ipynb
   - ne bomb cyclone data top tweets
      - ne_bomb_cyclone_boston_after_tweets.csv
      - ne_bomb_cyclone_boston_before_tweets copy.csv
      - ne_bomb_cyclone_boston_before_tweets.csv
      - ne_bomb_cyclone_boston_during_tweets.csv
   - ne bomb cyclone data w/o location
      - ne_bomb_cyclone_after_tweets.csv
      - ne_bomb_cyclone_before_tweets.csv
      - ne_bomb_cyclone_during_tweets.csv
   - spatial_data
      - 20_random_pts.csv
      - 20190109_tableau.csv
      - DC_Quadrants-shp.shp
      - random_pts.csv
      - tl_2017_us_cbsa.shp
      - wma_gpkg.gpkg
- Presentation.pdf
 


## Data Dictionary (Sara):

| Data        | Meaning                                   | Type    |
|-------------|-------------------------------------------|---------|
| Event       | Name of data pull \(primary\)             | object  |
| Stage       | Name of data pull \(secondary\)           | object  |
| Query Date  | Date from which query works backward      | object  |
| Query Term  | Term which query is pulled                | object  |
| Id          | Unique ID assigned per tweet              | int64   |
| Username    | Twitter handle                            | object  |
| Text        | Tweet text                                | object  |
| Date        | Datetime stamp tweet was posted           | object  |
| Hashtags    | Hashtags associated with tweet            | object  |
| Location    | Hidden geodata from tweet \(location ID\) | float64 |
| \_wkt\_geom |                                           |         |
| id          |                                           |         |
| xcoord      |                                           |         |
| ycoord      |                                           |         |
| Sentiment   |                                           |         |


## Links and Visuals (Eric, Dereje, Sara):

- [Presentation]('Presentation.pdf')
- [Tableau]('https://public.tableau.com/views/GA_DSI_DC_PowerOutages_20200513/Dashboard?:display_count=y&publish=yes&:origin=viz_share_link')

