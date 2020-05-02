This is data visualisation using Tableau.


Tableau is a powerful business intelligence and data visualization tool that has a very intuitive user interface.

Here is the link to my visualisatoin: https://public.tableau.com/views/Europeancities-SmallBusinessIndex2019/Map?:display_count=y&publish=yes&:origin=viz_share_link

<div class='tableauPlaceholder' id='viz1588443057891' style='position: relative'><noscript><a href='#'><img alt=' ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Eu&#47;Europeancities-SmallBusinessIndex2019&#47;Map&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='Europeancities-SmallBusinessIndex2019&#47;Map' /><param name='tabs' value='yes' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Eu&#47;Europeancities-SmallBusinessIndex2019&#47;Map&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='filter' value='publish=yes' /></object></div>                


# Find the best city for new small business expansion

## Table of Contents

<div class="alert alert-block alert-info" style="margin-top: 20px">

<font size = 3>

1. <a href="#item1">Description of the problem</a>

2. <a href="#item2">Description of the data</a>

</font>
</div>

## Description of the problem

A company has a small running business and want to expand to new locations somewhere in Europe. 

Criteria for new locations:
- must be most populous European cities 
- the cities that are not far from the actual company's location
- the cities that offer the best environment for small businesses including real estate prospects, third-party incentives and support

How to help the company to find the best cities sitting in Europe for its expansion?

<img src="https://github.com/pospisilboh/Coursera_Capstone/blob/master/2020-04-29_13h43_17.png" align="center">

The idea is:
1. To find cities that offer the best environment (**score** from data source *Small Business Index 2019*) for small businesses
2. To find a geographical coordinate of each city by its name and country
3. Via a venues of each city (top X venues that are in city a radius of Y meters) find a top Z **categories** (from data source *Foursquare API*) that have been applied to the venues in a city
4. Calculate **distance** between each city and the actual company's location
5. Classify cities via **score** and **distance** to appropriate count of clusters
6. As an output provide the company appropriate outputs in the form of maps, graphs or tables that can help it to select the best city or group of cities for its expansion.

Example 1: Map of cities + graphical identification of clusters.
<img src="https://github.com/pospisilboh/Coursera_Capstone/blob/master/2020-04-29_14h36_10.png" align="center">

Example 2: Scatter plots of the relationship between cities variables (**score** and **distance**) + graphical identification of clusters.
<img src="https://github.com/pospisilboh/Coursera_Capstone/blob/master/2020-04-29_14h16_50.png" align="center">

## Tableau
<div class='tableauPlaceholder' id='viz1588441609767' style='position: relative'><noscript><a href='#'><img alt=' ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Eu&#47;Europeancities-SmallBusinessIndex2019&#47;Map&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='path' value='views&#47;Europeancities-SmallBusinessIndex2019&#47;Map?:embed=y&amp;:display_count=y&amp;publish=yes' /> <param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Eu&#47;Europeancities-SmallBusinessIndex2019&#47;Map&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='filter' value='publish=yes' /></object></div>   

https://public.tableau.com/views/Europeancities-SmallBusinessIndex2019/Map?:display_count=y&publish=yes&:origin=viz_share_link

## Description of the data

The following data sources will be used in the solution:
- Small Business Index 2019 (https://sumup.co.uk/small-business-index-2019/)
- Foursquare API (https://developer.foursquare.com/)

### Small Business Index 2019
**The SumUp Small Business Index** reveals the European cities that offer the best environment for enterprise. The Index reveals the status quo of small businesses across Europe’s most populous cities, including real estate prospects, and third-party incentives and support.

<a href="https://sumup.co.uk/small-business-index-2019/"><img src="https://github.com/pospisilboh/Coursera_Capstone/blob/master/2020-04-29_11h02_16.png" align="center"></a>

**City List** includes 100 cities across Europe selected based on biggest population size, including all the capital cities in Europe, regardless of membership of the European Union.

- **Population:** Urban population, sourced from United Nations Statistics Division, with most recent data for each city.

- **Size:** Urban size (km²), sourced from United Nations Statistics Division, University Websites and Wikipedia

They have analysed four major **categories** which contribute to providing a comprehensive overview of Small Business in Europe, thus dividing the Small Business Index 2019 into:
- **Small Businesses** - the type and total number of small businesses per city
- **Density** - the number of small businesses per capita and km²
- **Rent and Real Estate** - the retail area provision and the cost of rent
- **External Support** - financial measures and subsidies supporting small businesses

Each category is broken down into sub-factors:
- For Small Businesses, the following criteria were researched:
  - 🛍 Shops: Total number of shops per city. Source: OpenStreetMaps.

  - ☕ Cafe/Bar: Total number of cafes and bars per city, calculated as an average from 3 different sources: OpenStreetMaps, Yelp, and TripAdvisor.

  - 🍴 Restaurant: Total number of restaurants per city, calculated as the average from 3 different sources: OpenStreetMaps, Yelp, and TripAdvisor.

  - 💼 Handyman: Total number of handyman businesses per city, calculated as an average from 2 different sources: OpenStreetMaps and Yelp. This category includes: electricians, plumbers, locksmiths, carpenters, and painters.

  - 💅 Beauty: Total number of beauty-related businesses per city, calculated as an average from 2 different sources: OpenStreetMaps and Yelp. This category includes: cosmetic shops, hairdressers, massage salons, nail salons, and tattoo studios.

  - 🚖Taxi: Total number of taxis per country. The data was obtained from a European Commission 2016 report: “Study on passenger transport by taxi, hire car with driver and ridesharing in the EU”. For cities not included in this report, manual research was undergone with data retrieved from government websites and news articles.
 
- For Density, the following criteria were researched:
  - 👪Per Capita: The number of small businesses per inhabitant. A percentage was calculated between the number of small businesses and the population of the city. Population data was obtained from the last official census data.

  - 📍Per square km: The number of small businesses per km². Calculated based on Total Nr. of Small business and Urban Area.
- For Rent and Real Estate, the following criteria were researched:
  - 🔑Availability: The retail sales area provision per person, calculated as the retail area per country divided by the population. Source: KfK study on key retail indicators.

  - 💵Price: Monthly rent for an 85m² space, calculated as an average from 2 different sources: Expatistan and Numbeo.
- For External Support, the following criteria were researched:
  - 💰EU Subsidies: The amount granted to each country by the EU, as part of the EU COSME (Competitiveness of Enterprises and Small and Medium-sized Enterprises) program. Scored per capita.

  - ⚖Tax: The percentage of a company's income that must be paid to the government by law. Source: PWC tax summaries.

  - 🚀Initiatives: Total number of social media users per city identifying as “Small Business Owner” in addition to total number of social media users per city ‘interested’ in ‘start-up related topics’, e.g. Startup Outlets. Tracked using digital behavioural data measured as ‘interest’.

  - 📈Investment: Total venture capital from the state. The data was obtained in US dollars from 2017 and current conversion rates applied (US to Euro = 0.83). Source: Venture Investment Data Review. Scored per capita.


In order to rank the cities in an index, a score was attributed to each category, with the sum equaling in the total small business score. Once scores were obtained, the overall rank was calculated by weighting each criteria according to: Small Businesses (35%), Density (15%), Rent and Real Estate (35%), External Support (15%), therefore resulting in the overall score.

**Once the overall score was obtained, the scale was adjusted to standardise the results, resulting in a range from 1-10.**
This was achieved by ranking the final scores, assigning 0 to the lowest score, 10 to the highest, and the proportional part of the grades to the rest of the values.


### Foursquare API
The Places API offers real-time access to Foursquare’s global database of rich venue data and user content.

**Venue Recommendations** returns a list of recommended venues near the defined location and for each venue an array of **categories** that have been applied to this venue. One of the categories will have a primary field indicating that it is the primary category for the venue. For the complete category tree, see: https://developer.foursquare.com/docs/build-with-foursquare/categories/

For the complete the Places API documentation, see: https://developer.foursquare.com/docs/places-api/
