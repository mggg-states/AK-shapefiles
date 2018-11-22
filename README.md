# Alaska Election Shapefile
This shapefile was compiled and processed by members of the Voting Rights Data Institute. The Voting Rights Data Institute (VRDI) was a 2018 summer intensive sponsored by the Metric Geometry and Gerrymandering Group (MGGG) at Tufts and MIT, with major support from a Bose Research Grant at MIT and from the Jonathon M. Tisch College of Civic Life at Tufts.

## Sources
The raw, unprocessed version of this shapefile was retrieved from the Alaska Division of Elections (available for download from http://www.elections.alaska.gov/Core/districtmaps.php). It was joined with a 2013 county shapefile from the US Census Bureau (https://catalog.data.gov/dataset/tiger-line-shapefile-2013-state-alaska-current-county-subdivision-state-based) and the 2013 Alaska statewide house district shapefile (from http://www.elections.alaska.gov/Core/districtmaps.php). Data for 2016 presidential and state house elections was scraped from http://www.elections.alaska.gov/results/16GENR/data/resultsbyprct.txt. Demographic data comes from the US Census Bureau.

## Processing
Demographic data for precincts was created by summing data from each census block with centroids in the precinct. Proration (available from https://github.com/gerrymandr/Preprocessing) was used to build vote totals from voting tabulation districts (VTDs).

## Metadata
- `AREA_x`: Area of precinct
- `DISTRICT`: Precinct code
- `NAME`: Precinct name and code
- `POPULATION`: Total population from 2010 Census
- `IDEAL_VALU`: True population 
- `DEVIATION_`: Deviation from true population
- `F_DEVIATIO`: Deviation from F statistic
- `Name_1`: Precinct name
- `District_1`: Alaska State Assembly district
- `D-Pres Vot`: Prorated vote totals for Democratic Party in 2016 presidential election
- `R-Pres Vot`: Prorated vote totals for Republican Party in 2016 presidential election
- `TP-Pres Vo`: Prorated vote totals for Third Parties in 2016 presidential election
- `D-Dist Vot`: Prorated vote totals for Democratic Party in 2016 assembly district election
- `R-Dist Vot`: Prorated vote totals for Republican Party in 2016 assembly district election
- `Contested`: D if race between 2+ Democrats, R if race between 2+ Republicans, B if two parties in contest
- `sumTOTALPO`: Sum of total number of people in each 2010 census block
- `sumWHITE`: Sum of total number of people in each 2010 census block who are White alone
- `sumBLACK`: Sum of total number of people in each 2010 census block who are Black/African American alone
- `sumNATIVE`: Sum of total number of people in each 2010 census block who are American Indians/Alaska Native alone
- `sumASIAN`: Sum of total number of people in each 2010 census block who are Asian alone
- `sumPACISLA`: Sum of total number of people in each 2010 census block who are Native Hawaiian or Pacific Islander alone
- `sumOTHER`: Sum of total number of people in each 2010 census block who are another race alone
- `sumTWO_PLU`: Sum of total number of people in each 2010 census block who are two or more races
- `sumHISPANI`: Sum of total number of people in each 2010 census block who are of Hispanic origin
- `sumNATALNC`: Sum of total number of people in each 2010 census block who are American Indians/Alaska Native alone or in combination
- `sumMALE`: Sum of total number of people in each 2010 census block who are male
- `sumFEMALE`: Sum of total number of people in each 2010 census block who are female
- `sumGRPQTRS`: Sum of total number of people in each 2010 census block who live in group quarters
- `sumHOUSEUN`: Sum of total number of housing units in each 2010 census block 
- `sumVACANT`: Sum of total number of vacant housing units in each 2010 census block
- `sumOCCUPIE`: Sum of total number of occupied housing units in each 2010 census block
- `sumOWNED`: Sum of total number of occupied housing units that are owned by tenant in each 2010 census block
- `sumRENTED`: Sum of total number of occupied housing units that are rented by tenant in each 2010 census block
- `County`: Name of county that precinct is in
- `Incumbent`: 1 if there was an incumbent Democrat in 2016 AK house race, 0 if not
- `Incumben_1`: 1 if there was an incumbent Republican in 2016 AK house race, 0 if not
- `Winner`: D if winner of 2016 AK house race was Democrat, R if Republican, or I if Independent
- `Reg. Voter`: Total number of voters registered within precinct
- `Reg. D-Vot`: Total number of voters registered with Alaska Democratic Party within precinct
- `Reg. R-Vot`: Total number of voters registered with Alaska Republican Party within precinct
- `Reg. N-Vot`: Total number of voters registered as nonpartisan (no party affiliation) within precinct
- `Reg. U-Vot`: Total number of voters registered as undeclared (no party declared) within precinct
- `pr_D-Pres`: Percent of vote in precinct for 2016 Democratic presidential candidate
- `pr_R-Pres`: Percent of vote in precinct for 2016 Republican presidential candidate
- `pr_TP=Pres`: Percent of vote in precinct for 2016 third party presidential candidates
- `pr_White`: Percent of population in precinct White
- `pr_Native`: Percent of population in precinct American Indian/Alaska Native
- `pop_dens`: Number of people per square mile

## Projection
This shapefile uses a WGS 84 geographic coordinate system.
