# Proposal for Interactive Visualization Project

Title: Where things are economically going better in the US? Interactive map that shows, at a glance,
    the current economical status for each big Metropolitan Statistical Area in the United States

Name of author: Miguel Pérez Rodríguez

## Description of the topic

 In the context of the heterogeneity of economic situations in cities accross 
    the United States (difference in incomes, distribution of income, recent economic 
    growth, generation/destruction of jobs), I want to generate an interactive map
     by Metropolitan Statistical Areas (MSA), that includes only the MSA
    that have population over 500,000. 
    
With this interactive map I want to
    show, "at a glance", the current economical status for each MSA in terms of population,
    average income, income distribution, people that moved into that area in the last year,
    change in the labor force, unemployment rate, and the composition of the labor 
    force by industry, among others.

## Data sources

The main data source that I am going to use is the data available at MSA
    level from the United States Census Bureau (https://data.census.gov/). Particularly,
    I have found data per MSA per year in the following series:

    * DP03 - Selected Economic Characteristics:
        - Per capita income (dollars)
        - Distribution on the household income (number of households with income
            under 25k, between 25-50k, and so on)
        - Unemployment rate
        - Change in the labor force (as a percentage and also as a total population change)
    
    * B24050 - Industry by Occupation for the Civilian Employed Population 16 Years and Over:
        - Number of workers by industry (i.e. Construction, Manufacturing, Retail, 
            Transportation, etc)
    
    * B07201 - Geographical Mobility in the Past Year for Current Residence:
        - Percentage of people that moved from a different metropolitan area in the last year

Additionally, maybe I am going to use the GeoJSON map available in www.carto.com
    (particularly, in this [link](https://common-data.carto.com/tables/cb_2013_us_cbsa_5m/public/map))
    to show the MSAs in the United States map.

## Examples of interactive visualization

For the project I am thinking in the approach B, this is, a Dynamic Ensemble with three
or more visualizations. These visualizations would be:

1) Interactive map: A map of the United States that shows the MSAs and it deliver a summary
    with a tooltip. This map will highlight MSA based on the criteria of population (interactive
    box to say "I just want to see MSA larger than, for example, 2 million people") and will have
    scale of colours based on a selected variable (for example, scale of colours related to per 
    capita income, or the total change in labor force). I am thinking that the user will be able to
    "click" in the MSA, and display more information about that MSA below the map (in the form
    of three more interactive graphs related to that specific MSA). The example of this map would
    be an interactive version of, for example, one of these two graphs:
    * [Choropleth version of MSA in the United States](https://media.licdn.com/dms/image/v2/C4E12AQF3RUDQkxixhQ/article-inline_image-shrink_1000_1488/article-inline_image-shrink_1000_1488/0/1520146691265?e=1735171200&v=beta&t=zjmGrdbUwBvvD6c4odPuPIGAiTuYtAVvOUG-uSA1fdo)
    * [Circle version of MSA in the United States](https://lh3.googleusercontent.com/pw/AM-JKLU3IwDX3SfPr-7_XHFTV-Wz1iOaDg2686kHmKIYEg5PxAZTiA4dZR9HhWpTUAbIzSIwzuxKT_0KE2Anb-a4-u9tYuyJAYgHMMOMrvoWtktqEzI40QmW8xBfrV5DI0Yt9u13yFLNJ1sagDcTnvzc3K7r=w1345-h744-no?authuser=0)

2) Variable over time for the MSA: After the "click" in one MSA from the interactive map, I want
    that a graph displays below with the evolution of economical variables over time for that MSA. 
    The economical variables would be selected by the user, for example, unemployment rate, and it
    would look something like this [link](https://www.statista.com/statistics/183827/gdp-of-the-chicago-metro-area/).
    This graph would be interactive in the sense that the selected economical variable can
    be changed by the user. The possible economical variables that the user could chose are:
        (i) Per capita income
        (ii) Unemployment rate
        (iii) Total labor force
        (iv) Yearly change in the labor force
        (v) Population
        (vi) Total people that moved from a different metropolitan area in the last year
        (vii) Percentage of population that moved from a different metropolitan area in the last year

3) Distribution of the income in the MSA: After the "click" in one MSA from the 
    interactive map, I want another graph that displays below, in this case, a bar graph
    that displays the distribution of the income as percentage of households with income
    related to different ranges (percentage of households with income under 25k, between 25k-50k, 
    between 50k-75k, and so on). I would also like to have a time tool for the user to see how this
    has change over the time. It would be something "like" this [link](https://furmancenter.org/data/images/soc2019-borough-income-distribution-bronx.png),
    but with only one column per income range that changes to the year specified by the user.


4) Distribution of jobs by industry in the MSA: After the "click" in one MSA from the 
    interactive map, I want another graph that displays below, in this case, a tree
    map of the jobs by industry in that MSA (for example, percentage of population that
    works in Construction, Manufacturing, Retail, Transportation, etc) for the 
    year selected by the user. I am still thinking about adding this graph 
    because it seems that general industries doesn't vary that much among MSA. 
    It would be something like this [link](https://commons.wikimedia.org/wiki/File:Tree_Map_of_Employment_by_Industries_in_Los_Angeles_County,_Ca_%282015%29.svg).

## Mock-up of this interactive proposal

![](/mock-up_proposal.png?raw=true "")

## Questions

A specific question is that I have found that the series from the Census Bureau
(https://data.census.gov/) are not that easy to get for different years in an unified database
(when I access the raw data I am downloading a winrar file with one different file for each years),
I don't know if there is a way to download the same serie (for example, median income in dollars 
of 2022) for each MSA for each year in a single file. This is very specific, but if you have
experience with the Census Bureau dataset, I will be happy to check this in Office Hours
(because it would reduce a lot the amount of work related to data manipulation).
