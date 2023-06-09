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

* **Clusters** - The t-SNE plot below indicates that the songs cluster in a nonrandom way and that there pattern that may be exploited for classification and regression.

* **Data Exploration** - describe(), info() and value counts have been visualized to get better understanding of the data.

* **Principal Component Analysis (PCA)** -  PCA made little difference. Multiplying feature attributes,RandomOverSampling or applying other mathmematical operations on features was not useful.


<h3>Data Pre- Processing:</h3>

Next we applied data cleaning, feature selection, and feature engineering methods.

* **Cleaning** : Replacing missing value with predicted genres using ML algorithm and dropping rows with outliers (z score > three std). One duplicate row was dropped.

* **Feature selection**: The "Id" column was dropped (it's not a feature). The "pop" (popularity) feature column was dropped ... "pop" was not predictive of top genre.

* **Feature engineering**: The text features "title", "artist", and "top genre" were one-hot encoded.


<h3>Train Models:</h3>

Below are the models used with the hyper parameters provided to train the Classification and Regression Problem and the results with it.

* **Classification** : 

LR_model = LogisticRegression(C=91, max_iter=1000, penalty='l1', solver='liblinear', random_state);
<br>
Validation Score : 52.81%

SVC_model = SVC(C=1.6, gamma='scale', kernel='sigmoid', random_state=42);
<br>
Validation Score : 37.17%

RFC_model = RandomForestClassifier(n_estimators=400, max_depth=14, random_state=42);
<br>
Validation Score : 39.62%

KNN_model = KNeighborsClassifier(n_neighbors=8, weights='uniform', random_state=42);
<br>
Validation Score : 34.48%

* **Regression** :




