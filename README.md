# Analyzing Iowa Liquor Sales using Online Analytical Processing (OLAP)

## Preface

Analyzing Iowa Liquor Sales using Online Analytical Processing (OLAP) is a project about analyzing and designing a Data Warehouse (DW) for the sales of liquor in Iowa in a team of 2 members. This is the one that I did when studying the subject of **Data Warehouse and OLAP**. I was responsible for **designing the snowflakes schema**, **performing OLAP cubes with SSAS and Power BI**, and finally **building models based on Linear Regression and Random Forest to forecast the daily sales in the next 14 days**. 

## Members

|No.| Full Name | Email |
|--|--------------|-------|
|1| Nguyen Ngoc Hien | 20520496@gm.uit.edu.vn |
|2| Nguyen Thi Kim Lien | 20520909@gm.uit.edu.vn | 

## Dataset

The dataset is provided by Iowa Department of Revenue, Alcoholic Beverages, containing the spirits purchase information of Iowa Class “E” liquor licensees by product and date of purchase from January 1, 2012 to current. The dataset can be used to analyze total spirits sales in Iowa of individual products at the store level.

This one consists of 28.200.000 rows (updated on January 2, 2024) and 24 columns. In this project, the dataset was from 02/01/2022 - 31/01/2022 and kept 23 attributes to design the Data Warehouse.

Source: [Iowa Liquor Sales | data.iowa.gov](https://data.iowa.gov/Sales-Distribution/Iowa-Liquor-Sales/m3tr-qhgy/about_data)

**Note**: Class E liquor license, for grocery stores, liquor stores, convenience stores, etc., allows commercial establishments to sell liquor for off-premises consumption in original unopened containers.

## Snowflakes schema

The snowflakes schema included **1 Fact table** and **7 Dimension tables** (Dim_Time, Dim_Vendor, Dim_Item, Dim_Category, Dim_Store, Dim_City, Dim_County).

![image](https://github.com/ngochien1007/olap-iowa-liquor-sales/assets/154615929/6fe18e1f-4a69-4779-9ec9-f5b983530bda)

## Method

![OLAP](https://github.com/ngochien1007/olap-iowa-liquor-sales/assets/154615929/aa9cba51-fc6b-4977-ba3d-e7085507ee09)

### SSIS

The dataset was imported to SQL Server as an original database. In this process, I accomplished the following tasks: cleaning data, reorganizing data into a multidimensional format, and creating foreign key constraints. After the process of extracting and transforming, data was loaded into the Data Warehouse (SQL Server).

![SSIS](https://github.com/ngochien1007/olap-iowa-liquor-sales/assets/154615929/8b867ce0-001c-4fc7-9b0e-ba7a138140cb)

### SSAS

Then, with the act of dragging and dropping in the SSAS project, I performed the OLAP cube by focusing on showing the daily sales (grouped by Store, City and County), the number of sold products, one of the most popular categories/products etc. bases on basic analytical operations (roll up, drill down, slice and dice, and finally, pivot). 

For example, showing the top 5 products having the highest sales.

* **Name set**
  ![image](https://github.com/ngochien1007/olap-iowa-liquor-sales/assets/154615929/a5029e44-6bb1-444a-a616-2bd24160a996)
  
* **Result**

![image](https://github.com/ngochien1007/olap-iowa-liquor-sales/assets/154615929/0a469754-2099-4d05-841d-3f158bf91397)

Also, I visualize the given issues by using Power BI. For example, I will show some charts that I have done below:

![image](https://github.com/ngochien1007/olap-iowa-liquor-sales/assets/154615929/f4b8118b-5901-4dac-9ff3-4cacd87a64aa)



### Data Mining 

#### Dataset

#### Problem Statement

#### Results

#### Conclusion

## Acknowledgement

