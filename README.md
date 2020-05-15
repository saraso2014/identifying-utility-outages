# Identifying Utility Outages Using Social Media:
Identifying utility outage events in the District of Columbia Metro Area

## Problem Statement: 
How can we identify utility outage events in the DC Metro Area by analyzing social-media streaming data?
(Elaborate)

## Executive Summary:
- Two sentences on EDA (Dereje) and Methodology (Sara)
- Two sentences on Feature Engineering and Visualization (Eric)
- Two sentences on Conclusions and Recommendations (Eric, Dereje, Sara)

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