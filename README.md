# House-Price-Prediction
I did data exploration and feature engineering before training Linear Regression and Decision Tree.

Data Exploration:
1. Aggregated mean and std of the features: "housing_median_age", "total_rooms", "total_bedrooms", "population", "households", "median_income", "median_house_value" grouped by Ocean Proximity
2. Aggregated statistical properties (mean,std,min,max) of the above numerical features on the basis of Geagraphic Clusters created using these methods:
   2a. Geohash codes derived from Latitude, Longitude
   2b. Applied hierarchical clustering based on Latitude, Longitude
Ultimately, derived another feature called Geographic Clusters based on hierarchical_cluster

Derived Following Insights:
1. Coastal areas (NEAR OCEAN, <1H OCEAN, NEAR BAY) have higher house values, have old houses and high median incomes.<br>
2. Inland areas have newer housing, lower house values, and more variability in total rooms/population.<br>
3. ISLAND is a unique case: low population and low median income but extremely high home values (suggesting luxury homes or vacation properties) & oldest housing.<br>
4. Clusters 4, 5, 6, and 10 appear to be wealthier, denser urban areas with high home values and incomes.
5. Clusters 2 and 7 seem to be lower-income, lower house value areas.
6. Cluster 10 has a high density and newer housing stock, possibly a developing area.

Achieved RMSE of 66413.5742, R²: 0.6775 on Test dataset using Decision Tree Regressor
