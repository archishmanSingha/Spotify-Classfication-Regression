# Spotify-Classfication-Regression

<h3>Problem Statement:</h3>

* A regression problem that aims to predict the popularity score of a song.

* A classification problem that aims to predict the top genre that a song belongs to.

<h3>Data Source:</h3>

* Regression Problem: https://www.kaggle.com/t/a87732e08c094e4db43b7b7b9b68cc67

* Classification Problem: https://www.kaggle.com/t/2b45806df59a477ab9e08bc96cff91aa


<h3>Exploratory Data Analysis (EDA) and Visualization:</h3>

* **Correlation Heatmap** - Visual Representation of Correlation Matrix using colours to depict the strength and direction of variables in the 															dataset.

* **Variance Inflation Factor (VIF)** - For each feature VIF was calculated by the formula *VIF = 1/(1-R^2)* where R^2 is the coefficient of 																correlation and R is the determination. If the value is too high, it shows that the feature is highly colinear with other features in the data. Strangely we found that if we drop 'dnce' or 'bpm' , that reduced the accuracy of the model. This was surprising and could be future work.

* **Outliers** - The default value for the whiskers is 1.5 standard deviations. The boxplots show that some features include data point far beyond the whiskers. While it's difficult to distinguish between significant data points and outliers (noise), we found that most values greater the 3 standards from the mean were noise. *sns.boxplot()* was used to reveal potential outliers.

* **Clusters** -

* **Data Exploration** - describe, info , value counts

* **Principal Component Analysis (PCA)** -  

<h3>Data Pre- Processing:</h3>

