# **Credit Risk Analysis**

an analysis of credit card loan applications using Supervised Machine Learning principles

## **Resources**
----------------

* Data: LoanStats_2019Q1.csv - a dataset from **LendingClub** a peeer-to-peer lending services company
* **Software**: Jupyter Notebook 6.4.8 Numpy and Pandas libraries, as well as imbalanced-learn, and scikit-learn

## **Overview**
----------------

This Analysis' purpose was too evaluate the level of risk involved in lending for the company **_LendingClub_**. Our target variable was identified as the *Loan Status* column; while we utilized the other columns as features.  Loan status column was cleaned to only include "low risk" and "high risk" as selection criteria. The original dataset conatained 68,470 instances of "low risk" and 347 instances of "high risk" - or 99.49% of the target dataset contained low risk loan applicants.

The following six machine learning models were utilized to assess the balanced accuracy, as well as the precision and recall scores: random oversampling, synthetic minority oversampling technique (SMOTE), undersampling with cluster centoid, combination sampling using SMOTE and Edited Nearest Neighbors (SMOTEENN),balanced random forest, and AdaBoost.

## **Results**
---------------

**Random Oversampling**:

![image](https://user-images.githubusercontent.com/93295751/156905817-004f14cf-60c8-4488-b879-1f67a0318133.png)
![image](https://user-images.githubusercontent.com/93295751/156905821-79dfba5c-81ab-4345-8f6e-c02eeb30f10e.png)

## **SMOTE**:

![image](https://user-images.githubusercontent.com/93295751/156905843-7c06599e-619e-42d9-bd4c-0fcefb08c766.png)
![image](https://user-images.githubusercontent.com/93295751/156905849-58c02c43-e343-4555-bd5b-e44d2a678d58.png)

## **Undersampling CLuster Centroid**:

![image](https://user-images.githubusercontent.com/93295751/156905858-a5a15a45-94a3-4d25-abcd-0d8404b4d46a.png)
![image](https://user-images.githubusercontent.com/93295751/156905868-1921b521-6e74-4ca2-9d80-16e55edbb147.png)

## **SMOTEENN**:

![image](https://user-images.githubusercontent.com/93295751/156905889-da23d951-0e21-4234-b3aa-ffacd8f30dae.png)
![image](https://user-images.githubusercontent.com/93295751/156905898-6df4011e-212c-4357-bd85-28dbd8856e16.png)

## **Balanced Random Forest**:

![image](https://user-images.githubusercontent.com/93295751/156905917-a0b577f7-2fd8-463f-9de7-fd57ede8ef0b.png)
![image](https://user-images.githubusercontent.com/93295751/156905921-159cc2fc-2250-4b03-a887-444f1de48c53.png)

## **AdaBoost**:

![image](https://user-images.githubusercontent.com/93295751/156905928-86bc54a4-f99f-4170-8a96-cb81ee381096.png)
![image](https://user-images.githubusercontent.com/93295751/156905933-473ba4d7-be0b-4fb4-abe4-6c15e6615aac.png)

## **Summary**
--------------

Overall these models all have issues with achieving high precision on identifying "*high risk applicants*". Meaning they are bad at avoiding false postives in regards to high rsik applicants, and run a risk with wrongly dismissing many applicants as bad candidates for potential loans. however where these models shine is in thier recall values, particularly the combination sampling methods. They are therefore very good at identifying high risk applicants, perhaps they are just too aggressive to find a balance between precision and recall. Leading to low **f-1 scores** with high risk applicants. In summary my recommendation is that we go back to the drawing board and develop a different modeling algorithm to more accurately identify high risk applicants without resulting in so many false-positives. 
