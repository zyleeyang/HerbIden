# IdenHerb
## Description
`IdenHerb` is an open-source, cross-platform R script to identify herbs contained in Chinese patent medicines or other complex systems.
## Installation instructions
To install via Github, run the following code in R console:
```R
devtools::install_github('zyleeyang/IdenHerb')
library(IdenHerb)
```
## Construction of characteristic ion groups of each herbs
```R
setwd("data") #data represents the path where the data is stored.
#Step 1
internal_standard(data_file) #data_file represents the file that the data is stored.
#Output the retention time and m/z of all samples, for ensuring reliable data
#Step 2
Pre_processdata("example_data/") #example_data is a file containing herbs' data for constructing of characteristic ion groups
#Convert data format for subsequent analysis. Result 1 : processed_rawdata.csv
#Step 3
filter_data(unfilter_data = "processed_rawdata.csv")
#filter the data that peak area > 10000 (AB Sciex). Result 2 : processed_rawdata (This is a file)
#Step 4
character_ion(proceseed_rawdata = "processed_rawdata") #Constrction of characteristic ion groups of each herbs
#Result 3 : herb_charcter_ion.csv
```



