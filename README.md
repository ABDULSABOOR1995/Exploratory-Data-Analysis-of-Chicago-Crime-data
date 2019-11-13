# EDA of Chicago Crime Data

## Context
This dataset reflects reported incidents of crime (with the exception of murders where data exists for each victim) that occurred in the City of Chicago from 2001 to present, minus the most recent seven days. Data is extracted from the Chicago Police Department's CLEAR (Citizen Law Enforcement Analysis and Reporting) system. In order to protect the privacy of crime victims, addresses are shown at the block level only and specific locations are not identified. Should you have questions about this dataset, you may contact the Research & Development Division of the Chicago Police Department at 312.745.6071 or RDAnalysis@chicagopolice.org. Disclaimer: These crimes may be based upon preliminary information supplied to the Police Department by the reporting parties that have not been verified. The preliminary crime classifications may be changed at a later date based upon additional investigation and there is always the possibility of mechanical or human error. Therefore, the Chicago Police Department does not guarantee (either expressed or implied) the accuracy, completeness, timeliness, or correct sequencing of the information and the information should not be used for comparison purposes over time. The Chicago Police Department will not be responsible for any error or omission, or for the use of, or the results obtained from the use of this information. All data visualizations on maps should be considered approximate and attempts to derive specific addresses are strictly prohibited. The Chicago Police Department is not responsible for the content of any off-site pages that are referenced by or that reference this web page other than an official City of Chicago or Chicago Police Department web page. The user specifically acknowledges that the Chicago Police Department is not responsible for any defamatory, offensive, misleading, or illegal conduct of other users, links, or third parties and that the risk of injury from the foregoing rests entirely with the user. The unauthorized use of the words "Chicago Police Department," "Chicago Police," or any colorable imitation of these words or the unauthorized use of the Chicago Police Department logo is unlawful. This web page does not, in any way, authorize such use. Data are updated daily. The dataset contains more than 6,000,000 records/rows of data and cannot be viewed in full in Microsoft Excel. To access a list of Chicago Police Department - Illinois Uniform Crime Reporting (IUCR) codes, go to http://data.cityofchicago.org/Public-Safety/Chicago-Police-Department-Illinois-Uniform-Crime-R/c7ck-438e

## Content
<b>ID -</b> Unique identifier for the record.

<b>Case Number -</b> The Chicago Police Department RD Number (Records Division Number), which is unique to the incident.

<b>Date -</b> Date when the incident occurred. this is sometimes a best estimate.

<b>Block -</b> The partially redacted address where the incident occurred, placing it on the same block as the actual address.

<b>IUCR -</b> The Illinois Unifrom Crime Reporting code. This is directly linked to the Primary Type and Description. See the list of IUCR codes at https://data.cityofchicago.org/d/c7ck-438e.

<b>Primary Type -</b> The primary description of the IUCR code.

<b>Description -</b> The secondary description of the IUCR code, a subcategory of the primary description.

<b>Location Description -</b> Description of the location where the incident occurred.

<b>Arrest -</b> Indicates whether an arrest was made.

<b>Domestic -</b> Indicates whether the incident was domestic-related as defined by the Illinois Domestic Violence Act.

<b>Beat -</b> Indicates the beat where the incident occurred. A beat is the smallest police geographic area – each beat has a dedicated police beat car. Three to five beats make up a police sector, and three sectors make up a police district. The Chicago Police Department has 22 police districts. See the beats at https://data.cityofchicago.org/d/aerh-rz74.

<b>District -</b> Indicates the police district where the incident occurred. See the districts at https://data.cityofchicago.org/d/fthy-xz3r.

<b>Ward -</b> The ward (City Council district) where the incident occurred. See the wards at https://data.cityofchicago.org/d/sp34-6z76.

<b>Community Area -</b> Indicates the community area where the incident occurred. Chicago has 77 community areas. See the community areas at https://data.cityofchicago.org/d/cauq-8yn6.

<b>FBI Code -</b> Indicates the crime classification as outlined in the FBI's National Incident-Based Reporting System (NIBRS). See the Chicago Police Department listing of these classifications at http://gis.chicagopolice.org/clearmap_crime_sums/crime_types.html.

<b>X Coordinate -</b> The x coordinate of the location where the incident occurred in State Plane Illinois East NAD 1983 projection. This location is shifted from the actual location for partial redaction but falls on the same block.

<b>Y Coordinate -</b> The y coordinate of the location where the incident occurred in State Plane Illinois East NAD 1983 projection. This location is shifted from the actual location for partial redaction but falls on the same block.

<b>Year -</b> Year the incident occurred.

<b>Updated On -</b> Date and time the record was last updated.

<b>Latitude -</b> The latitude of the location where the incident occurred. This location is shifted from the actual location for partial redaction but falls on the same block.

<b>Longitude -</b> The longitude of the location where the incident occurred. This location is shifted from the actual location for partial redaction but falls on the same block.

<b>Location -</b> The location where the incident occurred in a format that allows for creation of maps and other geographic operations on this data portal. This location is shifted from the actual location for partial redaction but falls on the same block.

## Inspiration
How has crime changed over the years? Perform exploratory data analysis on Chicago Crime Data.

## Data Source
https://www.kaggle.com/currie32/crimes-in-chicago<br><br>
I've performed analysis on all 4 data files.

<a id='goback'></a>
## Table of Content:
[1. Data Reading](#hh1)<br>
[2. Data Understanding](#hh2)<br>
[3. Data Cleaning](#hh3)<br>

### EDA

[1. Create a data frame that shows the total number of crimes reported in each year. ](#h1)<br>
[2. Make a line and bar charts that show the total number of crimes reported in each year.](#h2)<br>
[3. Find the year in which the maximum number of crimes are reported.](#h3)<br>
[4. Find the year in which the minimum number of crimes are reported.](#h4)<br>
[5. Find how many unique crimes recorded from 2001 to 2017 and what they are.](#h5)<br>
[6. How many Thefts (crime) and what are their different types of recorded with their count?](#h6)<br>
[7. Find for one primary type how many descriptions are there in the table.](#h7)<br>
[8. Find the total number of arrest are done.](#h8)<br>
[9. Create a data frame that shows the number of arrests each year.](#h9)<br>
[10. Find how much unique crime location is recorded from 2001 to 2017 and what they are. Show them with their count.](#h10)<br>
[11. Find the number of districts in which crime recorded and also show them with their count.](#h11)<br>
[12. Make a summary of everything related to crime like total crimes, total arrests, total unique crime types, etc. Also, make a data frame to show that summary.](#h12)<br>
[13. Create a data frame that shows the summary of unique crimes committed with their count.](#h13)<br>
[14. Make a data frame that shows the complete summary of each crime type.](#h14)<br>
[15. Make a pie chart to show the proportion of each unique crime reported in all crimes.](#h15)<br>
[16. Make a bar chart to show the proportion of each unique crime reported in all crimes.](#h16)<br>
[17. Make a donut chart to show the proportion of each unique crime reported in all crimes.](#h17)<br>
[18. Make a data frame and show all types of crime in that data frame according to their percentages then make its pie and bar charts.](#h18)<br>
[19. It is commonly said that crime rate is inversely proportional to arrest means if arrest goes up crime rate goes down and if arrest goes down then crime goes up, so now with the help of line and bar chart you have to prove that crime rate is inversely proportional to arrest.](#h19)<br>
[20. Create a data frame that shows the summary of total crimes each year and total arrest each year.](#h20)<br>
[21. What is the relation between crime and arrest? (Find correlation b/w crime and arrest)](#h21)<br>
[22. Which 3 crimes committed most of the time in 2008?](#h22)<br>
[23. List top 5 blocks where most of the crimes committed with their districts, community area name & count of a crime.](#h23)<br>
[24. Make a data frame that shows the top 5 districts where most of a crime committed.](#h24)<br>
[25. Make a data frame that shows the top 5 community areas where most of a crime committed.](#h25)<br>
[26. How many unique types of crime committed on the gas station and what they are? Show them with their count.](#h26)<br>
 
