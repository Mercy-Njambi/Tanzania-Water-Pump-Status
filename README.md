# Tanzania-Water-Pump-Status
## Introduction
This project was on anaysis and modelling of Tanzanian water pumps.The project followed the CRISP-DM framework as shown below:
![CRISP-DM](https://user-images.githubusercontent.com/58382818/182008486-01c0a56b-f055-4d94-b38f-7d838d5f8b0f.png)

### Business understanding:
#### Problem:
Tanzania has a population of 59 million. According to [water.org](https://water.org/our-impact/where-we-work/tanzania/#:~:text=4%20million%20people%20in%20Tanzania,long%20distances%20to%20collect%20water.) 29 million people in Tanzania lack access to improved sanitazation while 4 million people lack access to safe drinking water. 

#### Aim :
According to [UNICEF](https://www.unicef.org/tanzania/what-we-do/wash) as part of its Vision 2025, the Government of Tanzania has pledged to increase access to improved sanitation to 95 per cent by 2025. The Second Five Year Development Plan (FYDP II) has also set the target for access to improved sanitation facilities at 85 percent in rural areas. In light of this, Tanzania is trying to improve their water pump maintenance operations in order to ensure that clean, potable water is available to communities across Tanzania. 

In order to accomplish this, the Government wants to be able to better predict which pumps will fail, and to better identify pumps that need repair and what also identify the  factors that need to be considered in the future. This will help in improving maintenance efficiency and water access, and they have contracted Roots engineering company to make this happen.
 ### Data Understanding
 #### Data:
The dataset used for this anaysis was downloaded from [DrivenData](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/data/). The data was was acquired from [Taarifa](https://taarifa.org/) and [Tanzanian Ministry of Water](https://www.maji.go.tz/). The data contains information about wells in Tanzania. The data has three files: training set values, training set labels and test set values. The training data was used. This data contained 59,400 rows and 40 columns. The data description was also provided by DrivenData.

### Data Preparation
Before modelling could be done, the data was firts cleaned and preprocessed. The data was checked for null values and also duplicates. This data had a lot of columns that had similar information, meaning some had to be dropped. Some Exploratory Data Analysis(EDA) was done to the data to determine if there was any patterns in the data. This data had a lot of categorical columns, meaning that these columns had to be converted to numeric features in order to be used in modelling. The categorical columns were one hot encoded, and the numeric columns were scaled due to the huge difference in magnitude in the data. This data was then ready for modelling.

### Modelling
The data was split into training and test, where training was used to fit the models, while test data was used to assess the models. A baseline model was created using Decision Trees. Random Forest and K-Nearest Neighbor were also used. GridSearchCV was used first, but was computationally expensive, hence RandomizedSearchCV was used for the rest of the iterations.

### Evaluation
The evaluation metric used was accuracy score . The model had a a training score of 0.88 and a testing score of 0.8. This model performed the best, hence why it was picked as the final model. It also had an overall accuracy of 0.8, which means that the model is able to correctly classify 80% of the features. This model had the following features as the most important:
![image](https://user-images.githubusercontent.com/58382818/182107223-6f9c5353-37aa-4744-99be-5ffee4778dba.png)

## Conclusions
- The final random forest classifier is suitable for this business case, and is ready for deployment.
- Location is a crucial factor in predicting the status of the water point.
- Water points with enough water are at a higher chance to fail, and should be closely monitored.
- Water points with high population tend to wear out quickly, hence, higher chances of the wells needing repair, or them not functioning.
- Places with low GPS values have higher chances of having water points that need repair or that don't function

## Recommendations
- Water points that are in close proximity to those that need repairs or are non-functional should be accessed frequently since they are most likey to also suffer the fate of needing repair or becoming non-functional.
- Water points with enough water should be closely monitored, as the high use could lead to their failure.
- Water points with high use population should be closely monitored.
- Low lying areas need to be have the water points checked more often to avoid them failing and needing repair

## Repository Guide
- The raw data used for the project can be found [here](https://github.com/Mercy-Njambi/Tanzania-Water-Pump-Status/tree/main/Data/Raw)
- The cleaned data can be found [here](https://github.com/Mercy-Njambi/Tanzania-Water-Pump-Status/tree/main/Data/Processed)
- The images from EDA can be found [here](https://github.com/Mercy-Njambi/Tanzania-Water-Pump-Status/tree/main/Images)
- The notebook that contains the project can be found [here](https://github.com/Mercy-Njambi/Tanzania-Water-Pump-Status/blob/main/Tanzania%20Water%20Pump%20Status%20Modelling.ipynb)
- The presentation for this project can be found [here](https://github.com/Mercy-Njambi/Tanzania-Water-Pump-Status/blob/main/Tanzania%20Water%20Points%20Status%20Modelling%20Presentation.pdf)

