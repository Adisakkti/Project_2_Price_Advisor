# Price Advisor for Homeowners and Sellers
## Project name :  PriceAdvisor
**Description** : The tool aims to assist in evaluating property prices to facilitate accurate and successful buying and selling transactions

**Dataset:** : Price and facilities of property in Bangkok,Samut Prakan and Nonthaburi 

| Feature          | Type       | Dataset                               | Description                                      |
|:----------------:|:----------:|:-------------------------------------:|:------------------------------------------------:|
| **id**   | int | train.json | ID of selling item 
| **province** | string      | train.json | province name: this dataset only includes Bangkok,Samut Prakan and Nonthaburi|
| **district** | string | train.json | district name       |
| **subdistrict**      | string  |train.json            | subdtistrict name |
| **address**    | string     | train.json  | address e.g. street name, area name, soi number |
| **property_type** | string | train.json | type of the house: Condo, Townhouse or Detached House  |
| **total_units** | float | train.json | the number of rooms/houses that the condo/village has      |
| **bedrooms** |int| train.json | the number of bedrooms    |
| **baths** | int | train.json | the number of baths       |
| **floor_level** | int | train.json | floor level of the room  |
| **floor_area** | float | train.json | total area of inside floor [㎡]  |
| **land_area** | float | train.json | total area of the land [㎡]      |
| **latitude** | float | train.json | latitude of the house    |
| **longitude** |float | train.json | longitude of the house    |
| **nearby_stations** | string | train.json | district name       |
| **nearby_station_distance** | list | train.json | list of (station name, distance[m]). Each station name consists of station ID, station name, and Line such as "E4 Asok BTS"|
| **nearby_shops** | int| train.json | the number of nearby shops     |
| **nearby_supermarkets** | int| train.json | the number of nearby supermarkets    |
| **nearby_shops** | int| train.json | the number of nearby shops   |
| **year_built** | int| train.json | year built |
| **month_built** | string| train.json | month built: January-December |
| **long_distance** | float | train.json | The distance(longtitude) from the building to the median point |
| **lat_distance** | float | train.json | The distance(lattitude) from the building to the median point |
| **price** | float | train.json | TARGET VALUE selling price|

**Objective:**
1. To create a Model that helps homeowners accurately price their properties for sale, maximizing returns and simplifying the selling process
2. Evaluating real estate prices in the Bangkok, Nonthaburi, and Samut Prakan areas.
               

## Problem Statement
Many homeowners face challenges in accurately valuating their properties when looking to sell. The absence of reliable and data-driven valuation tools often leads to overpricing or underpricing, potentially resulting in delayed sales or missed opportunities. There is a need for an accessible and accurate tool that empowers homeowners to set optimal asking prices and maximize their returns within a reasonable time frame.


**Questions:**  
1. How can the Model ensure accurate property valuations while considering various factors like location, size, facilities, and market trends?
2. What features and functionalities should be incorporated to create a user-friendly experience for homeowners seeking property valuations?

**Solution:** The proposed solution is to develop an intuitive tool that allows homeowners to input property details and receive instant, accurate valuations. This platform will leverage robust data integration from reliable real estate sources and utilize advanced algorithms to calculate valuations based on a comprehensive set of factors including location, property type, size, amenities, and current market conditions

## Conclusions and Recommendations

**The model will be able to accurately assess house prices if we select appropriately sized features, good features that are relevant to the price. Therefore, I recommend these features that will allow the model to calculate prices accurately**
1. Bedroom 
2. Bathroom  
3. Nearby station
4. Floor area 
5. Floor level
6. Nearby shop 
7. Nearby station
8. Long distance 
9. Lat distance
10. District
11. Property type 

#### the most influential feature on price is `Latitude distance`. It has a negative correlation, meaning that if the distance from the median latitude of the data is large, the price will decrease.
**Recommendation: If your house has a `large floor area` and is `located close to shops`, there is a higher likelihood that the price of your house will be higher. Additionally, houses in Bangkok tend to have the highest prices compared to the other two provinces**

### when using Ridge regression, the model performs the best and is the most accurate based on all the experiments conducted so i reccomended to use Ridge Regression

![Model Performance](for_submit/pictures/modelperformance.png)



#  "If my model becomes more accurate, it means that users will trust it and come back to use my model again"



**Impact:** 
1. Empowered Homeowners: Provide homeowners with a reliable tool to confidently price their properties, increasing their chances of a successful and profitable sale.
2. Market Transparency: Increase transparency in the selling process by educating homeowners about the factors influencing property valuations.



