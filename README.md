# Snowflake-Table-Rename-DOMO

This Python Script renames table names that is being pushed using the DOMO Multicloud Connection using Snowflake. Please use this link to understand Domo - Snowflake Connection ( https://domo-support.domo.com/s/article/4412849158167?language=en_US )

The script requires the indvidual to build a Domo dataset in DOMO using the governance dataset to get the dataset ID numbers and DOMO table name lists. Furthermore, to set up using teh snowflake cloud connector to pull data from snowflake to DOMO Directly - Key columun are Snowflake dataset Names and the Dataset ID which we will using to the transformation in Domo.

# Setup

# 1) Build the DOMO ETL 

Use example JSON ETL Example - Important input dataset are Snowflake datasets and the Governance dataset containing both dataset ID and Dataset Name.

Our recommendation is to create a ETL transformation on top of the 'Domo Governance Datasets Connector' and the Snowflake cloud Connector. Filter your dataset view so that the resulting dataset contains the list of distinct Dataset ID's.

The script expects 2 columns to be present, 'TABLENAME' and 'DATASET_ID'. These are two of the default columns in the Governance Dataset for listing Cards.

Once your dataset view is created, containing the list of DATASET_ID and DATASET_NAMES, take a note of the Dataset ID / Dataset GUI (located in the URL when viewing the dataset view) this is your 'DOMO_DATASET ID' value. (it will be in a similar format to this: d99365a7-864a-435d-92f7-d8b12f2bf47b)

# 2) Clone this repository

Or download it to your local machine.

# 3) Important field inputs that needs to be used in the Script.

domain         = "DOMO DOMIN"
access_token   = "DOMO Access token"
client_id      = 'DOMO Client ID Found in using this url: https://developer.domo.com/ '
client_secret  = 'DOMO Client ID Found in using this url: https://developer.domo.com/ '
Dataset_url_ID = 'Dataset url ID ataset GUI (located in the URL when viewing the dataset view)'




