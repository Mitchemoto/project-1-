### US Energy Usage and Impacts on Air Pollution: 2001-2019
Authors: Andre Shearer, Erich Mitchell, Felix Pronove, Justynn Hammond, Kim Christensen, Lisa Caruana

Question: Does an increase in renewable energy production reduce air pollution levels?

Hypothesis: An increased use of renewable energies results in less air pollution. 


Data sources: 
1. Net generation for electric power across the US (2001-2019):  
US Energy Information Administration (EIA) Electricity Data Browser
(website: https://www.eia.gov/electricity/data/browser/#/topic/0?agg=2,0,1&fuel=vvvvu&geo=vvvvvvvvvvvvo&sec=008&linechart=ELEC.GEN.ALL-US-98.A&columnchart=ELEC.GEN.ALL-US-98.A&map=ELEC.GEN.ALL-US-98.A&freq=A&ctype=linechart&ltype=pin&rtype=s&pin=&rse=0&maptype=0)

2. Data on air pollution levels across the US by latitude and longitude:
US Environmental Protection Agency Air Quality System (AQS) API
(website: https://aqs.epa.gov/aqsweb/documents/data_api.html)    

Our project provided a broad overview of trends in US energy production by state and region from 2001-2019,
with a focus on shifts from nonrenewable to renewable energy sources. We examined changes in fuel source, 
megawatt hours by fuel source at the state level, and statistically significant changes in air pollution
levels across the US, with projections for when we can expect to see a shift to 100% renewable energy
production at the current rate of change.   

Research methods: For data on net generation of electric power by source, we  used a CSV file generated 
by the EIA Electricity Data Browser that broke down net energy generation by non-renewable and renewable 
energy sources at the country, regional, and state level on an annual basis from 2001-2019.  

For data on air quality across the US, we used an API call on the US EPA AQS. The EPA AQS API 
required state codes to make calls. Air pollution data was pulled for each state 
individually using the state code. Results returned for the states included different monitors at various 
latitude (lat) and longitude (lon) measurements. We also pulled in the latitude and longitude measurements, 
in order to facilitate using these values in the Google GMAPs API. Each year of data was pulled in a separate API call. 

### Results   
### Renewable Energy Trends in the US: 2001-2019
There was an overall upward trend in renewable energy generation in the US from 2001-2019, 
with renewable energy increasing at a rate of 1.02% per year. At this rate, the US will 
reach 100% renewable energy by 2089. The forecasted renewable energy use for 2020 is 25.47%
and 26.49% for 2021. 

However, even with recent gains in renewable energy production, coal is still king. US energy
production is so heavily reliant on coal that it is difficult to capture net energy generation by 
other energy sources in the same graph. Even with significant gains in renewable energy 
production over the last two decades, most energy in the US comes from the non-renewable resources
of coal and natural gas. There were significant increases in natural gas production during the
time period examined, as advances in extraction technology made mining previously unprofitable
deposits in shale and other geologic sources feasible and productive. A map of natural gas pipelines
across the US from the EIA website captures the physical infrastructure needed to move this 
resource around the country. 


### New England Region (Connecticut, Maine, Massachusetts, New Hampshire, Rhode Island, and Vermont)
The New England region saw a steady decline in non-renewable energy generation starting in 2010, 
with a slow but steady increase in renewable energy use. However, this trend was not consistent for every 
state across the region, Connecticut seeing a significant gap between renewable and non-renewable
energy production and an overall increase in non-renewables. While the majority of energy generation
in Connecticut comes from natural gas and nuclear, it should be noted that Connecticut does not have
any fossil fuel energy reserves and sources much of these non-renewables from out-of-state. 
Connecticut's energy use can be contrasted against Vermont, highlighting the role that state policy
initiatives can play in energy generation. Vermont saw a swift drop in non-renewable energy generation
between 2015-2016, with the closure of the Yankee Nuclear Power Station at the end of 2014 resulting
in a drastic shift to more hydropower. Vermont currently generates the bulk of its energy from hydropower
sources in Canada, which has its own set of environmental impacts. 

### Mountain Region (Arizona, Colorado, Idaho, Montana, Nevada, New Mexico, Utah, and Wyoming)
Similar to other regions, the Mountain region is dependent primarily on coal (51% of production), 
and natural gas (21% of production). Over the 2001-19 period, the Mountain region had higher renewable 
energy as a percent of total production (19%), than the nation as a whole (16%). The mountain state 
with the highest percentage renewable energy production is Idaho, with about 85% of its energy being 
renewable. This is due to hydroelectric power infrastructure. 

### South Atlantic Region (Delaware, District of Columbia, Florida, Georgia, Maryland, North Carolina, South Carolina, Virginia, and West Virginia)
Renewable energy is rising slowly in the South Atlantic region, with the region showing a steady 
increase from 2011-2019. Following trends in the US as a whole, the South Atlantic region saw
a steady move from coal to natural gas, with renewable energy generation rising more slowly. At the
current rate of change, it will take until 2452 for the South Atlantic region to reach 100% renewable
energy production. Within the region, natural gas is has become the predominant source, though the 
mixture is more varied in Florida and Virginia. Delaware has moved to almost entirely natural gas. 
This is also related to the availability of natural gas with the plethora of pipelines in this region.

### Pacific Coast Region (Washington, California, Oregon, Nevada, Alaska, Hawaii, and Arizona)  
Renewable energy use is rising slowly in the Pacific region, with an increase in 
renewable energy production over the time period captured in the data. However, renewable energy
production still remains only a small percentage of total energy generation, fluctuating at a 
consistent rate of production. 

### East Midwest/East North Central Region (Illinois, Indiana, Michigan, Ohio, and Wisconsin)
Coal is overwhelmingly the primary energy source in the East Midwestern portion of the US, with
natural gas the second largest energy source. Wind and what is listed as other renewables (solar,
etc.) are the largest renewable energy souorces, though energy production by renewables fluctuated 
wildly between 2012-2017. Current analysis shows a steady increase in wind energy production 
in the region. 


### Air Pollution Trends
The EPA AQS API was used to generate a heatmap of carbon monoxide readings in parts per million (PPM)
for across the US. The largest source of carbon monoxide air pollution is vehicles and combustion engines,
with the hottest spots in the continental 48 found at major urban centers. However, the heatmap readout
can appear skewed due to monitoring locations. Some states have more monitoring locations, which might make it
appear that there is more carbon monoxide.



### Analysis
## Does Energy Source Impact Air Pollution?      
Although the US has made strides in moving towards renewables, it remains heavily dependent on coal 
and natural gas to meet energy demands - both energy sources that contribute significantly to climate
change. Our project would require more and different data sources in order to draw a clear link between 
reductions in air pollution and increased renewables. Air pollution also does not recognize political borders
and can remain in the atmosphere years after emission, further complicating efforts to determine a link
between increases in renewable energy use and reductions in air pollution.   

The correlation between increase in renewable energy and carbon monoxide levels in California is -0.351, 
indicating a weak negative relationship. A steady decline in the maximum mean value of PPM air pollution 
from carbon monoxide can be seen from 2016-2020, most likely due to stricter regulations on vehicles.      

More broadly, when evaluating the environmental impact of different energy sources, it is important to 
keep the entire lifecycle of fuel production technology in mind. Solar photovoltaic cells require rare
earth metals to generate energy, and how these materials are both harvested and disposed of can have 
significant environmental impacts. Hydropower dams can also drastically alter the river that is harnessed,
with significant impacts on both the local environment and populations that depend on that water further
downstream. 

Storage continues to be a challenge, as well as an outdated grid system that favors large producers. 
It is difficult to draw any conclusions about the relationship between energy production and 
contributions to climate change by the US with the data we're working with given the complex global energy 
market and how energy sources are exported to countries with vastly different energy policies. For example, 
the US exports a large percentage of coal to India, which has much lower standards for coal-fired power plants. 

Looking ahead, moving away from nonrenewable energy sources to renewables will require policy initiatives 
at the state and federal level. Data analysis questions this project does not address include:
1. The relationship between air pollution levels and related human health issues, and the overall cost of these 
health problems to society.
2. Potential economic gains from fewer public health problems after switching to more renewable energy sources.    
3. Issues related to the cost of renewable energy production in the present and financial gains in the future from
reducing the threat of climate change.
4. A more detailed analysis of different air pollutants, including an analysis of air pollution from energy production, 
such as CO2 and SOx. 
5. Reductions in air pollution from the COVID lockdown and how these can be used to project future financial gains 
by switching to more renewables, which is the question that prompted this project.   
 
      
### Project Challenges
We faced significant challenges in simply finding usable data sources, both in the CSV file and with the API. We had 
to abandon the first CSV file that we generated for the project that broke down energy use by month over the same
time period due to the massive amount of formatting that would have been required to make the file usable. The file that
we ended up using for the project still required a significant amount of cleaning and formatting to be usable, as the
state/region and energy source were lumped in the same column in the original file and the megawatts in the year columns
were stored as objects and not integers. We were also surprised by how difficult it was to find data on energy use sources.
The AQS API also proved difficult to access for 1) the United States as a whole and 2) for multiple parameters. 
The API was also limited to only generating reports for a single year, making it overwhelmingly difficult to generate air 
pollution data for the same time period as covered in the CSV file. 
