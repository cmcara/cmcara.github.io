
### Currently studying Earth Data Analytics at CU Boulder. Some of the projects I have worked on are listed below and linked for further detail. ###

---

### First Interactive Map ###
This is a map generated in Python of the University of Virginia in Charlottesville, VA where I completed my undergrad studies.

<embed type="text/html" src="img/uva.html" width="600" height="600">

### OLS Regression on Charlottesville Daily Max Temperature Data ###
<embed type="text/html" src="img/cville_int_plot (3).html" width="600" height="600"> 
![Regression](img/cville_climate_reg_full (2).jpeg)
  
Using daily data pulled from NOA and resampled on an annual basis, I ran an OLS regression on temperature data in Charlottesville dating back to 1893. I found a minor positive correlation showing an increase of 0.00033993 degrees/year. This value lags behind most estimates of average annual temperature increase by multiple orders of magnitude ([Link](https://www.climate.gov/news-features/understanding-climate/climate-change-global-temperature)), but the more surprising result of this exercise was the variability I encountered when implementing different cut-offs for which years to include in the data. Given that some years in the data do not have a complete record for each day in that year, there is some bias in resampling each year by a mean value and considering all years' means equallly, but when I implemented different cutoffs to refine my results, I started seeing negative values contrary to expectations. [Read more about the process here](projects/cville_regression_project.html)

### Plotting Annual Migration for Ring-Necked Ducks

<div style="width: 1200px; height: 400px;">
  <iframe src="img/na_migration.html" style="width: 100%; height: 100%; border: none;"></iframe>
</div>

<div style="width: 1200px; height: 400px;">
  <iframe src="img/global_migration.html" style="width: 100%; height: 100%; border: none;"></iframe>
</div>

<embed type="text/html" src="img/na_migration" width="1200" height="400"> 
<embed type="text/html" src="img/global_migration" width="1200" height="400"> > 

I have always been fascinated by watching ducks fly, and in central Virginia where I grew up, one of the most prevalent species during the winter migration is the ring-necked duck ([Aythya collaris](https://en.wikipedia.org/wiki/Ring-necked_duck)). Using GBIF and ecoregions data, I plotted their migration patterns globally and focused on North America for the 2024 year. They are an often-overlooked species compared to the much more vibrant mallard or wood duck, but we see a lot of them and they have a particularly entertaining flight pattern. Ring-necked ducks should be called ring-billed ducks however. The white bands around their bills are much more pronounced than the barely visible crimson neckband for which they are allegedly named. My grandfather referred to the birds exclusively as ring-bills and it took me years to sort everything out as a child. Regardless of naming convention, I was surprised just how widespread these ducks are. Japan in particular was interesting, and I would assume they spend the warmer spring and summer months in more northern areas without sufficient data collection coverage. I was also not expecting there to be as many ecoregions in the continental US that maintained a population year round and would be interested to run the experiment again on North America with a higher resolution ecoregion map, particularly around the eastern and Mississippi flyways. [Read more about the process here](projects/ringneck_migration_project.html)


<embed type="text/html" src="img/ndvi_diff_plot_new.html width="1200" height="400">
In 2004, the Arizona Water Settlements Act took a major step in compensating for over a century of injustice concerning the water rights of the Gila River Indian Community south of Phoenix. Established in 1859 as the first reservation in Arizona, the GRIC quickly began seeing Gila River flows dimenished due to upstream dams and diversions which put historic agricultural lands and practices at risk. For decades, Tribal leaders engaged federal and state lawmakers in an effort to restore and secure sufficient water access for their people, but progress was slow. The GRIC [website](https://www.gilariver.org/index.php/about/history) and the First Nations Development Institute [case study](https://www.firstnations.org/wp-content/uploads/publication-attachments/2009_NAAW_Rethinking_Asset_Building_Case_1.pdf) on the region provide a much more detailed history. The full 2004 settlement is also available [online](https://www.congress.gov/108/plaws/publ451/PLAW-108publ451.pdf). 

In order to track improvements and changes within the GRIC post settlement, I set up the above plot to compare the Normalized Difference Vegetation Index (NDVI) values of each year after 2004 to average values for the three years prior. The most concentrated change between 2005 and 2022 appears near the middle of the map around coordinates (-111.8, 33.2) which I believe to be aggricultural or reforested land but cannot confirm with current data. Slightly below, there is an area in the lower central area of the GRIC that has gone in the negative direction, but I can tell from the GRIC satefy [website](https://www.gricsafety.org/index.php/fire-department/station-location-and-response-area) that is likely due to the growing downtown area. Overall, there seems to be improvement in NDVI values across the GRIC, but the urban growth of Phoenix and areas surrounding the GRIC make comparing the rates of change inside vs outside of the boundary more difficult. [Read more about the process here](projects/vegetation-project.ipynb)
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
