# Identifying Utility Outages Using Social Media:
Identifying utility outage events in the District of Columbia Metro Area

## Problem Statement: 
How can we identify utility outage events in the DC Metro Area by analyzing social-media streaming data?
(Elaborate)

## Executive Summary:
- Two sentences on EDA (Dereje) and Methodology (Sara)
We were able to obtain 18,000 tweets from January, July and October 2019 using the GetOldTweets3 API wrapper. 
- Two sentences on Feature Engineering and Visualization (Eric)
- Two sentences on Conclusions and Recommendations (Eric, Dereje, Sara)
We recommend that this model be scaled for production by connecting a database that pulls recent tweets in a set in the District of Columbia Metro Area 

## Project Directory (Eric):


- README.md
- Presentation.pdf
- data
 - clean
 - initial scrape
 - january
 - july
 - merged
 - ne bomb cyclone data top tweets
 - ne bomb cyclone data w:o location
 - spatial data
- data_collection
 - [Twitter Scraper (Eric's Credentials)]('../data_collection/twitter-eric.ipynb')
 - [Twitter Scraper (Sara's Credentials)]('../data_collection/twitter-sara.ipynb')
- EDA
- feature_engineering
- modeling
- tableau
- visualizations

## Data Dictionary:

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


## Links:

- [Presentation]('Presentation.pdf')
- [Tableau Dashboard]('https://public.tableau.com/views/GA_DSI_DC_PowerOutages_20200513/Dashboard?:display_count=y&publish=yes&:origin=viz_share_link')


## Sources and Tools

- [GetOldTweets3 Twitter API Wrapper]('https://pypi.org/project/GetOldTweets3/')
