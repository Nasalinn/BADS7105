# Customer Segmentation

## 1.) Import Dataset
The given Supermarket dataset contains 956K rows of sales transactions at sales-item level. Imported the file into Google BigQuery.

Note: the dataset received is just a part of Dunhumbly public dataset which is way more bigger. There seems to be historical data from only 2 stores from year 2006 to 2008.

## 2.) Prepare customer single view
### transfrom data
##### CUST_LIFESTAGE 
OA, OF, OT, PE, YA, YF | 1,2,3,4,5,6
----- | -----|
##### Basket_Type
Top Up, Full Shop, Small Shop, XX | 1,2,3,0
----- | -----|
##### BASKET_DOMINANT_MISSION
Grocery, Fresh, Mixed, Nonfood, XX | 1,2,3,4,0
----- | -----|

### Define features
* Total visits = COUNT(DISTINCT BASKET ID)
* Ticket size = SUM(SPEND)/COUNT(DISTINCT BASKET ID)
* Total no. of SKUs 
* TotalSpend = SUM(SPEND)
* FirstDate = MIN(SHOP_DATE)
* LastDate = MAX(SHOP_DATE)
* SHOP_HOUR = MEAN(SHOP_HOUR)
* LifeStage = MIN(CUST_LIFESTAGE)
* BasketType = MAX(BASKET_TYPE)                                                                               BasketMission = MAX(BASKET_DOMINANT_MISSION)
* Total_days = LastDate - FirstDate +1
* recency = max(date) - (LastDate)

## 3.) Cluster customers
A Comparative Efficiency of Clustering using Silhouette, Calinski-Harabasz, Davies-Bouldin 

![image](https://user-images.githubusercontent.com/95351692/147571211-b1bd837d-83e6-4dae-ad50-9e28754948a3.png)

The results of the run concluded that Spectral Clustering and KMeans Clustering were the most efficient in classification.

### KMeans Clustering
Create KMean model 
#### Choosing K number of clusters
Choose K = 5

![image](https://user-images.githubusercontent.com/95351692/147571375-9ba77060-7f04-45f5-a5fe-af8ecb653161.png)

## 4.) Clustering Result Analysis

### Spectral Clustering
![image](https://user-images.githubusercontent.com/95351692/147571501-c6751abd-ef72-4bf6-86a3-6e0b7a1213b9.png)

As a result of using Spectral Clustering in segmentation, it is evident that the classification is poor.
### KMeans Clustering
![image](https://user-images.githubusercontent.com/95351692/147571608-65b44d6e-694c-4cc7-b2fb-99b772a8e054.png)
![image](https://user-images.githubusercontent.com/95351692/147571659-40410a80-ee36-44d3-8f74-899414170ac8.png)

## 5.) Interpretation
![image](https://user-images.githubusercontent.com/95351692/147572167-683cdac8-9d7f-45f2-ae8f-64e38609d2db.png)







