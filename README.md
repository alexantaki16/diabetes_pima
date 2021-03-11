Welcome to my Pima Native American Project from Kaggle!

If you wish to see the code switch to the master branch and go into the code folder.  The file called pima-native-american-final.ipynb is the one that is the finished product.  If you wish to see my thought process then feel free to navigate through the other notebooks.

This is the notebook that will serve as the analysis and model building of the Pima Native Americans datasets from Kaggle.

# DISCLAIMER: I am by no means legally able to give any kind of health advice.  I am not a doctor of any kind, nor do I claim to be.  Take this analysis for what it is.  Please do not take this as advice or try to input information to see if you have diabetes.

<h3>Goals of this project</h3>
- Develop a strong structure to follow, as in a framework so I have the ability to use this a guide for future projects.

- Commit to GitHub so I can track my progress

- Foster my intuition on which plots are the best for certain types of data

- Standardize and normalize data quickly

- Feature Engineering ideas?

- Practice modularizing my code to make it easier to use


#Questions

- What kind of data are dealing with - structured or unstructred?
  - Structured data for sure

- Does the data have categorical, numerical, ordinal, or time series data?
  - Numerical

- What are my feature variables (inputs) and what are my target variables (outputs)?
  - The feature variables are here:
    - Pregnancy count
    - Glucose level
    - BloodPressure
    - SkinThickness
    - Insulin
    - BMI
    - DiabetesPedigreeFunction
    - Age

- Are we missing any data?
  - Thankful no!

- Are we dealing with outliers?
  - Sure are, we will handle this in the notebook

#Data Dictionary

* *FYI: Everyone person in this dataset is a woman at age 21 or higher*

| Column | Meaning | Thoughts |
|------- | ------- | -------- |
|Pregnancies | Number of times pregnant | An integer.  What is the min and what is the max?  |
| Glucose | Plasma glucose concentration a 2 hours in an oral glucose tolerance test | Measured in mmol/L?  1 mmol/L = 18 mg/dL.  I need to multiply by 18 to get the measurement for the HOMA IR Score|
|Blood Pressure | Diastolic blood pressure | mm Hg.  Can we figure out the systolic?  The number we are given is the second one -- 120/80 |
|SkinThickness | Triceps skin fold thickness (mm) | This seems kinda normal|
|Insulin | 2 hour serum insuling (muU/ml) | Measured in muU/ml.|
|BMI | Body mass index (weight in kg/(height in meters)<sup>2</sup> | Traditional measurement |
|Diabetes Pedigree | Diabetes Pedigree Function | A function used to determine whether you have diabetes given your family history |
|Age | Age in years| This is a normal whole integer |
|Outcome | Class variable (0 or 1) 268 of 768 are 1, the others are 0|  We have an imbalance so we can handle that but let's start without that|

**Future Enhancement for Feature Engineering**
HOMA - IR Blood Code 
- Insulin * Glucose = HOMA-IR
- Healthy is 0.5 - 1.5
- Less than 1.0 means you are insulin- sensitive, which is optimal
- A range of 1 - 1.9 is within "Normal limits"
- Above 1.9 indicates early insuling resistance
- Above 2.9 indicates significant signal resistance


#Models

What models do I want to use?
  - Dense network
  - Random Forrest
  - Logistic Regression
  - SVM
  - XGBoosst
