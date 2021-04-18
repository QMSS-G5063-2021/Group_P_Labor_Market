# Group P Labor Market Process Book

Members:
Ming Nie (mn2984) 
Chujun Zhao (cz2621) 
Edmund Lam (ecl2169) 
Chloe Cao (kc3410)

## Topic

The recent minimum bill proposal raised by the democrats shows their goal to increase minimum wage to $15 per hour by 2025. Inspired by this ambitious bill, we decide to make visualizations of the labor market data. In specific, we would like to explore the minimum wage and unemployment rate of each state of U.S. Hopefully, our map will enable small business owners, workers, and policy researchers to learn about the labor market statistics.


## Data Source

The data of labor statistics come from the National Census Bureau. The variables include the state minimum wage, federal minimum wage, unemployment rate, and CPI of the past five years. The latitude and longitude data comes mainly from geocode using Google API. The locations of Walmart and target shops data is from the Internet.


## Visualization

### Map 1

The variables I used for this plot include state name, unemployment rate, state minimum wage and federal minimum wage. The longitude and latitude are generated using geocode and google cloud API. I used leaflet package and added content by using `addCircleMarkers()`.

### Map 2

The variables I used for this plot include state name, state minimum wage, longitude and latitude . First I get the map from `map_data('state')`. The map is then merged with the `dataframe` containing state minimum wage data. Then I specify `fill = State.Minimum.Wage`and use `ggplot`  to create the Choropleth map.

### Map 3 Series 

The map above demonstrated the Minimum Wage in 2020 across the states. However, we are also interested in demonstrating how the minimum wage has changed over years. As a result, we created three additional choropleth maps for year 2000, 2008, and 2016. The maps are produced with minimum wage data and map state data from the same source as above. To make the maps a little bit easier to read, some interactions are added to the choropleth maps. The abbreviations of the states are also displayed on the maps (source of abbreviations came from `state.abb`, which is originally loaded with R).

#### Top 5 States With the Highest Minimum Wage (1968-2020)

Which states have the highest minimum wage over years? Since we obtained data from 1968 to 2020, we wanted to show the top 5 states for every year from 1968 to 2020. As a result, we produced a racing bar chart with `gganimate`. We first selected the top 5 states for each year and produced a plot for each year respectively. Then we combined the plots, used the `Year` variable as the axis. We eventually made the plot move by using `gganimate`.

### Map 4a

Similar Map to Map 2 using the unemployment rate.

### Map 4b

It is also important to find out the employment opportunities. Then we want to find the shop locations of Walmart stores, the biggest employer in the country. The variables I used for this plot include the longitude and latitude of all Walmart shops. I used `plot_geo` to create maps with zoom interactivity. 

### Map 5 

Similar map to Map 1. Added clustering interactivity using `clusterOptions`.

### Scatter Plot 1
Here is the scatter plot for the distribution of unemployment rate in different states in US in 2016. We hypothesize that the unemployment rate among different states distribute dispersedly. We want to investigate into the trend of unemployment rate among different states. I used the `ggplot--scatter` plot to describe the distribution of the unemployment rate in US.

### Scatter Plot 2
There is no denying that we should compare the unemployment rate from 2016 to 2020 if we want to look into the changes of unemployment rate in US. So I also plotted the unemployment rate in 2020 using the `ggplot_scatter` plot. 

### Interactive Plot
We plot an interactive plot here to compare the performance in Hawaii, Massachusetts and New York. I used the `plotly` to make an interactive plot which shows the information of the year and the unemployment rate in that year. And I choose the line chart to express the trend of the unemployment rate.
