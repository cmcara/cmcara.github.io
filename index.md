
### Currently studying Earth Data Analytics at CU Boulder. Some of the projects I have worked on are listed below and linked for further detail. ###

---

### First Interactive Map ###
This is a map generated in Python of the University of Virginia in Charlottesville, VA where I completed my undergrad studies.

<embed type="text/html" src="img/uva.html" width="600" height="490">

### OLS Regression on Charlottesville Daily Max Temperature Data ###
<embed type="text/html" src="img/cville_int_plot (3).html" width="850" height="320"> 
![Regression](img/cville_climate_reg_full (2).jpeg)
  
Using daily data pulled from NOA and resampled on an annual basis, I ran an OLS regression on temperature data in Charlottesville dating back to 1893. I found a minor positive correlation showing an increase of 0.00033993 degrees/year. This value lags behind most estimates of average annual temperature increase by multiple orders of magnitude ([Link](https://www.climate.gov/news-features/understanding-climate/climate-change-global-temperature)), but the more surprising result of this exercise was the variability I encountered when implementing different cut-offs for which years to include in the data. Given that some years in the data do not have a complete record for each day in that year, there is some bias in resampling each year by a mean value and considering all years' means equallly, but when I implemented different cutoffs to refine my results, I started seeing negative values contrary to expectations. [Read more about the process here](projects/cville_regression_project.html)

### Plotting Annual Migration for Ring-Necked Ducks

<div style="width: 600px; height: 505px;">
  <iframe src="img/na_migration.html" style="width: 100%; height: 100%; transform: scale(0.5); border: none;"></iframe>
</div>

I have always been fascinated by watching ducks fly, and in central Virginia where I grew up, one of the most prevalent species during the winter migration is the ring-necked duck ([Aythya collaris](https://en.wikipedia.org/wiki/Ring-necked_duck)). Using GBIF and ecoregions data, I plotted their migration patterns globally and focused on North America for the 2024 year. They are an often-overlooked species compared to the much more vibrant mallard or wood duck, but we see a lot of them and they have a particularly entertaining flight pattern. Ring-necked ducks should be called ring-billed ducks however. The white bands around their bills are much more pronounced than the barely visible crimson neckband for which they are allegedly named. My grandfather referred to the birds exclusively as ring-bills and it took me years to sort everything out as a child. Regardless of naming convention, I was surprised just how widespread these ducks are. Japan in particular was interesting, and I would assume they spend the warmer spring and summer months in more northern areas without sufficient data collection coverage. I was also not expecting there to be as many ecoregions in the continental US that maintained a population year round and would be interested to run the experiment again on North America with a higher resolution ecoregion map, particularly around the eastern and Mississippi flyways. [Read more about the process here](projects/ringneck_migration_project.html)


### Analyzing Vegetation Levels in the Gila River Indian Community

<div style="width: 1200px; height: 505px;">
  <iframe src="img/ndvi_diff_plot_new.html" style="width: 100%; height: 100%; border: none;"></iframe>
</div>

In 2004, the Arizona Water Settlements Act took a major step in compensating for over a century of injustice concerning the water rights of the Gila River Indian Community south of Phoenix. Established in 1859 as the first reservation in Arizona, the GRIC quickly began seeing Gila River flows diminished due to upstream dams and diversions which put historic agricultural lands and practices at risk. For decades, Tribal leaders engaged federal and state lawmakers in an effort to restore and secure sufficient water access for their people, but progress was slow. The GRIC [website](https://www.gilariver.org/index.php/about/history) and the First Nations Development Institute [case study](https://www.firstnations.org/wp-content/uploads/publication-attachments/2009_NAAW_Rethinking_Asset_Building_Case_1.pdf) on the region provide a much more detailed history. The full 2004 settlement is also available [online](https://www.congress.gov/108/plaws/publ451/PLAW-108publ451.pdf). 

In order to track improvements and changes within the GRIC post settlement, I set up the above plot to compare the Normalized Difference Vegetation Index (NDVI) values of each year after 2004 to average values for the three years prior. The most concentrated change between 2005 and 2022 appears near the middle of the map around coordinates (-111.8, 33.2) which appear to be agricultural efforts. Slightly below, there is an area in the lower central area of the GRIC that has gone in the negative direction, but I can tell from the GRIC safety [website](https://www.gricsafety.org/index.php/fire-department/station-location-and-response-area) that is likely due to the growing development. Overall, there seems to be some improvement in NDVI values across the GRIC, but the urban growth of Phoenix and areas surrounding the GRIC make comparing the rates of change inside vs outside of the boundary more difficult. [Read more about the process here](projects/vegetation-project.html)


### Looking Further into Gila River NDVI compared to neighboring Salt River Indian Community

<div style="width: 600px; height: 505px;">
  <iframe src="img/overview_plot.html" style="width: 100%; height: 100%; border: none;"></iframe>
</div>

In an effort to further understand the impact of the 2004 settlement restoring water rights to the Gila River Indian Community, I set up a difference in difference comparison between NDVI values for the Gila River and Salt River Indian Communities from 2002-2022 using 2005 as a break point. As the map above shows, both the GRIC and SRIC are located outside of present-day Phoenix, AZ and have river access to their namesake waters. The people of the Salt River and Gila River share common history, ancestors, and traditions, with the Salt River Reservation established in 1879, 20 years after the Gila River to the south, due to increased migration from the GRIC as their river continued to dry up from non-native dams and diversions. The [SRIC](https://srpmic-nsn.gov/about/history/) and [GRIC](https://www.gilariver.org/index.php/about/history) keep strong histories. 

For decades, both the GRIC and SRIC fought legal battles with the federal government as their rivers dried, but due to the smaller land size and relatively less far-reaching implications, the SRIC was able to reach a water rights [settlement](https://open.uapress.arizona.edu/read/dc19d40e-ae7d-4010-a72b-337de7467d64/section/fd79c1c1-d802-403e-a696-fc863e7b5fa1#id_224) in 1988, well before the 2004 settlement impacting the GRIC. For all of these reasons, we should see similar climate and annual trends between the GRIC and SRIC prior to the 2004 settlemt primarily affecting the GRIC. The data supports the prior trends assumption on an eye-test level, but in hindsight a longer lead time on both datasets could have been helpful.

<div style="max-width: 65%; height: auto; text-align: center;">
  <img src="img/ndvi_parallel_trends.png" 
       alt="NDVI parallel trends" 
       style="max-width: 100%; height: auto; display: inline-block;">
</div>

Next I ran the DiD analysis, which should identify what, if any, effect the 2004 settlement might have had when annual trends and patterns present in both datasets are removed. Unfortunately, those annual trends, particularly in climate variability, have a large impact on vegetation growth annually and can overshadow any improvement due to water flow. Additionally increased development in the GRIC as downtown has grown would downwardly bias the mean values. The treated:post = .0085 which while positive is very weak on a 0-1 scale. 

<div style="width: 600px; height: 250px;">
  <iframe src="img/did_model_summary.html" style="width: 100%; height: 100%; border: none;"></iframe>
</div>

I have not solved how to fully mask out human development and isolate as much 'pure' vegetation as possible, but I have expanded on the last project as a step in that direction. I modified the NDVI sliding plot to now calculate a running average of NDVI values from 2005 to the year selected as compared to mean values for 2002-2004. Calculating a running average helps smooth out the data more and really highlight areas where NDVI has been consistently changing in the same direction. 

<div style="width: 600px; height: 505px;">
  <iframe src="img/gric_avg_diff_plot.html" style="width: 100%; height: 100%; border: none;"></iframe>
</div>

The restoration of water right from the settlement has certainly led to [improvement](https://nativesciencereport.org/2021/12/bringing-a-river-back-to-life/#:~:text=At%20a%202015%20conference%20on,segment%20of%20the%20Gila%20River.) for the local communities, and overcoming challenges to quantify those benefits helps justify similar actions elsewhere. [Read more about the process and potential next steps here.](project/gric_sric_project.html)

----------

## About Me ##
WIP

<img 
  src="/img/Fish Picture.png" 
  alt="Test image of me holding a fish" 
  width="40%">
  
### Contact ###
* Email - <Charlie.Caravati@colorado.edu>
* GitHub - [cmcara](https://github.com/cmcara)
