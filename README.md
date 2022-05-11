# YIGBY in Berkeley and the San Francisco Bay Area  

*Jessica Finkel, CP255 Urban Informatics + Visualization (Spring 2022)*            

# Background  

<img align="left" src="https://user-images.githubusercontent.com/98304807/167493657-83f1a98e-de76-4a64-a7c4-33b2fa3a86d0.png" width="300" style="float:left; padding-right:10px"> Berkeley is a city of approximately 120,000 people in the San Francisco Bay Area. With a median household income of $85,530, compared to $75,235 in California as a whole, Berkeley is a relatively affluent, high opportunity area. However, wealth is distributed unevenly within the city, with a growing number of residents unable to afford housing and other basic needs. Over the last two decades rising rents and property values, combined with a growing population, have produced, as the Anti-Eviction Mapping Project (AEMP) put it, “an extreme crisis of housing affordability and displacement.” In its March 2022 report, AEMP found that “between 2005-2019, the median gross rent for the city increased by over 50%,” and that “the average rent in Berkeley in 2019 was approximately $3,165 per month, only affordable to a household with an annual income of $130,000 or more.” Historically Black neighborhoods and other communities of color have been most impacted by this crisis, the legacy of more than a century of exclusionary zoning and anti-development policies that continue to reinforce patterns of racial residential segregation. Decades of restrictive land use policies have limited the production of new housing in Berkeley, and especially affordable housing. The city failed to meet its Regional Housing Needs Allocation (RHNA) goals for the 2007-2014 period, building just over 50% of its total allocated 2,431 units. Of those constructed, less than 14% (163 units) were affordable to very low- or low-income households. Amid growing public concern about the lack of affordable housing, homelessness, and ongoing gentrification and displacement, local policymakers are urgently searching for opportunities to add to the city's housing stock, particularly for seniors, people with disabilities, and other underserved populations.  
  
In this context, one recently completed housing development points to a promising strategy: enabling churches, synagogues, and other religious institutions to convert underutilized parking lots, buildings, and other facilities into affordable housing. **<a href="https://jessica-finkel.github.io/CYPLAN255-Final-Project/explore_map.html" target="_blank">Jordan Court</a>**, located in North Berkeley and opened in March 2022, was developed through a joint venture partnership betweep All Souls Episcopal Parish (All Souls), an inclusive, progressive church, and Satellite Affordable Housing Associates (SAHA). Providing much-needed senior housing, the building contains 34 affordable studios for senior residents earning 20-60% of the Area Median Income (AMI), along with an on-site manager's unit and space for All Souls' use.  
  
<p float="left">
  <img src="http://www.allsoulsparish.org/wp-content/uploads/cache/2015/10/church-on-cedar/1459840523.jpg" width="250" /> <img src="https://user-images.githubusercontent.com/98304807/167351158-ad1787e4-2a98-4e27-a139-f59571d83911.jpg" width="250" /> <img src="https://user-images.githubusercontent.com/98304807/167451971-eb2bdfe9-8e36-4445-8bd3-6f8226a9ab72.JPG" width="250" />
</p>
<p float="left">
  <img src="https://user-images.githubusercontent.com/98304807/167347373-ae42b5d9-5609-4f75-895a-6698ab839d60.JPG" width="250" /> <img src="https://user-images.githubusercontent.com/98304807/167347490-e3fcce3e-8d63-4ee4-973a-2ea834595f16.JPG" width="250" /> <img src="https://user-images.githubusercontent.com/98304807/167452238-b82dc126-5221-4962-a2e8-17b0d8b63ba2.jpeg" width="250" />
</p>

 *From top left to bottom right: All Souls Main Building (source: All Souls); Previous Site Layout (source: Google, via Berkeleyside); Old Parish House, 2015 (source: Google); Jordan Court (source: author); All Souls Next to Jordan Court (source: author); Jordan Court Courtyard (source: All Souls)* 

When All Souls first began exploring the possibility of redeveloping a portion of its land for housing in 2014, the Parish had relatively few local examples to follow. However, in recent years a "Yes in God's Backyard" or YIGBY movement has emerged. Gathering steam since the nickname was coined in 2019, a growing number of religious institutions across California, as well as other high-cost places like Seattle, New York City, the Washington, DC area, Atlanta, Denver, Miami, and San Antonio, are considering similar projects. While the motivations vary from congregation to congregation, a key factor driving this trend is a decline in membership. In part, this reflects a broader pattern of waning religiosity in the United States, as fewer people formally join religious institutions or regularly attend religious services, especially among younger generations. Yet for some institutions, particularly those in historically marginalized communities, this decline has been exacerbated as rising housing costs and gentrification displace their congregants and staff. The drop in membership has left many religious institutions land rich and cash poor, with valuable land assets but lacking the financial resources and demand to maintain and improve their facilities.  
  
  
# Research Question  

In researching Jordan Court and the YIGBY movement for my capstone project, I found that there is significant and growing interest in this model among congregations and policymakers in California, but information is difficult to find. Information is decentralized and largely shared informally via word-of-mouth, making it challenging to identify patterns, pitfalls, and successful policy or programmatic initiatives related to this model. In addition, several people I interviewed observed that many of the congregations pursuing this path are majority-Black churches in neighborhoods facing heavy displacement pressure. I also learned that exclusionary zoning and land use barriers frequently pose an obstacle for congregations looking to redevelop their land. These findings guided my research question for this project:

Are there sociospatial patterns with respect to the congregations in the Bay Area that are pursuing housing development on their property? In particular, do the data support the anecdotal evidence that majority-Black churches are driving this trend?

  
# Methodology

To explore this question, I relied on the following datasets:
- 2019 5-year American Community Survey data, by census tract (accessed via API)
  - Table S1901 (Income in the Past 12 Months)  
  - Table B03002 (Hispanic or Latino Origin by Race)  
  - Table S0101 (Age and Sex)
- California Tax Credit Allocation Committee 2022 Opportunity Map (hosted by the Othering and Belonging Institute)
- City of Berkeley Parcels and Zoning data (downloaded) 
- Alameda County Assessor's Office Land Use Codes 
- A novel dataset of "YIGBY Congregations"  

I used a Python Jupyter Notebook to complete my analysis, relying on a variety of libraries, particularly Matplotlib, Seaborn, Pandas, Geopandas, Shapely, Contextily, and Folium.

A few notes about my approach to the data:

- Using code adapted from **<a href="https://github.com/agaidus/census_data_extraction/blob/master/census_mapper.py" target="_blank">here</a>** and **<a href="https://github.com/LucyMakesMaps/COVID_VaccineClinics/blob/main/Notebooks/DotMap.ipynb" target="_blank">here</a>**, I created a dot density map of demographics in Berkeley. It reflects 2019 5-year ACS race/ethnicity data at the census tract level retrieved from the Census Bureau's API. I chose to focus only on four race/ethnicity categories, non-Hispanic White, non-Hispanic Black, non-Hispanic Asian, and Hispanic (referred to throughout this page as White, Black, Asian, and Hispanic, respectively) because the population identifying as other categories was too small to read clearly on the map. I clipped the map to an administrative boundary layer, which cut off additional dots in the western-most tract extending into the water. It would have been better to clip the map before generating the dots for that census tract polyon; however, this tract has a very small total population and this did not significantly change the information in the map. Following **<a href="https://www.axismaps.com/guide/dot-density" target="_blank">best practice</a>**, I projected the dot density map to EPSG 5070, which is an Albers Equal Area projection using the NAD 83 Datum.  

- Aside from the dot density map, all of the maps below are projected to EPSG 2227. The series of choropleth maps reflects census tract-level data. It may have been better to use block group-level data, but I was concerned about high margins of error if I used a smaller geography. I did not conduct statistical testing for this project; therefore, apparent differences across census tracts may not be statistically significant.  

- The zoning data available through Berkeley's online data portal includes inconsistencies and does not strictly align with the City's zoning ordinance. The original dataset included 10 zone designations codes and 39 unique "zone class" category codes, some for which I could not find a definition. For the purpose of this project, I created my own "zoning' classification with 8 categories: low-density residential, medium-density residential, high-density residential, mixed use-residential, mixed use-light industrial, commercial, manufacturing, and other. In general, "Low density residential" includes R-1 zone classes, "medium density residential" includes R-2 zone classes, and "high density residential" includes R-3, R-4, and R-5 zone classes. "Commercial" includes neighborhood commercial areas, commercial corridors, and predominately commercial areas in the downtown core.

- I compiled the list of YIGBY congregations from news reports, press statements, interviews, blog posts, and social media. These list includes congregations at various stages of the development process, from exploring options through completion. I used the Mapbox API along with Shapely to geocode the addresses of congregations in my novel dataset and create point geometry for each site. While I came across institutions in southern California and a handful in Marin County, for the purpose of this project I limited the dataset to congregations in Alameda, Contra Costa, and Santa Clara Counties. Even within these three counties, the list is quite preliminary. I hope to continue to build out the dataset as I continue research in this area, adding more congregations and more details, such as denomination, surrounding zoning designation, housing typology, and number of housing units. My goal is to create a prototype of an interactive map that congregations, policymakers, and researches could use to find centralized information about the movement and policy and programmatic initiatives to facilitate it. Initially I hoped to calculate the development potential on land coded for religious use in Berkeley, and I explored using OSMnx to gather building footprint and location data. In the end, though, I was not confident in my tagging scheme and opted against pursuing this avenue for this project. 

  
# Findings  

## Berkeley Context
  
I began by analyzing sociodemographic data for Berkeley from the Census Bureau and the Othering and Belonging Institute. As expected, I found that the city is heavily segregated and that race/ethnicity is correlated with spatial patterns of wealth, opportunity, and land use. In general, the city is predominantly White, particularly in census tracts in North Berkeley and the Berkeley Hills. Reflecting a history of redlining and exlusionary land use policies in the city, census tracts with a higher percentage of White residents are generally higher resourced, with a higher median income and lower housing density than those with a higher percentage of BIPOC residents.  

  
![berk_dot_dens](https://user-images.githubusercontent.com/98304807/167543697-243fe9fa-8bba-41d3-b702-9a45168791c0.png)  

  
![race_bw](https://user-images.githubusercontent.com/98304807/167543714-ba14eb24-a813-48b0-aa06-8ceeadf50a2b.png)
![race_ah](https://user-images.githubusercontent.com/98304807/167541867-857308db-247d-4f66-85ac-35e2115e2927.png)  

  
![berk_pop_dens](https://user-images.githubusercontent.com/98304807/167542319-cf8012c9-5538-4d63-ba54-f6762c0e731b.png)
  
  
<img src="https://user-images.githubusercontent.com/98304807/167546058-d9b101af-84c2-4c91-8318-68ceacfd5f43.png" width="500" /> <img src="https://user-images.githubusercontent.com/98304807/167546173-533e9aba-b8f2-49f3-b39b-a0654ff693dc.png" width="500" />  
 
  
![berk_opp](https://user-images.githubusercontent.com/98304807/167545655-3874a069-af10-4d87-8813-42a284f14edd.png)


Berkeley is an extremely residential city, and most neighborhoods are zoned for low- and medium-density housing.


![berk_zoning_x](https://user-images.githubusercontent.com/98304807/167708123-31edb20d-cce8-4955-aee7-d7e11600ed5a.png)  
(Note: Unless disaggregated, "mixed use" includes both mixed use-residential and mixed use-light industrial.)

## YIGBY in Berkeley

According to data from the Alameda County Assessor's Office, there are 104 religious use parcels in Berkeley. Not surprising given that most of the city is zoned for residential use, the majority of these sites are in residential areas, and particularly in areas zoned for medium-density housing. Exclusionary zoning has historically limited affordable housing production in California, but recent legislative initiatives like SB 35 seek to overcome this barrier. Effective as of January 1, 2018, cities in California not meeting their housing production goals under RHNA must grant ministerial approval to housing developments on sites zoned for residential or mixed use that meet certain affordability thresholds. My analysis suggests that 73% (76 total) religious use parcels are in areas zoned residential, with another 7% (7 total) zoned for mixed use. Notably, another 20% (21 total) religious use parcels are in areas zoned commercial. While there are limitations in my analysis due to the way I coded zoning categories, this suggests that at least some congregations would face challenges building affordable housing. SB 899 (D-Wiener) would have expanded on SB 35 by giving ministerial approval to certain affordable housing projects on land owned by religious institutions in areas zoned for commercial use, in addition to residential or mixed use, but it failed to pass the California legislature in 2020. 

![relig_x_zone](https://user-images.githubusercontent.com/98304807/167708332-c4e4f3e9-b299-4330-a3e2-496a4fe21eee.png)

![congreg_countxzone](https://user-images.githubusercontent.com/98304807/167721792-9a804198-92be-4d53-827e-f5a174b89ff9.jpg)  

(Note: Areas zoned manufacturing, other, and mixed use-light industrial did not contain any religious use parcels and are not included in this chart.)

![congreg_zoningtype](https://user-images.githubusercontent.com/98304807/167721771-23c3b14b-df56-424b-aaf4-da835954ed58.png)

My dataset of YIGBY congregations only contains 5 congregations in Berkeley thus far, but they are noticeably concentrated in South Berkeley. This aligns with recent reports such as **<a href="https://www.berkeleyside.org/2022/03/13/south-berkeley-black-churches-are-building-affordable-housing-on-their-properties" target="_blank">this article</a>** from Berkeleyside, which noted that several South Berkeley Black churches are looking to redevelop their sites into affordable housing to combat intense gentrification and displacement. 

![berk_congs](https://user-images.githubusercontent.com/98304807/167738365-146756d5-c741-44be-8c72-1869c0bc6e45.png)


## YIGBY in East Bay  

**Still a work in progress, but <a href="https://jessica-finkel.github.io/CYPLAN255-Final-Project/east_bay_yigby.html" target="_blank">click here to explore congregations building housing on their land!</a>**

My preliminary list of YIGBY congregations in Alameda, Contra Costa, and Santa Clara Counties included 31 religious institutions. The maps below suggest a growing YIGBY movement, particularly in Alameda County. However, this could also reflect the fact that there is more information available about congregations pursuing this model. In particular, Alameda County funds a Housing Development Capacity Building Program for faith-based and community-based organizations, and LISC Bay Area, which manages the program, has published information about its participants online. Thus far the program has served two cohorts, with 7 faith-based groups in the first and 10 in the second. The maps also suggest that congregations building affordable housing are largely in low-resource areas and census tracts with a relatively high BIPOC population, but additional data on income, rent burden, development potential, and other factors would help tease out any true correlations and explain differences between, for example, census tracts along the bay and those farther inland.


<img src="https://user-images.githubusercontent.com/98304807/167752803-bf415090-b974-4151-89d8-31534779691a.png" width="700" />  

![alameda_congs](https://user-images.githubusercontent.com/98304807/167745303-4daf5556-597a-4515-90f4-7badb8b91f29.png)
![costa_congs](https://user-images.githubusercontent.com/98304807/167745320-30c826d8-5464-4a23-a039-03595781f81b.png)
![clara_congs](https://user-images.githubusercontent.com/98304807/167745333-ea363614-5c58-448c-b27f-b3c686c5cb55.png)
 
![HDCPB_final](https://user-images.githubusercontent.com/98304807/167752834-fae59342-cca6-4a0d-8bf0-1fc80cb5e8dc.png)  
  
# Next Steps  
  
With more time, I would have liked to deepen my analysis of the racial and social equity implications of this movement, as well as expand my analysis of congregations that might face zoning barriers to redeveloping their property into affordable housing. I would also like to build out the interactive map of institutions with more congregations and more information about each one. Local jurisdictions across California are exploring or implementing policy and programmatic initiatives such as affordable housing overlays on religious land, reduced minimum parking requirements, and capacity-building programs like the one in Alameda County to facilitiate this model as they face pressure from the state to meet RHNA targets. I hope to add these initiatives to the map as a resource to policymakers. It also would have been interesting to add transit data to the map and conduct a network analysis of the YIGBY sites, as well as to include more charts summarizing, for example, the status of projects in the development process (e.g., how many are exploring feasibility, obtaining entitlements, in construction, and completed).

# Acknowledgements  

I am indebted to my classmates Sydney Maves, Molly Sun, and Matthew Hui for their help troubleshooting code for this project. I also owe extra dishwashing shifts to my partner for helping me compile my list of YIGBY congregations. 

## References

Barber, Jesse. “Berkeley Zoning Has Served for Many Decades to Separate the Poor from the Rich and Whites from People of Color.” Berkeleyside (blog), March 12, 2019. https://www.berkeleyside.org/2019/03/12/berkeley-zoning-has-served-for-many-decades-to-separate-the-poor-from-the-rich-and-whites-from-people-of-color.

Enterprise Community Partners. “Bringing Faith-Based Development Nationwide,” February 24, 2022. https://www.enterprisecommunity.org/blog/bringing-faith-based-development-nationwide.
———. Public/Private Funding Sources for Faith-Based Development. “Feeding Faith Leaders with Community Fervor” Fall Webinar Series, 2021. https://www.enterprisecommunity.org/resources/feeding-faith-leaders-community-fervor-fbdi-webinar-series-12296.

Garcia, David, and Eddie Sun. “Mapping the Potential and Identifying the Barriers to Faith-Based Housing Development,” May 2020, 23. https://ternercenter.berkeley.edu/wp-content/uploads/2020/08/Mapping_the_Potential_and_Identifying_the_Barriers_to_Faith-Based_Housing_Development_May_2020.pdf.

The Anti-Eviction Mapping Project. “Densifying Berkeley: Potential Impacts on Displacement and Equity,” March 2022. https://www.berkeleyside.org/wp-content/uploads/2022/04/AEMP-UpzoningReport-Draft4-3.pdf.

Menendian, Stephen, Samir Gambhir, Karina French, and Arthur Gailes. “Single-Family Zoning in the San Francisco Bay Area: Characteristics of Exclusionary Communities.” Othering & Belonging Institute, October 2020. https://belonging.berkeley.edu/single-family-zoning-san-francisco-bay-area.

City of Berkeley. “2015-2023 Berkeley Housing Element,” April 28, 2015. https://www.cityofberkeley.info/uploadedFiles/Planning_and_Development/Level_3_-_Commissions/Commission_for_Planning/2015-2023%20Berkeley%20Housing%20Element_FINAL.pdf.

