# Coursera_Capstone

## Description of the problem
and a discussion of the background
Small Business


In Module 3, we explored New York City and the city of Toronto and segmented and clustered their neighborhoods. Both cities are very diverse and are the financial capitals of their respective countries. One interesting idea would be to compare the neighborhoods of the two cities and determine how similar or dissimilar they are. Is New York City more like Toronto or Paris or some other multicultural city? I will leave it to you to refine this idea.
In a city of your choice, if someone is looking to open a restaurant, where would you recommend that they open it? Similarly, if a contractor is trying to start their own business, where would you recommend that they setup their office?

## Description of the data

The following data sources will be used in the solution:
- Small Business Index 2019 (https://sumup.co.uk/small-business-index-2019/)
- Foursquare (https://developer.foursquare.com/)

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


### Foursquare
