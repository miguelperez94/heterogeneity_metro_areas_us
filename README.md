# A tool to analyze economic heterogeneity of metropolitan areas in the United States

Author: Miguel Pérez Rodríguez

![](/embedded_screenshot.png?raw=true "")

## To see the webpage related to this project

You can see the webpage related to this project in this [link](https://heterogeneitymsaunitedstates.netlify.app/).

If by any chance that link doesn't work, you can run the webpage by going to
the directory "www", then run the command "python -m http.server", and then open 
"http://localhost:8000" in your browser. The base webpage should look 
like the image provided above in this file.

## Description of the project

This project attempts to analyze economic heterogeneity in the United 
States at the Metropolitan Statistical Area (MSA) level with two 
questions that a user could have in mind: (i) "Where are things going better 
and worse economically in the United States?", and (ii) 
"How is a particular MSA doing in comparison to the rest of the United States?"

By definition, each MSA has at least one urban core and includes
adjacent communities having a high degree of economic and social integration.
In this context, common approaches to do this type of analysis are at the County and 
State level, the analysis at the MSA level presented in this project is an intermediate 
level of analysis that is currently scarce and that captures important trends 
in metropolitan economic activity that (i) can reflect actual economic 
relationships inside each area and (ii) shows important economic 
differences across MSA in the country.

To answer each of the questions for the purpose of this project, this project 
presents economic data for each Metropolitan Statistical Area (MSA) in the 
United States in two ways: (i) an <strong>interactive map</strong> 
that shows a general overview of heterogeneity in the United States by different 
economic variables, and (ii) an <strong>interactive bar graph</strong> 
that shows the percentile of the selected Metropolitan Area for each economic 
variable in comparison to the other MSAs in the country.

The economic variables available to analyze are (i) <strong>per capita 
income</strong>, current levels and growth over time, (ii) 
<strong>population</strong>, current levels and growth over time, and (iii) 
<strong>general and housing regional price indices</strong>, current levels.

The "Motivation" section of the webpage presents the general motivation 
behind the project and a couple of conclusions that can be easily
derived by the use of the tools presented in the webpage, but
as an interactive tool, the final conclusions are up to the user, and overall, it is
easy to see huge differences in almost every economic variable across the different MSAs,
which reflects part of the economic heterogeneity in the United States.

## Data Sources

<a href="https://apps.bea.gov/itable/?ReqID=70&step=1&_gl=1*1hajvqr*_ga*NDk0MDAwMTYxLjE3MzI5MDY3NzA.*_ga_J4698JNNFT*MTczMzcwMTUzNS42LjEuMTczMzcwMTc0MC41MS4wLjA.">
U.S. Bureau of Economic Analysis (BEA) - Regional Data</a>: 
Economic data at the MSA level related to population, personal income per capita, 
and general and housing price indices.
<br>

<a href="https://www.jsdelivr.com">
jsDelivr Open Source maps</a>: 
TopoJson maps related to (i) 
<a href = "https://www.jsdelivr.com/package/npm/world-atlas">countries of the world</a> 
and (ii) <a href = "https://www.jsdelivr.com/package/npm/us-atlas">
states in the United States</a>.
Licensed <a href = "https://github.com/jsdelivr/jsdelivr/blob/master/LICENSE.md">MIT</a>.
<br>

<a href="https://github.com/loganpowell/census-geojson/tree/master/GeoJSON/20m/2021">
Logal Powell GitHub</a>: 
GeoJson map related to Metropolitan Statistical Areas in the United States.
<br>

<a href="https://www.census.gov/programs-surveys/metro-micro/about.html">
United States Census Bureau</a>: 
Formal definition of Metropolitan Statistical Area.
<br>

<a href="https://www.bryantsmith.com/template/">
Bryant Smith CSS Templates - Reverted Template </a>: 
Part of CSS structure for this webpage.
<br>

<a href="https://www.w3schools.com/css/css_navbar_horizontal.asp">
W3Schools - CSS Navigation Bar Guidelines</a>: 
Guidelines for CSS code related to Navigation Bars.
<br>
