# Identifying Utility Outages Using Social Media:
Identifying utility outage events in the District of Columbia Metro Area

## Problem Statement: 
How can we identify utility outage events in the DC Metro Area by analyzing social-media streaming data?
(Elaborate)

## Executive Summary:
This project is an effort to spatially and temporally understand social media surrounding power outage events. We assess Twitter to be the most viable means of analyzing power outage events using social media. We couple sentiment analysis with spatial and temporal analaysis in an interactive dashboard to provide insight into power outage events. Our methods, findings, and recommendations are detailed below. 

- Two sentences on EDA (Dereje) and Methodology (Sara)
We were able to obtain the data by using a 

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

## Project Directory (Eric):

data
    --clean
    --initial test scrape
    --january
    --july
    --merged
    --ne bomb cyclone data top tweets
    --ne bomb cyclone data w:o location
    --spactial data
data_collection
EDA
feature_engineering
modeling
tableau
visualizations
README.md


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

- [Presentation]('https://docs.google.com/presentation/d/128lOfsY1CZh6_4jX0TtL15vsUzMp7NTwL2Twcxc9xho/edit')

<iframe seamless frameborder="0" src="https://public.tableau.com/views/GA_DSI_DC_PowerOutages_20200513/Dashboard?:display_count=y&publish=yes&:origin=viz_share_link" width = '650' height = '450' scrolling='yes' ></iframe>    

