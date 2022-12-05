# Surfs Up Analysis

## Overview
While on vacation in Hawaii last year, the analyst discovered and newfound love for surfing.  This passion impacted them so much, that the analyst decided to create a long term plan to open a "surf and shake" shop on Oahu that serves surfboards and ice cream to locals and tourists.  

To make this dream a reality, the analyst got in contact with an investor, W. Avy, to get his input and, hopefully, his investment.  W. Avy seemed extremely intrigued by the opportunity, but his main concern is weather.  To earn W. Avy's partnership, the analyst must provide an analysis of local weather using Python and a SQLite database to prove that this is a sound investment, and that their dreams literally don't get rained away.

## Results
W. Avy tasked the analyst to analyze the temperature data for months of June and December.  To do this, the analyst used a series of queries to collect weather data from a SQLite database and turn that data into a python dataframe to then provide the summary that W. Avy is looking for.  The queries that the analyst used to extract the data from the SQLite database are below:

June Temperatures Query:

!["june_temps_code.png"](https://github.com/hillmanj1995/surfs_up/blob/main/Outputs/june_temps_code.png)

December Temperatures Query:

!["dec_temps_code.png"](https://github.com/hillmanj1995/surfs_up/blob/main/Outputs/dec_temps_code.png)

The data that was extracted using the queries was then turned into dataframes and summarized using a .describe() command.  The resulting dataframes summaries are shown below:

June Temperature Summary:

!["june_temps_description.png"](https://github.com/hillmanj1995/surfs_up/blob/main/Outputs/june_temps_description.png)

December Temperature Summary:

!["dec_temps_description.png"](https://github.com/hillmanj1995/surfs_up/blob/main/Outputs/dec_temps_description.png)

The comparison of the data summaries shows a couple minor differences between the June and December:

- The count of temperatures for December is roughly 200 less than that of June (1517 vs. 1700).
    - The difference in datapoints should not make a noticeable impact on the results as multiple data readings are taken from the station each day.

- There is a difference of almost 4 degrees between the June and December average temperatures (74.94F vs. 71.04).
    - A difference of 4 degrees is likely negligible from a personal comfort standpoint.

- The minimum temperature for December is 8 degrees less than that of June (56F vs. 64F).
    - Minimum temperatures occur late at night/early in the morning when the sun is down and it cools down, likely before or after business hours. While the data does not specify the time that the reading was taken, the temperatures of 64F (June) and 56F (December) should be treated as outliers and will likely not impact business.

## Summary
From the analysis of the June and December temperatures, the data summaries show that, temperature-wise, Oahu is a great location to open a surf and ice cream shop.  The average temperatures in the summer and winter are within 5 degrees of each other (~75F for June, and ~71F for December), and the minimum temperatures are either outlier days or reading taken after the sun goes down.

An important piece of data to factor into the weather analysis is precipitation.  Rainfall has a significant ability to impact a consumer's behavior to do outdoor activities (surfing) or indulge in warm weather treats (ice cream).  The analyst performed queries and summaries similar to the temperature analysis to provide information on the levels of rainfall for Oahu.  The code used for the queries is found below:

June Precipitation Query:

!["june_precip_code.png"](https://github.com/hillmanj1995/surfs_up/blob/main/Outputs/june_precip_code.png)

December Precipitation Query:

!["dec_precip_code.png"](https://github.com/hillmanj1995/surfs_up/blob/main/Outputs/dec_precip_code.png)

The queries were turned into dataframes to get a statistics summary.  Those summaries are below:

June Precipitation Summary:

!["june_precip_description.png"](https://github.com/hillmanj1995/surfs_up/blob/main/Outputs/june_precip_description.png)

December Precipitation Summary:

!["dec_precip_description.png"](https://github.com/hillmanj1995/surfs_up/blob/main/Outputs/dec_precip_description.png)

The summaries of the precipitation for June and December show the average level of rainfall for December is almost twice that of June (~0.22" for December vs. ~0.14" for June).  That being said, a difference of 0.1" is not likely to impact rainy day sales performance/consumer turnout.  It is worth noting that the max level of rainfall for December is noticeably higher than that of June (6.42" for December vs. 4.43" for June).  While max and min values are usually outliers, it is something the analyst and W. Avy should be prepared for in case they get a particularly rainy day.

Based on the temperature and precipitation summaries that the analyst provided, W. Avy's concerns on the temperature and precipitation should be put to rest.  If the analyst was to analyze data even further, it would be worthwhile to look at the consumer data of other surf and ice cream shops on Oahu, and see if there is any correlation between sales data, number of consumers, and weather data.  Most consumers tend to stay inside on a rainy day, so it would be informative to analyze sales data on sunny vs. rainy days, and do an analysis of how frequently it rains.  W. Avy and the analyst can use this information to get a better idea on if they would need to diversify their business model to accommodate for rainy day activities/goods, should they see a lack of sales in surfboards and ice cream during rainy periods.