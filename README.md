# Valley Fever Prevalence (VYF) and Climate 

## Summary  
This project is an exploration of valley fever prevalence and temperature and precipitation controls.
Valley Fever is a soil based pathogen that has been growing in prevalence year by year. It is endemic to the southwest and the majority of cases are seen in California and Arizona. 
While this project explores the entire southwest, California and Arizona VYF prevalence are the primary focus. 
I aggregated Census, Temperature, Precipitation, and Valley Fever Prevalence data to use in this project. State level analysis shows data from 1998 to 2022. County level analysis shows data from 2001 - 2021 for California and 2006 to 2021 for Arizona.

The statistical heart of this analysis is an OLS linear model applied to a long spanning county level 1895 - 2022 Temperature and Precipitation data set, to quantify climate change at a county level to use for analysis and visualization. This output of this model is then used in tandem with Valley Fever Prevalence data to allow us a little leverage to explore prevalence in light of climate change. 

## Project Walkthrough

### Tableau Visualization

A full version of the tableau visualization is included in the repo. Here is a sample: 

![Dashboard 1 (1)](https://github.com/maxinavarrette/valleyfeverclimate-/assets/79235014/ab86c5ff-036c-4153-8a34-8c382b8807f9)

Here is a link to the online location of the Tableau Visualization Dashboard: https://public.tableau.com/app/profile/maxi.navarrette/viz/ValleyFeverVYFPrevalenceandClimateChange/Dashboard1

### Python, SQL 

Data pre-processing was split between SQL and Python. 
The outputs of the  Jupyter notebook where pre-processing, eda, and quantitative analysis was performed is included in the repository. 
The SQL script that was used to pre-process Valley Fever Prevalence data from the CDC is included in the repo. 
Eda in python informed focus of visualization in tableau. Temperature had higher correlation than precipitation with VYF prevalence. 


# Data Sources and References

## Valley Fever: 

### State Level

VYF data 1998 - 2017 for Arizona, California, Nevada, New Mexico, Utah, and 'Other States' 
was acquired through the CDC. 
https://www.cdc.gov/fungal/diseases/coccidioidomycosis/statistics.html


2018 - 2022 acquired through CDC NNDSS weekly tables, and California and Arizona state county health deperatments. CDC data seems to be underreported or just misaligned with state data often, so in the case of discrepancies we went with state agency reports. Processed in SQL. 

### County Level

California:
2001 - 2021
https://www.cdph.ca.gov/Programs/CID/DCDC/Pages/ValleyFeverDataPublications.aspx

Arizona: 
2006 - 2021 
https://directorsblog.health.azdhs.gov/
*very difficult site to work with. you can use their in house search to find executive reports for the years listed. 


## Climate:

Acquired county level climate and precipitation data from [NOAA's National Climatic Data Center FTP](ftp.ncdc.noaa.gov). 


## References 
Packages Used: Pandas, Numpy, Seaborn, Matplotlib, Sklearn  

[Economic Valuation of Coccidioidomycosis (Valley Fever) Projections in the United States in Response to Climate Change](https://pubmed.ncbi.nlm.nih.gov/34316325/)  

[Washington Post 2C provides inspiration for analysis](https://github.com/washingtonpost/data-2C-beyond-the-limit-usa)







