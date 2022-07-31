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
A baseline model was created using Decision Trees. Random Forest, Adaboost and XGBoost models were also used.

### Evaluation
The evaluation metric used was accuracy score and balanced accuracy score.
