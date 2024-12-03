# A tool to analyze economic heterogeneity of metropolitan areas in the United States

By Miguel Pérez Rodríguez

## What is your current goal? Has it changed since the proposal?

My current goal is to generate an interactive map of the United States that includes economic information at a level of Metropolitan Statistical Areas (MSA) to show the heterogeneity of different urban areas in the country. The MSA focus is because I have seen analysis at the state and county levels, but not at the MSA level, and I am interested because the MSA analysis is something closer to a "city" level analysis.

Also, I want to provide information of a single Metropolitan Area that the user would want to know more about it. Because of that, using the selection from the user, the webpage shows a table of information and a graph of ratios related to the variables for that specific Metropolitan Area and the comparison with the whole United States Metropolitan Areas.

The goal hasn't changed from the proposal, but the specifics on how to accomplish it have changed a bit. I am maintening the interactive map, but as a second visualization I think that I prefer a bar graph that shows the comparison of different variables to the US, rather than a line map that would show the history for a selected variable over time (mainly because I think that the bar graph of comparison can provide more information more quickly related to the different variables).

## Are there data challenges you are facing? Are you currently depending on mock data?

I am not depending on mock data currently, but I stil want to add more economic data on the map. Now I am using only variables related to population, per capita income and per capita growth over time, but I want to add more data, at least unemployment and population change in the last year and last 10 years.

The main challenge that I am facing regarding the data is that it is not easy to find "clean" data at a time series level for MSA, mainly because MSA change over time, so it is not easy to see the evolution of the indicators. Currently I am counting a lot on the data that I found from the US Bureau of Economic Analysis (BEA) that have the data at a time series level (they did the job of estimating data for each Metropolitan Area even when the area was not even defined in previous years or it has change in its composition of counties over the years). This challenge is mainly reducing the amount of data that I can show (because the BEA doesn't have that much data at the MSA level), but I think that I can manage it and I think that the visualization will be good even with not that much more data.

## Walk us through an interaction, either in words or you can record a quick 2-3 minute video.

Firstly, to run the webpage you have to enter the directiory "interactive_draft", then run the command "python -m http.server", and then open "http://localhost:8000" in your browser. Just in case, the webpage should look like the file "image_of_interactive_draft" provided in the same folder.

The webpage have 4 sections, two of them with interactivity. The section "Economic Outlook of Metropolitan Areas in the United States at a Glance" presents the interactive map at the MSA level: 

- The first interactivity is that the user can select the minimum population of the MSA that he wants to see in the map. The default is 50,000 people (that is the threshold to be considered a MSA defined by the government), but if, for example, we want to see only the MSA with over 5 million people, the user can select that and the map will change accordingly.
- The second interactivity is that the user can select the attribute of interest in the map. Currently there are six different options.
- The third interactivity is the mouseover hover effect, where the user can see with its mouse the information of the MSA related to: (i) Name, (ii) FIPS Code (this will be useful in the next part), (iii) Population, and (iv) the value for the selected attribute of the map.
- The fourth interactivity is that the user is able to do zoom and move around the map with its mouse.

On the other hand, the section "Economic Outlook of the selected Metropolitan Area" presents a interactive table and WILL present an interactive graph (currently the graph is just an image from Excel, but that will change in the final version). The interactivity here is that the user will chose the FIPS code of the MSA of interest, and with that the table and the graph will change to show him the information related to that specific MSA.

## Include a _numbered_ list of questions for us to respond to.

1. I have a very particular question about the zoom and the interaction. Currently the zoom is working, but if I zoom or move the map, and afterwards I change a parameter, the changes in the map will show in the "original" position and zoom of the map, not the current position and zoom. This is solved simply because moving or zooming around the map solves the issue fast, but I don't like that the interaction causes problem with the zoom. Do you know any tip to solve this?

2. In general terms, I am thinking on focusing of adding a couple of more variables to chose, create the second graph for the interaction, and improving the outlook of the page. Is this enought interactivity for the project or should I look for something else? Thank you in advance for your answers!