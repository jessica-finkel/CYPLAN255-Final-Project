# YIGBY in Berkeley and the San Francisco Bay Area

## Background
Add: Map of California with Zoom to Berkeley (render in GIS + Adobe)
_Berkeley is a city of approximately 120,000 people in Alameda County, California.[^1]_  

With a median household income of $85,530, compared to $75,235 in California as a whole, Berkeley is a relatively affluent, high opportunity area. However, wealth is distributed unevenly within the city, with a growing number of residents unable to afford housing and other basic needs. Over the last two decades rising rents and property values, combined with a growing population, have produced, as the Anti-Eviction Mapping Project (AEMP) put it, “an extreme crisis of housing affordability and displacement.” In its March 2022 report, AEMP found that “between 2005-2019, the median gross rent for the city increased by over 50%,” and that “the average rent in Berkeley in 2019 was approximately $3,165 per month, only affordable to a household with an annual income of $130,000 or more.” Historically Black neighborhoods and other communities of color have been most impacted by this crisis, the legacy of more than a century of exclusionary zoning and anti-development policies that continue to reinforce patterns of racial residential segregation. Decades of restrictive land use policies have limited the production of new housing in Berkeley, and especially affordable housing. The city failed to meet its Regional Housing Needs Allocation (RHNA) goals for the 2007-2014 period, building just over 50% of its total allocated 2,431 units. Of those constructed, less than 14% (163 units) were affordable to very low- or low-income households.

Amid growing public concern about the lack of affordable housing, homelessness, and ongoing gentrification and displacement, local policymakers are urgently searching for opportunities to add to the city's housing stock, particularly for seniors, people with disabilities, and other underserved populations. In this context, one recently completed housing development points to a promising strategy: enabling churches, synagogues, and other religious institutions to convert underutilized parking lots, buildings, and other facilities into affordable housing.  

**Jordan Court**, located in North Berkeley and opened in March 2022, was developed through a joint venture partnership betweep All Souls Episcopal Parish (All Souls), an inclusive, progressive church, and Satellite Affordable Housing Associates (SAHA). Providing much-needed senior housing, the building contains 34 affordable studios for senior residents earning 20-60% of the Area Median Income (AMI), along with an on-site manager's unit and space for All Souls' use. 

<img src="http://www.allsoulsparish.org/wp-content/uploads/cache/2015/10/church-on-cedar/1459840523.jpg" width="300"> <img src="https://user-images.githubusercontent.com/98304807/167351158-ad1787e4-2a98-4e27-a139-f59571d83911.jpg" width="300"> <img src="https://user-images.githubusercontent.com/98304807/167351214-492b73b6-5a84-47c9-836a-06ac3367d3c9.JPG" width="300"> <img src="https://user-images.githubusercontent.com/98304807/167347373-ae42b5d9-5609-4f75-895a-6698ab839d60.JPG" width="300"> <img src="https://user-images.githubusercontent.com/98304807/167347490-e3fcce3e-8d63-4ee4-973a-2ea834595f16.JPG" width="300"> <img src="https://user-images.githubusercontent.com/98304807/167347453-dbc26e4a-6f16-4d9b-9971-404d1580ef09.jpeg" width="300">

_From left to right:_  
_Top Row: All Souls Main Building (source: All Souls' website), Site Pre-Redevelopment (source: Google), Old Parish House (source: Google);_  
_Bottom Row: Jordan Court, Looking West from All Souls towards Jordan Court, Courtyard between All Souls and Jordan Court (source: author)_  

When All Souls first began exploring the possibility of redeveloping a portion of its land for housing in 2014, the Parish had relatively few local examples to follow. However, in recent years a "Yes in God's Backyard" or YIGBY movement has emerged. Gathering steam since the nickname was coined in 2019, a growing number of religious institutions across California, as well as other high-cost places like Seattle, New York City, the Washington, DC area, Atlanta, Denver, Miami, and San Antonio, are considering similar projects.  

While the motivations vary from congregation to congregation, a key factor driving this trend is a decline in membership. In part, this reflects a broader pattern of waning religiosity in the United States, as fewer people formally join religious institutions or regularly attend religious services, especially among younger generations. Yet for some institutions, particularly those in historically marginalized communities, this decline has been exacerbated as rising housing costs and gentrification displace their congregants and staff. The drop in membership has left many religious institutions land rich and cash poor, with valuable land assets but lacking the financial resources and demand to maintain and improve their facilities.  

## Research Question  
In researching Jordan Court and the YIGBY movement, I found that there is significant and growing interest in this model among congregations and policymakers in California, but information is difficult to find. Information is decentralized and largely shared informally via word-of-mouth, making it challenging to identify patterns, pitfalls, and successful policy or programmatic initiatives related to this model. In addition, several people I interviewed observed that many of the congregations pursuing this path are majority-Black churches in neighborhoods facing heavy displacement pressure. 

These findings guided my research question for this project:

**Are there sociospatial patterns with respect to the congregations in the Bay Area that are pursuing housing development on their property? In particular, do the data support the anecdotal evidence that majority-Black churches are driving this trend?** 

## Methodology
To explore this question, I relied on several key data sources, including:
- 2019 5-year American Community Survey data by census tract
  - Table S1901 (Income in the Past 12 Months)  
  - Table B03002 (Hispanic or Latino Origin by Race)  
  - Table S0101 (Age and Sex)
- California Tax Credit Allocation Committee 2022 Opportunity Map data
- City of Berkeley data
  - Parcel Data
  - Zoning Data  

I also compiled a novel dataset of "YIGBY Congregations" based on news reports, press statements, interviews, blog posts, and social media. After gathering the information, I used the Mapbox API to geocode the addresses then used Shapely to create point geometry for each site. For the purpose of this project, I have limited the dataset to congregations in Alameda, Contra Costa, and Santa Clara counties. However, even within these three counties, the list is quite preliminary and incomplete. I hope to continue to build out the dataset as I continue research in this area. 



## Key Findings  
_Note: differences between census tracts may not be statistically significant._  

Berkeley is heavily segregated, and race/ethnicity is correlated with spatial patterns of wealth, opportunity, and land use. 
![Berk_dot_density_png](https://user-images.githubusercontent.com/98304807/167347178-86fc9dd2-f9b1-4543-8611-bd8286c13124.png) 
Add: Choropleth Maps of Berkeley normalized by population
Add: Opportunity Map for Berkeley
Add: Correlations between income and race/ethnicity
Add: Pop Density Map  
Add: Zoning Map showing LDR, MDR, HDR

The congregations pursuing housing on their land in Berkeley and the Bay Area are more likely to be in low-resource and BIPOC neighborhoods.

Add: Opportunity Maps and congregations
Add: % POC Map and congregations

### Conclusions and Next Steps
TKTKT
Prototype YIGBY Map


## References
