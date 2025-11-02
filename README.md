This readme file was generated on [2025-10-30] by [Carlos Zetina]

# GENERAL INFORMATION

* Calgary Communities, Economic Sustainability: 
Name: Carlos Francisco Zetina
Student ID: 30066882
Institution: University of Calgary
Address: Calgary, Alberta
Email: c.zetina9@gmail.com


* Date of data creation: *(2025-10-07)- (2025-10-25)*
* Study Area: *Calgary, Alberta, Canada*

# PURPOSE

* To access the economical sustainability of Calgary using tax revenue information on a community basis. 

# SHARING/ACCESS INFORMATION

* Licenses/restrictions placed on the data: <a href="https://example.com">Calgary Economic Sustainability Repository</a> © 20025 by <a href="https://example.com">Carlos Zetina</a> is licensed under <a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a><img src="https://mirrors.creativecommons.org/presskit/icons/cc.svg" alt="" style="max-width: 1em;max-height:1em;margin-left: .2em;"><img src="https://mirrors.creativecommons.org/presskit/icons/by.svg" alt="" style="max-width: 1em;max-height:1em;margin-left: .2em;">
*  Data derived from:
	* Current Year Property Assessments (Parcel) [csv] - Open Calgary - https://data.calgary.ca/Government/Current-Year-Property-Assessments-Parcel-/4bsw-nn7w/about_data
	* Community Boundaries - Open Calgary [shapefile] - https://data.calgary.ca/Base-Maps/Community-Boundaries/ab7m-fwn6
	* Calgary Community Census 2021 [csv] - Spatial & Numeric Data Services - https://sands.ucalgary.ca/datacatalogue.php 


# DATA & FILE OVERVIEW

## File List: *list all files (or folders, as appropriate for dataset organization) contained in the dataset, with a brief description*

* comm_pop_list.csv: Population counts for 207 Calgary communities as per the 2021 federal census. Communities labled using community code only. 
* prop_assess_clean.csv: Total assessed value of residential properties & total residential property tax for 274 communities in Calgary as of October 2025. Communities labled using community code only. 
* final_commun_table.csv: Clean derived data set including the total residential property value, total property tax, total population count, total area (m^2) and population density for 207 communities in Calgary. 
* csv_processing.ipynb: Jupyter notebook that outlines how the csv files were derived from the raw data. 
* correlation_plots.ipynb: Jupyter notebook that outlines how the final clean tables (commun_table.csv) was used in a correlation analysis and to generate scatter plots. 
* plots.png: Image that shows the scatter plots created using commun_table.csv


* Relationship between files: comm_pop and prop_assess_clean were derived from Calgary Community Census 2021 and Current Year Property Assessments (Parcel), respectiveley, using the csv_processing jupyter notebook. 
* Additional related data collected that was not included in the current data package: The Area and Population Density were calculated in ArcGIS Pro using calculate geometry and calculate field. 
* CRS: NAD83 / Alberta 3TM ref meridian 114 W [EPSG:3776]


# METHODOLOGICAL INFORMATION

## Description of methods used for collection/generation of data: 
In order to create the csv files in this repository pandas was used. The plots were created using matplotlib. Python was used using jupyter notebooks. Two data sets were downloaded from Open Calgary, Current Year Property Assessments & Community Boundaries. Calgary Community Census 2021 was obtained through the Spatial & Numeric Data Services of the University of Calgary. 

## Methods for processing the data: 

The Current Year Property Assessments data sets was cleaned by eliminating all undesired columns. Then, using the Property Assessments column Property Tax was calculated for each row. Following this step all rows were joined by community code to have a representation of total property tax for each community in Calgary. The Community Census 2021 data set was cleaned by eliminating all undesired columns and then modifying the naming convention of communities to match that of the Current Year Property Assessments data set. Using the Calgary Community Boundaries dataset the area of each community was calculated in m^2 on ArcGIS Pro and the two cleaned datasets were combined to this one. Finally a correlation analysis was preformed using this final combined dataset.  


## Instrument- or software-specific information needed to interpret the data: 
Visual Studio Code 1.96.4 (Universal)
Python 3.12.2
Pandas Library for Python
MatPlot Library for Python
ArcGIS Pro 3.5


# DATA-SPECIFIC INFORMATION FOR: [Calgary Community Census 2021 CPD]

* Format: csv
* Number of columns: 2602
* Number of cases/rows: 311
* Variable List: The 311 rows are 311 Calgary Communities. The columns are detailed population counts for 2601 different de demographic variables. Columns tht begin with 'Total-' are the actual total population counts for each community. 
* Missing data codes: 'x'
* Encoding: 'latin1' 

# DATA-SPECIFIC INFORMATION FOR: [Current Year Property Assessments (Parcel) ]
*repeat this section for each dataset, folder or file, as appropriate*

*Format: csv
* Number of columns:  21
* Number of cases/rows: 588825
* Variable List:  Rows are registered parcels in the city of Calgary. Columns are infromation about them [Address, Number, Assessed Value, Class etc. ]
* Missing data codes: 'NaN'

# DATA-SPECIFIC INFORMATION FOR: [prop_assess_clean]

* Format: csv
* Number of columns: 3 
* Number of cases/rows: 273
* Variable List: 273 communities. First column is community code of a community, second is the total residential property assessed value and third is the total property tax on a community scale.


# DATA-SPECIFIC INFORMATION FOR: [comm_pop_clean]

* Format: csv
* Number of columns: 2 
* Number of cases/rows:  208
* Variable List: 208 Calgary Communities. First row is community code, second is total population. 

# DATA-SPECIFIC INFORMATION FOR: [final_comm_table]

* Number of columns: 207  
* Number of cases/rows: 7
* Variable List: 207 Calgary Communities. Columns: Community Code, Community name, total residential property value, total property tax, population, area (m^2) and population density (per m^2)

# DATA-SPECIFIC INFORMATION FOR: [Community Boundaries]

*Format: Shapefile
* Number of columns: 10
* Number of cases/rows: 313
* Variable List: 313 Calgary Communities, 10 variables relating to community: type, built status, creation date etc. 
