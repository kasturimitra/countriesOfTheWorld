# Countries of the World

The data used is available publicly at [Kaggle](https://www.kaggle.com/fernandol/countries-of-the-world/version/1).

The data has been saved as an Excel Workbook to make it compatible with Tableau.

## Regions

To analyse the data, the countries have been divided into several regions. The following map shows the various regions. You can hover or click to see the various names.

<iframe src="https://public.tableau.com/views/WD2Regions/RegionsinColour?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Regions Map)

## GDP

One of the major factors on which a country is assessed is its GDP. The following map shows the GDP for each country, colour coded for easy comparisons.

<iframe src="https://public.tableau.com/views/WD1GDPMap/Dashboard1?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (GDP Map)

The map shows that not many countries have high GDP. But how well is this distributed? 

<iframe src="https://public.tableau.com/views/WD3GDPHistogram/GDPHistogram?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (GDP Histogram)

This is clearly not a normal distribution. Most countries have low GDP with only a few in the higher ranges. A significant portion of the world wealth is concentrated among a few countries.

So which countries are these? Obviously we could simply list them down and sort them to see the top 10 countries with the highest GDP. With over 200 countries, selecting the top 10 doesn't tell us why these countries have a higher GDP.
If we tried to create a graph with GDP of all countries to see a trend, it would become cumbersome and confusing to find any.

A better solution: group countries by their region and compare the GDP of each region.

<iframe src="https://public.tableau.com/views/WD4GDPbyRegion/GDPbyRegion?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (GDP by Region)

Western Europe has the highest GDP, which makes perfect sense. The region is well developed and well regulated by EU with high living standards.
It also makes sense that Northern Africa has the lowest GDP.

But with Sub-Saharan Africa having nearly equal GDP as North America, our data seems flawed. Very few industries lie in Sub-Saharan Africa; the United States of America ishould itself surpass Sub-Saharan Africa's economy, and do so by a huge margin.
So what happened?

The regions have varying areas and varying number of countries. Comparing them directly doesn't give us very profound results.

The previous graph compared the regions by the sum total of their GDP. What we'll do instead, is compare the average GDP of each region. This should give us a better understanding of the economic conditions of each region.

<iframe src="https://public.tableau.com/views/WD5GDPbyRegionAverage/GDPbyRegionavg?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (GDP by Region (Average))

This graph seems to make a lot more sense.

Just as the previous, Western Europe is still the at the top with highest average GDP.
North America is at second place now, no longer lost in the centre. With two superpowers, USA and Canada, this only seems fair. A closer inspection would let us know that North America is behind Western Europe by only about a $1000 per capita.

Sub-Saharan Africa, on the other hand, has managed to move to the very end of the list. This also seems fair, considering the lack of industries and comparable development.

GDP alone doesn't provide a lot of insight on a country, or even a region. But it's a good place to start. GDP would probably also be used in the upcoming sections because most factors are inter dependent.

To better our understanding, we will take up area next.