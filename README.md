# Countries of the World

## Introduction

The acquired data is a table with facts about the countries in the world. This includes GDP per capita, population, literacy rate, to name a few.

We'll be making visualizations of these, often categorizing them by the pre-defined regions.

## Usage

The data used is available publicly at [Kaggle](https://www.kaggle.com/fernandol/countries-of-the-world/version/1).

The data has been saved as an Excel Workbook to make it compatible with Tableau. Since the original dataset used commas as decimal separators, they've been replaced with decimal points. This ensures the values aren't interpreted as strings.

## Regions

To analyse the data, the countries have been divided into several regions. The following map shows the various regions. You can hover or click to see the various names.

<iframe src="https://public.tableau.com/views/WorldData_17/RegionsinColour?:embed=y&:display_count=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Regions Map)

## GDP

One of the major factors on which a country is assessed is its GDP per capita. The following map shows the GDP for each country, colour coded for easy comparisons. The terms GDP and GDP per capita will be used interchangeably in this text.

<iframe src="https://public.tableau.com/views/WorldData_17/GDPMap?:embed=y&:display_count=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (GDP Map)

The map shows that not many countries have high GDP. But how well is this distributed? 

<iframe src="https://public.tableau.com/views/WorldData_17/GDPHistogram?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (GDP Histogram)

This is clearly not a normal distribution. Most countries have low GDP with only a few in the higher ranges. A significant portion of the world wealth is concentrated among a few countries.

So which countries are these? Obviously we could simply list them down and sort them to see the top 10 countries with the highest GDP. With over 200 countries, selecting the top 10 doesn't tell us why these countries have a higher GDP.
If we tried to create a graph with GDP of all countries to see a trend, it would become cumbersome and confusing to find any.

A better solution: group countries by their region and compare the GDP of each region.

<iframe src="https://public.tableau.com/views/WorldData_17/GDPbyRegion?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (GDP by Region)

Western Europe has the highest GDP, which makes perfect sense. The region is well developed and well regulated by the EU with high living standards.
It also makes sense that Northern Africa has the lowest GDP.

But with Sub-Saharan Africa having nearly equal GDP as North America, our data seems flawed. Very few industries lie in Sub-Saharan Africa; the United States of America ishould itself surpass Sub-Saharan Africa's economy, and do so by a huge margin.
So what happened?

The regions have varying areas and varying number of countries. Comparing them directly doesn't give us very profound results.

The previous graph compared the regions by the sum total of their GDP. What we'll do instead, is compare the average GDP of each region. This should give us a better understanding of the economic conditions of each region.

<iframe src="https://public.tableau.com/views/WorldData_17/GDPbyRegionavg?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (GDP by Region (Average))

This graph seems to make a lot more sense.

Just as the previous, Western Europe is still the at the top with highest average GDP.
North America is at second place now, no longer lost in the centre. With two superpowers, USA and Canada, this only seems fair. A closer inspection would let us know that North America is behind Western Europe by only about a $1000 per capita.

Sub-Saharan Africa, on the other hand, has managed to move to the very end of the list. This also seems fair, considering the lack of industries and comparable development.

GDP alone doesn't provide a lot of insight on a country, or even a region. But it's a good place to start. GDP would probably also be used in the upcoming sections because most factors are inter dependent.

To better our understanding, we will take up area next.

## Area

Let's see if GDP is affected by the area of a country.

<iframe src="https://public.tableau.com/views/WorldData_17/GDPAreaCorr?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (GDP Area Correlation)

The x-axis has been made logarithmic to better scatter the points on our plot.

There seems to be no direct correlation between the two.

How about the population and area? 

<iframe src="https://public.tableau.com/views/WorldData_17/PopulationAreaCorr?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (GDP Population Correlation)

Even though there does seem to be a correlation between the population, this doesn't tell us much.
Note that both the axes have been made logarithmic to better graph our plot. The relation is a power relation.

Instead of considering the entire area of a country, we could look at land utilization. We could see how much percentage of land of a certain country is arable, for starters.

<iframe src="https://public.tableau.com/views/WorldData_17/ArableLandMap?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Arable Land Map)

One would assume the more perecntage of arable land, the more percentage of crops produced.

<iframe src="https://public.tableau.com/views/WorldData_17/ArableLandtoCrops?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Arable Land to Crops)

Surprisingly enough, that is not the case.

Land doesn't seem to tell us a lot about a country. Perhaps, we would find something interesting looking at the population.

## Population

Which countries are the most populated? This would give us a general idea of where most of our population resides.

<iframe src="https://public.tableau.com/views/WorldData_17/PopulationMap?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Population Map)

China and India stand out from the rest of the map with their individual populations crossing over a billion people. With increasing population, resource distribution becomes a challenge.

Another factor that could affect quality of life is population density.

<iframe src="https://public.tableau.com/views/WorldData_17/PopulationDensityMap?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Population Density Map)

Something seems very wrong here. Every country seems to have nearly the same density. The reason for this is that we have considered high density regions to be big enough to stand out. Most densely populated countries happen to be very small, and often cannot be viewed from a zoomed out view of the world map.

We'll make a bubble chart to look at the countries on the top of this list.

<iframe src="https://public.tableau.com/views/WorldData_17/PopulationDensityBubble?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Population Density Bubble)

Monaco and Macau are the densest of all, with an alarming 16,272 and 16,183 people per square mile respectively. These are very small countries, and explains why we didn't get to see them initially.

Singapore and Hong Kong are close contenders but with only about two-fifths the population per square mile of Monaco (or Macau).

Beyond Malta, the colours more or less converge into the same as not much of a varying range of numbers is left. 
Majority of the countries happen to fall in this category and are practically indistinguishable till the denser ones like Monaco are removed.

Density directly affects resource availability and technological advancement, and thus quality of life.

## Literacy Rate

An easy way to check the advancement of a country is to check its literacy rate. Higher literacy rates show effective education infrastructure and access to potential higher education.

<iframe src="https://public.tableau.com/views/WorldData_17/LiteracyRateMap?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Literacy Rate Map)

Most of the world seems well literate with a few exceptions in Africa and Asia. 
To get a closer look, let's compare literacy rates by region.

<iframe src="https://public.tableau.com/views/WorldData_17/AverageLiteracybyRegion?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Literacy Rate by Region Bar Chart)

As noted from the world map, Sub-Saharan Africa and Northern Africa are at the very end.

It is difficult to make a comparison among the top five regions as they all have a literacy rate of over 97%. North America and Western Europe lie within.

This seems familiar; the GDP by region plot showed similar results. Is it possible that GDP is affected by literacy rate?

<iframe src="https://public.tableau.com/views/WorldData_17/LiteracyGDPCorrelation?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Literacy GDP Correlation)

Literacy rate seems to affect GDP almost exponentially. This makes sense considering the greater the number of educated individuals, the better will they be able to fill and do high skilled work.
In most countries, high skilled work affects GDP significantly more than low skilled.

Apart from better jobs, literacy also provides better decision making skills.
In particular, we talk about dependence of birth rate on literacy, since it is readily available in our data.

<iframe src="https://public.tableau.com/views/WorldData_17/LiteracyBirthrateCorrelation?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Literacy Birthrate Correlation)

As literacy rate goes up, birthrate comes down. This isn't a bad thing; it means literate individuals are capable of family planning.
With limited resources and the world population reaching almost 8 billion, population growth is a cause for concern and needs to be tackled.

A better measure would be infant mortality rate, which would tell us the quality and accessibility of a country's medical infrastructure.

<iframe src="https://public.tableau.com/views/WorldData_17/LiteracyInfantMortalityCorrelation?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Literacy Mortality Correlation)

Note that infant mortality cannot be equated with family planning as it is a calamity, not a choice. Death of children will stunt the growth of a nation as it means poor health standards and/or lack of accessibility or affordability to healthcare.

Clearly, as literacy rates go up, mortality rates come down. Literate individuals are much more likely to be able to contribute to the medical sector and access it in times of need.

Another thing we could check is the dependence of technology on literacy rate.

<iframe src="https://public.tableau.com/views/WorldData_17/LiteracyPhoneCorrelation?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Literacy Mobile Correlation)

In our graph, we see an almost exponential dependence of phones per 1000 people on literacy rate.

Technological advancement of a country isn't purely dependent on the percentage of phone users. But it does give us a basic idea of how technologically literate the population of a country is.
Technological literacy determines the number of high skilled workers, which would affect the economy.

## Migration

Net migration is the difference between immigrants and emmigrants. A country with a high migration rate usually means that it is a wealthy country providing plenty of opportunity. A low migration rate might imply lack of political stability or infrastructure.

<iframe src="https://public.tableau.com/views/WorldData_17/MigrationMap?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Migration Map)

Afghanistan is a clear outlier with the highest migration rate. This seems unlikely with the present conditions. Perhaps the data is outdated or has genuine errors.

We'll compare regions next.

<iframe src="https://public.tableau.com/views/WorldData_17/MigrationbyRegion?:embed=y&:display_count=yes&publish=yes:showVizHome=no&:embed=true" width="800" height="500"></iframe> [//]: # (Migration by Region)

This makes a lot more sense, with Western Europe back at the top. Asia and Near East provide plenty of job, so obviously they'd be close.

Northern America has a negative migration. This is surprising considering it has USA and Canada. However, it also has Greenland, which is already sparsely populated, and people tend to move away to other countries for better opportunities.