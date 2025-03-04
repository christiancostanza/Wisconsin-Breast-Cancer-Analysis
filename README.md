# **Wisconsin Breast Cancer Data Analysis**

## **Overview**
This project analyzes the Wisconsin Breast Cancer Dataset using multiple machine learning techniques in R. The objective is to develop predictive models for cancer diagnosis and compare their performance using various validation techniques, including cross-validation, best subset selection, Lasso regression, random forests, and support vector classification.

## **Authors**
- **Nico Gonnella**
- **Christian Costanza**

 **Date:** May 5, 2024

## **Objectives**
 Perform **Exploratory Data Analysis (EDA)** to understand relationships between features.  
 Implement **Multiple Linear Regression (MLR)** for quantitative feature analysis.  
 Develop **classification models** to predict cancer diagnosis.  
 Use **validation techniques** (cross-validation, validation set approach) to assess model performance.  
 Apply **Lasso regression** for feature selection.  
 Train **Random Forest** and **Support Vector Classification (SVC)** models to improve classification accuracy.  

## **Dataset**
 **Source:** Wisconsin Breast Cancer Dataset

### **Preprocessing**
- Removed a column containing only NA values.
- Selected relevant features based on domain knowledge.

## **Requirements**
Ensure the required R libraries are installed before running the analysis:

```r
install.packages(c("tidyverse", "leaps", "glmnet", "randomForest", "e1071", "corrplot"))
```

## **Methodology**
### ** Data Preprocessing & Exploratory Analysis**
 Filtered dataset to select key features.  
 Used `pairs()` to visualize relationships between variables.  
 Generated a **correlation matrix** with `corrplot()`.  

### ** Multiple Linear Regression (MLR)**
 Built an **MLR model** to predict `compactness_mean` using relevant features.  
 Evaluated model performance using **residual plots** and **confidence intervals**.  

### ** Classification Models**
#### ** Best Subset Selection**
- Identified the most relevant features for cancer diagnosis prediction.

#### ** Lasso Regression**
- Applied **L1 regularization** to improve feature selection and reduce overfitting.

#### ** Random Forest**
- Built an **ensemble model** and assessed **feature importance**.

#### ** Support Vector Classification (SVC)**
- Tuned **hyperparameters (cost)** and evaluated **accuracy**.

## **Results & Evaluation**

| **Model**                  | **Error Metric**  | **Performance**                        |
|----------------------------|------------------|----------------------------------------|
| Best Subset Selection      | MSE = 1.0614     | Feature selection using validation set |
| Lasso Regression           | MSE = 0.0743     | Regularization improved performance    |
| Random Forest              | MSE = 1.4319     | Lower accuracy than Lasso              |
| **SVC (Best Model)**       | **Accuracy = 97.4%** | **Best performing model**        |

## **Usage**
To run the analysis, execute the following command in R:

```r
source("analysis_script.R")
```

## **Future Improvements**
 **Tune hyperparameters** further for Random Forest and SVM.  
 **Experiment with additional feature selection techniques** to refine models.  
 **Test alternative classification models** such as **Gradient Boosting**.
