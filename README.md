# Capstone_CDF_April21

Group project work for collaboration

Our observation excel link:
https://docs.google.com/spreadsheets/d/18yDcIQdF4LxTW9CgJncvkv7RYptsECOj/edit#gid=632981895


Our Report Doc link:
https://docs.google.com/document/d/1-F9eYHbAQkO81y3Cm84ahFjoTObW5lWEg7vIaVJRtK0/edit#heading=h.z6ne0og04bp5

==================================================================================================================================

### Capstone Group Project (CDF) - **Consulting Assignments**

Telecom operators are waging a war for connectivity and customer intimacy. Being a consultanting group, we have analyzed the user data of **InsaidTelecom** and helping them to better understand their customers, build superior networks, find a sustainable path to growth and achieve cost leadership while maintaining a high-performance organization.

<img src="https://github.com/pathakchiranjit/Capstone_CDF_April21/blob/main/Picture/it-consulting-min.gif?raw=true" align='left'><br/>




### Behavioural analysis of **InsaidTelecom** users

**InsaidTelecom**, one of the leading telecom players, understands that customizing offering is very important for its business to stay competitive.
Currently, InsaidTelecom is seeking to leverage behavioral data from more than 60% of the 50 million mobile devices active daily in India to help its clients better understand and interact with their audiences.

<img src="https://github.com/pathakchiranjit/Capstone_CDF_April21/blob/main/Picture/Telecom-Industry.jpg?raw=true" align='left'><br/>




### **Data Sources I**:

The Data is collected from mobile apps that use **InsaidTelecom** services. Full recognition and consent from individual user of those apps have been obtained and appropriate anonymization have been performed to protect privacy. Due to confidentiality, **InsaidTelecom** won't provide details on how the gender and age data was obtained.

The data schema can be represented in the following Table:
1.gender_age_train - Devices and their respective user gender, age and age_group.
2.phone_brand_device_model - device ids, brand, and models phone_brand.

These datasets are being downloaded from MySQL instance.          
host	'cpanel.insaid.co'
user	'student'
passwd	'student'
database	'Capstone1'

<img src="https://github.com/pathakchiranjit/Capstone_CDF_April21/blob/main/Picture/device_id_6.jpg?raw=true" align='left'><br/>




### **Data Source II**:

"events_data" - when a user uses mobile on **InsaidTelecom** network, the event gets logged in this data.
Each event has an event id, device id, location (lat/long), and the event corresponds to frequency of mobile usage.
timestamp: when the user is using the mobile.

This dataSet for events_data downloaded from:
https://drive.google.com/file/d/1Ir3rW0YTKmk7MSjVjCU_UGMQevhe1v9W/view

<img src="https://github.com/pathakchiranjit/Capstone_CDF_April21/blob/main/Picture/device_id_2.jpg?raw=true" align='left'><br/>

### **What is a Device Id**:
Device Ids are basically mobile device identifiers. They are unique strings of letters or/and numbers. These identifiers connect apps with specific servers and they are obtained after the app was installed on customers’ gadgets. Using them we can track users based on the data sent by their smartphone or tablet. Obviously, due to customers’ privacy regulations we can do that if and only if they allow us to access that data. When users opt in for being followed by marketers, great things can happen for both parties implied in the process. The device IDs send the information from users towards apps.

<img src="https://github.com/pathakchiranjit/Capstone_CDF_April21/blob/main/Picture/device_id_1.jpg?raw=true" align='left'><br/>

### **How To Use Device IDs for efficient marketing strategy?**:
One of the major disadvantages of these identifiers is that they require users’ approval for gathering data. But for those who offer their consent, mobile IDs represent a very efficient way for customizing ads/services based on customers’ interests. Because device IDs can be tracked inside apps, they allow app owners to learn more about their users’ preferences when it comes to analyze their creation. This information is also very important whenever they want to update the app. It gives a considerable advantage over other competitors who don’t pay attention to this technique. For maintaining the highest standards and to impress customers while they complete the activities inside the app service providers can benefit of this real time opportunity.

<img src="https://github.com/pathakchiranjit/Capstone_CDF_April21/blob/main/Picture/device_id_3.png?raw=true" align='left'><br/>

### **Weekly Goals for the team?**:
The DS consultant team will follow the below week-wise goals,

<img src="https://github.com/pathakchiranjit/Capstone_CDF_April21/blob/main/Picture/image1.png?raw=true" align='left'><br/>

## Table of Contents

1. [Objective: Problem Statement](#section1)<br>
2. [2. Tools : Importing Packages, Libraries & Defining Functions:](#section2)<br>
  - 2.1 [Import Packages and Libraries:](#section201)<br>
  - 2.2 [Defining Functions :](#section202)<br>
    - 2.2.1 [plot_on_map : To plot points on map using folium package](#section2021)<br>
    - 2.2.2 [missing_data : To find all the missing data in the data set](#section2022)<br>
3. [Collecting & Loading Data](#section3)<br>
  - 3.1 [Collect data from Google drive:](#section301)<br>
  - 3.2 [Collect data from MySQL Instances:](#section302)<br>
    - 3.2.1 [Import User details from gender_age_train dataset](#section3021)<br>
    - 3.2.2 [Import Device details from brand_model dataset](#section3022)<br>
4. [Data Preprocessing](#section4)<br>
  - 4.1 [Translation of Model names from Chienese to English:](#section401)<br>
  - 4.2 [Translation of Brand names from Chienese to English:](#section402)<br>
  - 4.3 [Checking the occurance of the missig data:](#section403)<br>
5. [Data processing and Imputing methodologies:](#section5)<br>
  - 5.1 [Imputing missing latitude and longitudes:](#section501)<br>
  - 5.2 [Imputing missing States:](#section502)<br>
  - 5.3 [Imputing missing Device Ids:](#section503)<br>
  - 5.4 [Imputing missing latitude and longitudes:](#section504)<br>
  - 5.5 [Data Selection : Based on defined six (6) States:](#section505)<br>
  - 5.6 [Data preparation/extraction for Dashboarding using Web UI Tools:](#section506)<br>
  - 5.7 [Datetime conversion to Weekday and Time:](#section507)<br>
  - 5.8 [Outlier selection for Age of user and age segment creation:](#section508)<br>
6. [Exploratory Data Analysis](#section6)<br>
  - 6.1 [Duplicate detection and removal:](#section601)<br>
  - 6.2 [Total Event Analysis:](#section602)<br>
  - 6.3 [Unique Event Analysis:](#section603)<br>
      - 6.3.1 [Statewise Distribution Analysis:](#section60301)<br>
      - 6.3.2 [Day, Time wise Distribution Analysis:](#section60302)<br>
      - 6.3.3 [City wise Distribution Analysis:](#section60303)<br>
      - 6.3.4 [Gender wise Distribution Analysis:](#section60304)<br>
      - 6.3.5 [Age segment wise Distribution Analysis:](#section60305)<br>
      - 6.3.6 [Phone brand wise Distribution Analysis:](#section60306)<br>
      - 6.3.7 [Summary: Correlation among all the columns:](#section60307)<br>
7. [Conclusions](#section7)
  - 7.1 [Actionable Insights](#section701)
  - 7.2 [Limitation of this study](#section702)


