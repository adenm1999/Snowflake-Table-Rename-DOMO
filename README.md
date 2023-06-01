# Snowflake-Table-Rename-DOMO

This Python Script renames table names that is being pushed using the DOMO Multicloud Connection using Snowflake. Please use this link to understand Domo - Snowflake Connection ( https://domo-support.domo.com/s/article/4412849158167?language=en_US )

This Python script automates the renaming of table names in the DOMO Multicloud Connection using Snowflake. To understand the Domo-Snowflake connection, please refer to this link: Domo - Snowflake Connection.

To use this script, you need to follow these steps:

Build a Domo dataset in DOMO using the governance dataset. This will provide you with the dataset ID numbers and DOMO table name lists.

Set up the Snowflake cloud connector in Domo to pull data from Snowflake directly. Key columns in this connector are the Snowflake dataset names and the dataset ID, which we will use for the transformation in Domo.

# Setup

# 1) Build the DOMO ETL 

Important input dataset: are Snowflake datasets and the Governance dataset containing both dataset ID and Dataset Name.

Our recommendation is to create a ETL transformation on top of the 'Domo Governance Datasets Connector' and the Snowflake cloud Connector. Filter your dataset view so that the resulting dataset contains the list of distinct Dataset ID's.

The script expects 2 columns to be present, 'TABLENAME' and 'DATASET_ID'. These are two of the default columns in the Governance Dataset for listing Cards.

Once your dataset view is created, containing the list of DATASET_ID and DATASET_NAMES, take a note of the Dataset ID / Dataset GUI (located in the URL when viewing the dataset view) this is your 'DOMO_DATASET ID' value. (it will be in a similar format to this: d99365a7-864a-435d-92f7-d8b12f2bf47b)

# 2) Clone this repository

Or download it to your local machine.

# 3) Important field inputs that needs to be used in the Script.

1) domain         = "DOMO DOMIN"
2) access_token   = "DOMO Access token"
3) client_id      = 'DOMO Client ID Found in using this url: https://developer.domo.com/ '
4) client_secret  = 'DOMO Client ID Found in using this url: https://developer.domo.com/ '
5) Dataset_url_ID = 'Dataset url ID Dataset GUI (located in the URL when viewing the dataset view)'
6) friendlyName   = 'DOMO Multi-Cloud Connection Name'

# 4) NOTES
Section 3: Using the ETL to get the Domo ID'S ---- Should only be ran if the connection is being set up using the jupyter notebook in DOMO. 
If code is ran outside DOMO using the python SDK use the run: Section 3 - Calling the Domo Dataset Outside of Domo.


