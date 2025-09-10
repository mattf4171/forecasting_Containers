## Forecasting Analysis for Containers

ML based Approach to provide service technicians with confidence of which containers and their associated locations to service with the utmost priority. This helps reduce time wasted traversing clinics and hospitals searching all containers and instead targets with high confidence which containers and their location need to be serviced if threshold of 80%> has been filled. These two notebooks follow best practice MLOps with the help of Databricks MLFlow, Spark, 

This projects goal is to forecast when a particular container needs to be serviced. 
<br>There are two ML models answering these questions:
<br>1. How many weeks out will a container need to be serviced?
<br>2. Will a container need to be serviced next week?

<hr>

**DanielsHealth_Forecasting_Analysis.ipynb** Used Data Creation to simulate real-world data for containers and their locations. Data Exploration section tell us a bit about some containers and their associated location, we really want to visualize how often each container has been serviced. Implemented Feature engineering ensuring to incorporate cyclical encodings for date using sin and cos, Lags and Deltas were used to ensure that temporal relationships are captured, and finally Rolling window statistics used to provide information of averaging out short-term fluctuations in trends. Finally saving the Containers Dataset ready for ML practices using Spark ML on Databricks.

**DanielsHealth_ML_Forecasting.ipynb** Loads the data with Spark ML. Uses MLFlow to track all runs on Databricks. And builds both models with best parameter sets for forecasting container service time and if container needs to be serviced next week.

