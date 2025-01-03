# Data-Science-Project

# The Problem
This project is focused on the case of the 2019 Novel Coronavirus (2019-nCov), a specified type of virus identified to affect an outbreak of respiratory illness discovered in the far eastern part of the world in Wuhan, China. Reports stated that the primary source of infection came from the link to a huge amount of seafood and animal markets, resulting in animal-to-person spread. The increase of the virus infection amongst humans in that part of the region was recorded not from the exposure to the animal market but indicating person-to-person spread. It is reported and unclear how sustainable the virus is spreading among people.

# Dataset Used
Descriptive-and-Predictive-Analysis-For-2020-CoronaVirus

# Tools Used
  - **Pandas**
  - **Interquartile Range**
  - **Matplotlib.PyPlot as plt**
  - **Correlation**
  - **KNN Classification**
  - **Logistic Regression**
  - **Decision Tree**
  - **Accuracy**
  - **ROC Curve**

This repository contains Python script for variable identification, missing value treatment, outlier identification, correlation between variables and machine learning modeling. 

## Python Script Descriptive Statistics

1. **'Import pandas as pd'**
   - **Purpose**: To import CVS file into Python Notebook for statistical and predictive analysis.

2. **'Variables'**
   - **Imported Variables**: ID, Case in Country, Unnamed, Summary, Reporting Date, Location, Country, Gender, Age, Symptom Onset, if Onset Approximated, Hospital Visit Date, Exposure Start, Exposure End, Visiting Wuhan, From Wuhan, Death, Recovered, Symptom, Source, Link.
  
   - **Selected Variables**: Case in Country, Reporting Date, Country, Gender, Age, Symptom Onset, Hospital Visit Date, Exposure Start, Exposure End, Visiting Wuahn, From Wuhan, Death, Recovered.

4. **'corona_virus.head()'**
   - **Purpose**: Used to have insight into the dataset.
  
5. **'corona_virus.info()'**
   - **Purpose**: Used to get the concise summary of the corona virus dataset.

6. **'corona_virus.dtypes()'**
   - **Purpose**: Used to check variable types for Int, Float or Object.

7. **'corona_virus.shape'**
   - **Purpose**: Used this script know the number of columns and rows present in the dataset
  
8. **'corona_virus2.rename(columns={'reporting date':'reporting_date'}, inplace=True)'**
   - **Purpose**: Changed column names such as Visiting Wuhan to Visiting_Wuhan, From Wuahn to From_Wuhan etc.
  
9. **'corona_virus2.gender  = corona_virus2.gender.str.replace('female', '0').str.replace('male', '1')'**
   - **Purpose**: Replaced categorical class values to class Binary values as well as using value_counts() to check number number of males and females.
  
10. **'corona_virus2[["reporting_date"]] = corona_virus2[["reporting_date"]].apply(pd.to_datetime)'**
    - **Purpose**: Changed date related columns to Datetime.
   
11. **'corona_virus2.fillna(0, inplace=True)'**
    - **Purpose**: Filling in the null for better result accuracy.
   
 12. **'IQR = Q3 - Q1'**
     - **Purpose**: To identify outliers with interquartile range (IQR).
    
 13. **'Box Plot'**
     - **Purpose**: Another method used to check for outliers, matplotlib inline, importing seaborn as sns and matplotlib.pyplot as plt.
     - **Box Plot Code**: plt.boxplot = corona_virus3.boxplot(grid=False, rot=45, fontsize=15).
     - plt.show().

        ![image](https://github.com/user-attachments/assets/275559fd-e7a3-4ee5-bee7-a00f86ea7e67).

   - **Seaborn Code**: sns.boxplot(corona_virus3.case_in_country).
   -  Executed the same code for other variables.

        ![image](https://github.com/user-attachments/assets/96c74724-cf76-40ff-ad42-c4d1b154285c)

   - **Histogram**: corona_virus3.case_in_country.hist().
   -  Executed the same code for the selected variables.

        ![image](https://github.com/user-attachments/assets/49d90bf6-1de5-479b-9915-ef5ba84fec69)


## Computing Correlation Metrices

1. **Correlation Metrices**: corr_p = corona_virus3[['case_in_country']].corr(method='pearson').
2. print(corr_p).

3. Used Seaborn Heatmap to showcase correlation between variables.

   ![image](https://github.com/user-attachments/assets/5c3fe7ef-b84b-4469-a6d1-eb30ad3eff3c)


1. **Feature Collection for X-Variables**: Gender, Age, Visiting_Wuhan, Recovered
2. **Target Variable**: Dealth


# MACHINE LEARNING
## Train and Test Data

1. X_train, X_test, y_train, y_test = model_selection.train_test_split(X,y,test_size=0.3,random_state=0).
2. from sklearn.preprocessing import StandardScaler
   - scaler = StandardScaler()
   - scaler.fit(X_train)
   - X_train_scaled = scaler.transform(X_train)
   - X_test_scaled = scaler.transform(X_test).
  
## Model Classification and Model Evaluation
1. Three model classification were used machine learning;
   - KNN Classification
   - Logistic Regression and
   - Decision Tree
  
2. Each model was evaluated on Accuracy and ROC Curve.
3. **Accuracy**: KNN - 0.972, Logistic Regression - 0.969, Decision Tree - 0.975
4. **ROC-Curve**: KNN - 0.784, Logistic Regression - 0.923, Decision Tree - 0.917

## ROC-Curve

  ![image](https://github.com/user-attachments/assets/2c25b69e-6769-4829-8884-d8c0a1efb916)


## Conclusion
The ROC curve and accuracy best describe the best model between Logistic Regression and Decision Trees. From the accuracy and the ROC curve, the decision tree model is the most accurate but Logistic Regression is shown in the ROC curve as the best model to choose.





   





 

  
