# BellaBeat Case Study
## Dataset from Kaggle - Origin and Context:
The data being analyzed is public data that explores smart device users’ daily habits. 
Sršen proposes this specific dataset for analysis: 
Fitbit Fitness Tracker Data (CC0: Public Domain, dataset made available through Mobius
Bellabeat is  a high-tech company that manufactures health-focused smart products for women. 
The company has been successful and seeks to become a major player in the smart device global market.
## Business Task 
Urška Sršen cofounder, of Bellabeat is requesting an analysis of smart device usage data, to gain insights into how consumers use non-Bellabeat smart devices. 
She then wants these insights to be applied to one of Bellabeat’s products. 
## Project Goals
- Identify trends in smart device usage.
- Apply insights to one of Bellabeat’s products
- Make recommendations based on insights from the analysis.
## Limitations of Data
- Reliability: The data is not reliable. It has a sample size of 30 persons which is quite a small sample size to inform actionable decisions.   
- Originality: The data is not original. It was generated using Amazon mechanical Turk. 
- Comprehensive: The data makes no mention of demographics. This study is focused on products for women, and it would have been good to have a representation of that demographic in the data. 
- Current: The data is not current. It is from 2016 
- Cited: The data has not been cited.

It is worth mentioning that the dataset is "CCO: Public domain".
This means that the person who associated a work with this deed has dedicated the work to the public domain by waiving all his or her rights to the work worldwide under copyright law, including all related and neighboring rights, to the extent allowed by law. You can copy, modify, distribute, and perform the work, even for commercial purposes, all without asking for permission.

## Data Sources Used:  
The following CSV files from the dataset are being analyzed for this case study.
- dailyActivity_merged
- dailyCalories_merged
- dailyIntensities_merged
- dailySteps_merged
- sleepDay_merged.
- weightLogInfo_merged
- HourlyCalories_merged
- HourlyIntensities_merged
  
These subsets of data will help me identify trends in smart device usage using averages. The minutes and seconds info are too granular to paint the big picture I want to portray.

# Data Analysis
## Data Cleaning
- Use of Count Function to validate Daily Activity data
  
DailyActivity Data was loaded successfully into MS Excel, Big Query and SQL Server Management Studio and data loaded successfully in all 3 platforms. This helped me test for integrity.  I counted 940 rows across all 3 platforms for “dailyActivity_merged” table. There were no inconsistencies. 

<img width="1291" height="623" alt="BIG QUERY - dailyActivity_merged rows loaded " src="https://github.com/user-attachments/assets/36be3c8d-1c81-4c8b-82c9-6b5bd30c2b7b" />
<img width="1253" height="745" alt="SSMS - 'dailyActivity_merged'  rows loaded " src="https://github.com/user-attachments/assets/3e4e12b0-b35c-4139-bf59-bbe151933f1f" />
<img width="1377" height="689" alt="Ms Excel - 'dailyActivity_merged' rows loaded " src="https://github.com/user-attachments/assets/cdda31cf-e715-4de6-8166-ff1fdeb1bbf1" />

However, other data sources like ‘Heartrate in seconds’ had a voluminous set of data over a million rows which got loaded into SSMS. Excel can’t load those many rows. 
I chose SSMS (SQL Server Management Studio) for analysis. I find the interface quite simple and intuitive.

- Checking for NULLs: Using the ‘is NULL’ function for each column.
- Checking for duplicates: Usinf DISTINCT - No duplicates found.

The data also shows that not just 30 people (sample size) provided data.  33 unique Ids were found using the below query. 

<img width="1912" height="1006" alt="Unique Ids -SSMS" src="https://github.com/user-attachments/assets/be1d3f2f-3ed2-45a2-9745-45358142dd8c" />

Using the below query, it was also possible to infer the amount of data supplied by each unique Id. Most of the participants provided data for a month (31 days), others for a little less than 31 days, but 1 person provided data for just 4 days. 

<img width="1085" height="1003" alt="Records per Id - SSMS " src="https://github.com/user-attachments/assets/d30de972-bd01-4fdc-abb7-6835630218c3" />


A series of queries were run to identify trends. ( See 'SQL Queries - Bellabeat Project' Word document file attached to this project) 
- Data was organized in tables in SSMS
- Several queries were run on the data to aggregate for better analysis.
- Aggregated data was imported into Tableau as extracts and visualizations created to show the trends discovered.

# Findings

Figure 1

- A total of 33 unique participant IDs were found from the dataset.
- On average, just 21.21% of participants complete 10,000steps a day which is the CDC benchmark.
- 78.79% fall short.
<img width="1053" height="886" alt="image" src="https://github.com/user-attachments/assets/61a9b8e2-19cc-4ac3-ac50-ed7c894b20da" />

Figure 2

- There is no direct correlation between level of activity and quality of sleep. 
- As a matter of fact, in the case of ID # 8053475328, there is an inverse relationship. The more active, the less sleep and the less active, the more sleep. 
- There must be other factors than level of activity impacting the quality of sleep.
- The number of participants who reported numbers for sleep is 24. Not all participants wear their trackers in bed.
<img width="857" height="942" alt="image" src="https://github.com/user-attachments/assets/107c6455-4c2a-44cc-9ef6-bcb484dd86c7" />

Figure 3 

- There is a somewhat direct correlation between the intensity of activity and the calories burned.
- For most participants, both graphs peaked at the same points. Meaning as average intensity goes up, average calories burned also go up.
- However, for ID # 4057192912, there is an indication of high calorie burn with minimal intensity. Therefore, there are other factors contributing to calorie burn which the data does not necessarily portray
<img width="1023" height="861" alt="image" src="https://github.com/user-attachments/assets/b8193c9a-e424-4d2f-a399-1cbc05cd1152" />

Figure 4 
- Just 8 participants logged in Weight Info. This is an indication of probably a lack in smart device technologies to conveniently record weight info.
- Of the 8 records, 5 are overweight, (more than 50%) going by the below interpretation of BMI results.
<img width="2687" height="147" alt="image" src="https://github.com/user-attachments/assets/ca1aee63-2462-4cdc-b330-bc48e4c9186a" />







  



























