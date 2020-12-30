# Big Mountain Resort Pricing Model

![Resort](https://user-images.githubusercontent.com/67468718/103321199-58c03380-49ed-11eb-9ab2-8f1063fd2ab9.JPG)

## Problem Statement: 
    
What opportunities exist for Big Mountain Resort to effectively develop and implement a new pricing strategy that can maximize capitalization in their facilities investments to offset their recent additional operating cost by $1,540,000 this season.

## Resort Story:
 
Big Mountain Resort offers spectacular views of Glacier National Park and Flathead National Forest, with access to 105 trails. Every year about 350,000 people ski or snowboard at Big Mountain. The business expressed a desire for some guidance on how to select a better value for their ticket price. by considering number of changes hoping to reduce cost without reducing ticket price or increasing ticket price.

## Current Resort's Pricing Strategy:

For Big Mountain Resort to base their pricing mainly on just the market average won’t be enough to maximize their capitalization investment and can’t be sustainable to gain an edge over the competition. 

## Modeling scenarios:

Big Mountain Resort has been reviewing potential scenarios for either cutting costs or increasing revenue (from ticket prices). Ticket price is not determined by any set of parameters; the resort is free to set whatever price it likes. However, the resort operates within a market where people pay more for certain facilities, and less for others. Being able to sense how facilities support a given ticket price is valuable business intelligence. This is where the utility of our model comes in.

The business has shortlisted some options:

 * Permanently closing down up to 10 of the least used runs. This doesn't impact any other resort statistics.
 * Increase the vertical drop by adding a run to a point 150 feet lower down but requiring the installation of an additional chair lift to bring skiers back up, without additional snow making coverage
 * Same as number 2, but adding 2 acres of snow making cover
 * Increase the longest run by 0.2 mile to boast 3.5 miles length, requiring an additional snow making coverage of 4 acres

The expected number of visitors over the season is 350,000 and, on average, visitors ski for five days. Assume the provided data includes the additional lift that Big Mountain recently installed.

## Feature Engineering:

 * **Feature Correlation heatmap**: a great way to gain a high level view and idnetify patterns of relationships amongst the features:
     * summit and base elevation are quite highly correlated. This isn't a surprise. 
     * AdultWeekend ticket price, we see quite a few reasonable correlations. fastQuads stands out, along with Runs and Snow Making_ac. 
     * The last one is interesting. Visitors would seem to value more guaranteed snow, which would cost in terms of snow making equipment, which would drive prices and costs up.
     * As well as Runs, total_chairs is quite well correlated with ticket price. This is plausible; the more runs you have, the more chairs you'd need to ferry people to them! Interestingly, they may count for more than the total skiable terrain area. For sure, the total skiable terrain area is not as useful as the area with snow making. People seem to put more value in guaranteed snow cover rather than more variable terrain area.
 
 ![correclations_heat](https://user-images.githubusercontent.com/67468718/103321593-46df9000-49ef-11eb-95e4-ed68a07ca5b8.JPG)
 
  * **Feature Correlation Scatterplots**: Correlations, particularly viewing them together as a heatmap, can be a great first pass at identifying patterns. But correlation can mask relationships between two variables
     * There's a strong positive correlation with vertical_drop.
     * fastQuads seems very useful. Runs and total_chairs appear quite similar and also useful.
    
![resort_Scatter](https://user-images.githubusercontent.com/67468718/103321868-8d81ba00-49f0-11eb-9fb6-26dc1a4c91b1.JPG)






