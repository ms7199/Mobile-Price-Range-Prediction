# Mobile-Price-Range-Prediction


## Table of content

- [Problem Statement](#Problem-Statement)
- [Data Description](#Data-Description)
- [Observations](#Observations)


## Problem Statement

* In the competitive mobile phone market companies want to understand sales data of mobile phones and factors which drive the prices. The objective is to find out some relation between features of a mobile phone(eg:- RAM, Internal Memory, etc) and its selling price. In this problem, we do not have to predict the actual price but a price range indicating how high the price is.


## Data Description 


| Columns  | Description |
| ------------- | ------------- |
| **Battery_power**  | Total energy a battery can store in one time measured in mAh  |
| **Blue**  | Has bluetooth or not  |
|**Clock_speed**|  speed at which microprocessor executes instructions|
|**Dual_sim** | Has dual sim support or not |
|**Fc** | Front Camera mega pixels|
|**Four_g** | Has 4G or not|
|**Int_memory** | Internal Memory in Gigabytes|
|**M_dep** | Mobile Depth in cm|
|**Mobile_wt** | Weight of mobile phone|
|**N_cores** | Number of cores of processor|
|**Pc** | Primary Camera mega pixels|
|**Px_height** | Pixel Resolution Height|
|**Px_width** | Pixel Resolution Width|
|**Ram**  |Random Access Memory in Mega Bytes|
|**Sc_h** | Screen Height of mobile in cm|
|**Sc_w** | Screen Width of mobile in cm|
|**Talk_time** | longest time that a single battery charge will last when you are|
|**Three_g** | Has 3G or not|
|**Touch_screen** | Has touch screen or not|
|**Wifi** | Has wifi or not|
|**Price_range** | This is the target variable with value of 0(low cost), 1(medium cost), 2(high cost) and 3(very high cost). |

## Observations
* **Before Hyperparameter Tuning**

  *Accuracy score on train set is 98.5% and Test score is 89%.

  * Model seems to be overfitted as the differance between train and test accuracy score is almost 10%.

* **After Hyperparameter Tuning** 

  * Train accuracy remained almost same (98.3%) but the test accuracy score increased to 97%. From this we can say that

  * **SVM** performed very well as compared to other alogorithms.

  * We also observed that in terms of **Feature importances**

  * **RAM**, **battery_power**, **px_height** and **px_weight** are the important features.

  * f1 score for individual classes is also very good.

  * From the AUC ROC plot we saw that, The area under curve for each class prediction is almost and equal to **1**.

  * Hence from all these results we can say that the Support Vector Machine(SVM) model is performing very well and can be deployed for usage.
