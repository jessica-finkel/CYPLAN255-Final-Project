# YIGBY in Berkeley and the San Francisco Bay Area

Final Project for CP255 Urban Informatics + Visualization (Spring 2022)  |  Jessica Finkel  |  5.9.2022


## Background

<img align="left" src="https://user-images.githubusercontent.com/98304807/167493657-83f1a98e-de76-4a64-a7c4-33b2fa3a86d0.png" width="300" style="float:left; padding-right:10px"> Berkeley is a city of approximately 120,000 people in the San Francisco Bay Area. With a median household income of $85,530, compared to $75,235 in California as a whole, Berkeley is a relatively affluent, high opportunity area. However, wealth is distributed unevenly within the city, with a growing number of residents unable to afford housing and other basic needs. Over the last two decades rising rents and property values, combined with a growing population, have produced, as the Anti-Eviction Mapping Project (AEMP) put it, “an extreme crisis of housing affordability and displacement.” In its March 2022 report, AEMP found that “between 2005-2019, the median gross rent for the city increased by over 50%,” and that “the average rent in Berkeley in 2019 was approximately $3,165 per month, only affordable to a household with an annual income of $130,000 or more.” Historically Black neighborhoods and other communities of color have been most impacted by this crisis, the legacy of more than a century of exclusionary zoning and anti-development policies that continue to reinforce patterns of racial residential segregation. Decades of restrictive land use policies have limited the production of new housing in Berkeley, and especially affordable housing. The city failed to meet its Regional Housing Needs Allocation (RHNA) goals for the 2007-2014 period, building just over 50% of its total allocated 2,431 units. Of those constructed, less than 14% (163 units) were affordable to very low- or low-income households.

Amid growing public concern about the lack of affordable housing, homelessness, and ongoing gentrification and displacement, local policymakers are urgently searching for opportunities to add to the city's housing stock, particularly for seniors, people with disabilities, and other underserved populations. In this context, one recently completed housing development points to a promising strategy: enabling churches, synagogues, and other religious institutions to convert underutilized parking lots, buildings, and other facilities into affordable housing. Jordan Court, located in North Berkeley and opened in March 2022, was developed through a joint venture partnership betweep All Souls Episcopal Parish (All Souls), an inclusive, progressive church, and Satellite Affordable Housing Associates (SAHA). Providing much-needed senior housing, the building contains 34 affordable studios for senior residents earning 20-60% of the Area Median Income (AMI), along with an on-site manager's unit and space for All Souls' use. 

**Jordan Court Photos**

<p float="left">
  <img src="http://www.allsoulsparish.org/wp-content/uploads/cache/2015/10/church-on-cedar/1459840523.jpg" width="300" /><img src="https://user-images.githubusercontent.com/98304807/167351158-ad1787e4-2a98-4e27-a139-f59571d83911.jpg" width="300" /><img src="https://user-images.githubusercontent.com/98304807/167451971-eb2bdfe9-8e36-4445-8bd3-6f8226a9ab72.JPG" width="300" />
</p>
<p float="left">
  <img src="https://user-images.githubusercontent.com/98304807/167347373-ae42b5d9-5609-4f75-895a-6698ab839d60.JPG" width="300" /><img src="https://user-images.githubusercontent.com/98304807/167347490-e3fcce3e-8d63-4ee4-973a-2ea834595f16.JPG" width="300" /><img src="https://user-images.githubusercontent.com/98304807/167452238-b82dc126-5221-4962-a2e8-17b0d8b63ba2.jpeg" width="300" />
</p>

 *From left to right:    
Row 1: All Souls Main Building (source: All Souls), Previous Site Layout (source: Google, via Berkeleyside), Old Parish House, 2015 (source: Google)
Row 2: Jordan Court (source: author), All Souls Next to Jordan Court (source: author), Jordan Court Courtyard (source: All Souls)* 

When All Souls first began exploring the possibility of redeveloping a portion of its land for housing in 2014, the Parish had relatively few local examples to follow. However, in recent years a "Yes in God's Backyard" or YIGBY movement has emerged. Gathering steam since the nickname was coined in 2019, a growing number of religious institutions across California, as well as other high-cost places like Seattle, New York City, the Washington, DC area, Atlanta, Denver, Miami, and San Antonio, are considering similar projects.  

While the motivations vary from congregation to congregation, a key factor driving this trend is a decline in membership. In part, this reflects a broader pattern of waning religiosity in the United States, as fewer people formally join religious institutions or regularly attend religious services, especially among younger generations. Yet for some institutions, particularly those in historically marginalized communities, this decline has been exacerbated as rising housing costs and gentrification displace their congregants and staff. The drop in membership has left many religious institutions land rich and cash poor, with valuable land assets but lacking the financial resources and demand to maintain and improve their facilities.  

## Research Question  

In researching Jordan Court and the YIGBY movement for my capstone project, I found that there is significant and growing interest in this model among congregations and policymakers in California, but information is difficult to find. Information is decentralized and largely shared informally via word-of-mouth, making it challenging to identify patterns, pitfalls, and successful policy or programmatic initiatives related to this model. In addition, several people I interviewed observed that many of the congregations pursuing this path are majority-Black churches in neighborhoods facing heavy displacement pressure. I also learned that exclusionary zoning and land use barriers frequently pose an obstacle for congregations looking to redevelop their land. 

These findings guided my research question for this project:

**Are there sociospatial patterns with respect to the congregations in the Bay Area that are pursuing housing development on their property? In particular, do the data support the anecdotal evidence that majority-Black churches are driving this trend?** 

## Methodology

To explore this question, I relied on the following datasets:
- 2019 5-year American Community Survey data, by census tract (accessed via API)
  - Table S1901 (Income in the Past 12 Months)  
  - Table B03002 (Hispanic or Latino Origin by Race)  
  - Table S0101 (Age and Sex)
- California Tax Credit Allocation Committee 2022 Opportunity Map (hosted by the Othering and Belonging Institute)
- City of Berkeley Parcels and Zoning data (downloaded) 
- Alameda County Assessor's Office Land Use Codes 
- A novel dataset of "YIGBY Congregations" in Alameda, Contra Costa, and Santa Clara Counties that I compiled from news reports, press statements, interviews, blog posts, and social media

I used Python in Jupyter Notebook to complete my analysis, relying on a variety of Python libraries, including among others Matplotlib, Seaborn, Pandas, Geopandas, Contextily, and Folium. I also used the Mapbox API along with Shapely to geocode the addresses of congregations in my novel dataset and create point geometry for each site. I explored using OSMnx to gather building footprint and location data for congregations in Berkeley, but I was not confident in my tagging scheme and opted against using it in the end. I supplemented work in Python with ArcGIS to troubleshoot projection issues and Adobe Illustrator to modify legends and image sizing. 

Using code adapted from https://github.com/agaidus/census_data_extraction/blob/master/census_mapper.py and https://github.com/LucyMakesMaps/COVID_VaccineClinics/blob/main/Notebooks/DotMap.ipynb, I created a dot density map of demographics in Berkeley. It reflects 2019 5-year ACS race/ethnicity data at the census tract level retrieved from the Census Bureau's API. I chose to focus only on four race/ethnicity categories, non-Hispanic White, non-Hispanic Black, non-Hispanic Asian, and Hispanic (referred to throughout this page as White, Black, Asian, and Hispanic, respectively) because the population identifying as other categories was too small to read clearly on the map. I clipped the map to an administrative boundary layer, which cut off additional dots in the western-most tract extending into the water. It would have been better to clip the map before generating the dots for that census tract polyon; however, this tract has a very small total population and this did not significantly change the information in the map. Following best practice, I projected the dot density map to EPSG 5070, which is an Albers Equal Area projection using the NAD 83 Datum.  

The series of choropleth maps reflects the percent of residents in each category normalized over the total population in each census tract. It would have been better to use block group-level data, but I was concerned about high margins of error if I used a smaller geography. Aside from the dot density map, all of the maps are projected to EPSG 2227. 

## Key Findings  
_Note: differences between census tracts may not be statistically significant._  

I began by analyzing sociodemographic data for Berkeley from the Census Bureau and the Othering and Belonging Institute. As expected, I found that the city is heavily segregated and that race/ethnicity is correlated with spatial patterns of wealth, opportunity, and land use. In general, the city is predominantly White, particularly in census tracts in North Berkeley and the Berkeley Hills. The direct result of the history of redlining and exlusionary land use policies in the city, census tracts with a higher percentage of White residents are generally higher resourced, with a higher median income and lower housing density than those with a higher percentage of BIPOC residents.   

![berk_dot_dens](https://user-images.githubusercontent.com/98304807/167543697-243fe9fa-8bba-41d3-b702-9a45168791c0.png)  


![race_bw](https://user-images.githubusercontent.com/98304807/167543714-ba14eb24-a813-48b0-aa06-8ceeadf50a2b.png)
![race_ah](https://user-images.githubusercontent.com/98304807/167541867-857308db-247d-4f66-85ac-35e2115e2927.png)  
![berk_pop_dens](https://user-images.githubusercontent.com/98304807/167542319-cf8012c9-5538-4d63-ba54-f6762c0e731b.png)

<img src="https://user-images.githubusercontent.com/98304807/167546058-d9b101af-84c2-4c91-8318-68ceacfd5f43.png" width="500" /> <img src="https://user-images.githubusercontent.com/98304807/167546173-533e9aba-b8f2-49f3-b39b-a0654ff693dc.png" width="500" />  
 
![berk_opp](https://user-images.githubusercontent.com/98304807/167545655-3874a069-af10-4d87-8813-42a284f14edd.png)


Berkeley has an aging population, with a growing number of residents reaching retirement age. All Souls took this into account when it began exploring options for redeveloping the Old Parish House and parking lot, ultimately deciding to focus on affordable senior housing. This was also a strategic choice to minimize neighborhood opposition to the project. 

![berk_seniors](https://user-images.githubusercontent.com/98304807/167546872-f4441d69-734a-41df-8350-1efafb32ebf6.png)




Add: Zoning Map showing LDR, MDR, HDR

The congregations pursuing housing on their land in Berkeley and the Bay Area are more likely to be in low-resource and BIPOC neighborhoods.

Add: Opportunity Maps and congregations
Add: % POC Map and congregations

## Conclusions and Next Steps
TKTKT
Prototype YIGBY Map

**[click here:](https://jessica-finkel.github.io/CYPLAN255-Final-Project/explore_map.html)** 

## Acknowledgements
I am indebted to my classmates Sydney Maves, Molly Sun, and Matthew Hui for their help troubleshooting code for this project. I also owe extra dishwashing shifts to my partner Drew Liming for doing research to flesh out my list of YIGBY congregations.  

## References
