# Identifying Utility Outages Using Social Media:
Identifying utility outage events in the District of Columbia Metro Area

## Problem Statement: 
How can we identify utility outage events in the DC Metro Area by analyzing social-media streaming data?
(Elaborate)

## Executive Summary:
- Two sentences on EDA (Dereje) and Methodology (Sara)
We were able to obtain the data by using a 
- Two sentences on Feature Engineering and Visualization (Eric)
- Two sentences on Conclusions and Recommendations (Eric, Dereje, Sara)

## Project Directory (Eric):


- README.md

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
 - [twitter Scraper (Sara's Credentials)]('../data_collection/twitter-sara.ipynb')
- EDA
- feature_engineering
- modeling
- tableau
- visualizations

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

- [Tableau Dashboard]('https://public.tableau.com/views/GA_DSI_DC_PowerOutages_20200513/Dashboard?:display_count=y&publish=yes&:origin=viz_share_link')

<iframe seamless frameborder="0" src="https://public.tableau.com/views/GA_DSI_DC_PowerOutages_20200513/Dashboard?:display_count=y&publish=yes&:origin=viz_share_link" width = '650' height = '450' scrolling='yes' ></iframe>    

## Sources / Tools

- [GetOldTweets3 Twitter API Wrapper]('https://pypi.org/project/GetOldTweets3/')
