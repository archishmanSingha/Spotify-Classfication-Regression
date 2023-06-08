# Spotify-Classfication-Regression

<h3>Problem Statement:</h3>

~ A regression problem that aims to predict the popularity score of a song.

~ A classification problem that aims to predict the top genre that a song belongs to.

<h3>Data Source:</h3>

~ Regression Problem: https://www.kaggle.com/t/a87732e08c094e4db43b7b7b9b68cc67

~ Classification Problem: https://www.kaggle.com/t/2b45806df59a477ab9e08bc96cff91aa


<h3>Exploratory Data Analysis (EDA) and Visualization:</h3>

~ **Correlation Heatmap** - Visual Representation of Correlation Matrix using colours to depict the strength and direction of variables in the 															dataset.

~ **Variance Inflation Factor (VIF)** - For each feature VIF was calculated by the formula *VIF = 1/(1-R^2)* where R^2 is the coefficient of 																correlation and R is the determination. If the value is too high, it shows that the feature is highly colinear with other features in the data. Strangely we found that even if we drop 'dnce' or 'bpm' , that reduced the accuracy.

~ **Outliers** - 

