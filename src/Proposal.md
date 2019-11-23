Proposal- Vancouver Crime Tracker
================
Chimaobi Amadi, Elliott Ribner, Shivam Verma, Xugang Zhong(Kirk)
22/11/2019

## Motivation and Purpose

-----

## Description of the Data

-----

The dataset is obtained from the [Vancouver Police Department (VPD)
website](https://geodash.vpd.ca/opendata/). It is based on the VPD
Records Management System and contains information about the type of
crime, nearest block, nearest neighborhood and date & time of the crime.
The data contains information from the 1st of January 2003 to the 31st
of October 2019. VPD aims to provide this data for the public interest,
to enhance awareness & maintain transparency about crimes in Vancouver.
Please note that the dataset does not include all the crimes because of
privacy & investigative reasons. Location information in the data was
offset so that no association with a specific person or property can be
made.

### Variable Description

| S No. | Variable       | Description                                  | Insight                                                                                                                                                                                                                                                                                                   |
| ----- | -------------- | -------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1     | TYPE           | Type of crime reported                       | The most common type of crime is `Theft from Vehicle`, `Mischief` and `Break and Enter Residential/Other`                                                                                                                                                                                                 |
| 2     | YEAR           | Year of crime reported                       | Number of crime occurrences reduced from 2003 to 2011 after which it started increasing. In 2018 the number of crimes was the same as in 2007                                                                                                                                                             |
| 3     | MONTH          | Month of crime reported                      | There is no significant difference in the number of crimes by month                                                                                                                                                                                                                                       |
| 4     | DAY            | Day of the month when the crime was reported | There is no significant difference in the number of crimes by day of month                                                                                                                                                                                                                                |
| 5     | HOUR           | Hour of crime reported                       | Most of the crimes happen between 5 PM and midnight. Past midnight there are fewer occurrences                                                                                                                                                                                                            |
| 6     | NEIGHBOURHOOD  | Neighbourhood of crime reported              | The data is for 24 neighborhoods in Vancouver. 10.42% of the crimes had no neighborhood associated with it. Even though the neighbourhood is missing for some records, the crime did happen. Therefore, neither imputing the data nor excluding those records as it describes other relevant information. |
| 7     | X              | X-coordinate of the location                 | Longitude                                                                                                                                                                                                                                                                                                 |
| 8     | Y              | Y-coordinate of the location                 | Latitude                                                                                                                                                                                                                                                                                                  |
| 9     | HUNDRED\_BLOCK | Generalized location of Crime Activity       | Not using                                                                                                                                                                                                                                                                                                 |
| 10    | MINUTE         | Hour of crime reported                       | Not using                                                                                                                                                                                                                                                                                                 |

## Research Questions and Usage Scenarios

-----

Peter and his family plans to relocate to Canada. As a result of the
favourable weather condition in Vancouver, they decide to settle in
Vancouver. Their first goal is to find accommodation: renting and
eventually owning a house in a safe neighbourhood, as well as safety for
their kids especially at school. The family does not know anyone in
Vancouver and relies on a reliable source of information regarding the
crime situation and trend in each of the neighbourhoods in Vancouver.

There are many people like Peter and his family; and to help solve their
problem, we plan on creating an interactive app that has the capability
of displaying crime information at a glance. The secondary motivation
for this app is answer general crime trends in Vancouver and create
awareness about crime rates per neighbourhood and need for drastic
intervention.

Using the dataset provided by the Vancouver Police Department (VPD), we
will build an interactive dashboard with the historic crime situation in
the city from 2003 to 2019. There are 3 filters provided in the
dashboard which includes the neighborhood, type of crime and the period
in years. The filter option streamlines the visualization and produces
charts that answer the questions.

The filtered data is molded to show the crime occurrences by
Month-of-Year (*Chart 1*) & Time-of-Day (*Chart 2*) to help him
understand the behavior of crimes around the city. In addition to this,
he can look at the trend of crime rate by year (*Chart 3*) and get to
know the composition of crimes (*Chart 4*) as
well.

-----

## Sketch of the Application

-----

## ![Sketch](https://raw.githubusercontent.com/vermashivam679/DSCI_532_Group114_SKEC/master/Img/sketch.png "Crime Information by Vancouver Neighbourhood")

### App Desciription

-----

  - We will have interactive visualizations of the VPD dataset described
    above.
  - The sketch above gives a glimpse of how the data will be visualized.
  - We will have three selectors (described below) that will allow us to
    filter the data that is represented in the five visualizations
    above.
  - The neighbourhood selector will allow us to filter by neighbourhood,
    crimes only in that neighbourhood will show up. We can’t colour or
    mark neighbourhoods on map because the variable latitude & longitude
    is for a particular crime scene & in the dataset there is a
    categorical variable: neighbourhood and linking it on the map would
    be difficult. But we can colour code type of crime.
  - We will have a type of crime selector that will filter the data set
    and the data visualizations by crime type, if no crime type is
    selected we will show all crime types.
  - The slider for selecting year is given because old data may be less
    relevant, so we can let the user decide the time period that is most
    relevant to them.
  - A histogram of crime by month will show the monthly crime patterns.
  - A histogram of crime by hour will show the patterns of crime
    throughout the day.
  - A map of Vancouver will be used to show crime trends by location.
    Different colors will be applied to different regions of the map to
    denote high and low crime areas.
  - A line chart will show the pattern of crime over the years,
    normalized for population change.
  - Lastly a pie chart will be used to show what percentage of the total
    crimes any particular type of crime represents.