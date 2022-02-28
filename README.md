# MTN-Cote-d-Ivoire

 MTN Cote d'Ivoire Data Report
 
1.0 Business Understanding 
 
The MTN Cote d'Ivoire would like to upgrade its technology infrastructure for its mobile users in Ivory Coast. 
 
Below are the descriptions of the various columns that we shall be using on the various dataset.

VILLES- These are the Cities. (A French word for the word cities)

STATUS- The state of being in In Network Service or not

LOCALISATION- This is reference to a location in ABIDJAN or not

DECOUPZONE- This implies the Geographical Zone

ZONENAME- The Name of the respective Zone

LONGITUDE- The measurement east or west of the prime meridian

LATITUDE- The measurement north or south of the equator

REGION- The respective Region in Cote d’Ivore

PRODUCT - This is either Voice or SMS services offered by MTN

VALUE -  This is the Billing price of the product resources

DATE_TIME - This is the time in format yyyy-MM-dd hh:mm:ss.0

CELL_ON_SITE- Which cell in the site was used (not needed here)

DW_A_NUMBER_INT- Anonymized phone number of the person for which the CELL_ID and SITE_ID are given.

DW_B_NUMBER_INT- Anonymized phone number of the counterparty

CELL_ID: This is the ID of the network cell 

SITE_ID:  This is  ID of the SITE
 
N/B: There are several cells per site, several sites per City, several Cities per Zone.
 
 
2.0 Data Understanding 
 
We shall use the following datasets for the analysis.

cells_geo_description.xlsx(Links to an external site.)

cells_geo.csv (Links to an external site.)

CDR_description.xlsx [Link]

CDR 20120507 [http://bit.ly/TelecomDataset1]

CDR 20120508 [http://bit.ly/TelecomDataset2]

CDR 20120509 [http://bit.ly/TelecomDataset3]
 
From the dataset above we can check that Cell_geo as the following columns. 

The CDR datasets have similar shapes.

 
3.0 Data Preparation 

We shall select the data into our Python environment i.e Google Colab using the Pandas LIbrary.
We shall be removing NULL from Cells_geo dataset.
Renaming the three CDR datasets i.e CDR 20120507,CDR 20120508 and CDR 20120509 columns to be common to enable easy merging.
Combining the above three CDR datasets respectively. 
Dropping Unnecessary columns from the combined CDR dataset.
Splitting the Date_Time column from the combined CDR dataset to create two columns of DATE and TIME respectively and dropping the redundant DATE_TIME column
Merging the Cell_geo data with the combined CDR dataset
Grouping product by time
 
 
4.0 Analysis 

We used the count function i.e value_count to calculate the number of Villes(City). We found out that Cocody is the most used city. Also the most used during the business and home hours. 
The least used city is Dananon
 

5.0 Recommendation 
 
From the study,  we can recommend improvement of the infrastructure in Dananon to improve the uptake of the products.
