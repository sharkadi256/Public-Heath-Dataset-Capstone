# Public-Heath-Dataset-Capstone
An understanding of code and machine learning models for a public healthcare dataset

Public Health Trends: 2014-2016 CDC(centers for disease control and prevention) Data Analysis. 

  Me and my group built machine learning models using CDC survey data from 2011-2024 to see how accurately we could predict state-level general health ratings based on regional lifestyle habits and chronic health metrics.

  Chronic health conditions impact millions of Americans and place big financial pressure on public healthcare systems. Understanding how overall health ratings and health risks vary across different states helps public health agencies direct money and medical resources where they are needed most. By building reliable predictive models, health organizations can identify high-risk regions early and plan outreach programs.
  
  The year for the Behavioral Risk Factor Surveillance System (BRFSS) I did was the survey dataset from 2014 to 2016. I had 19,627 rows × 25 columns after removing missing numeric entries and irrelevant metadata(data about data). Variables Used: Tobacco Use, Alcohol Consumption, Cholesterol Awareness, Chronic Health Indicators, Days of Poor Health, Demographics, E-Cigarette Use, HIV-AIDS, Health Care Access/Coverage, Health Status, Hypertension Awareness, Immunization, Injury, Overweight and Obesity (BMI), Physical Activity, Colorectal Cancer Screening, Lung Cancer Screening, Oral Health, Women's Health, Fruits and Vegetables, Prostate Cancer, state location indicators, and survey sample sizes. I was surprised to find differences in survey sizes of large states and small states.
  
  Cleaned the data: I filtered the dataset for the years 2014–2016 and removed incomplete rows and unnecessary columns. Prepared the features: I converted categorical survey questions into numbers. Built the model: I created a multi-layer Neural Network to learn complex connections between survey responses. Trained and checked it: I ran the model through 50 training rounds (epochs) and tracked its performance using Mean Absolute Error (MAE) to measure how close the predictions were to the actual survey values. I plotted the Training vs. Validation Loss/MAE curve over the 50 rounds to confirm that the network was steadily improving and learning real trends without just memorizing the training data. In addition, I paired the classes into groups of three based on how close they are categorically and made charts to compare them. I created bar graphs, histograms, line graphs, Random Forest Classifier, Training vs. Validation Loss/MAE Curve, and an Actual vs. Predicted Scatter Plot.
  
    Main Result: On average, the model's predictions were off by only 1.9 percentage points (Validation MAE = 1.91).
Key Chart: The Training vs. Validation Loss/MAE curve in my notebook shows the error rate dropping smoothly over 50 training rounds (epochs) as the model learned without severe overfitting.

    I made a graph that compares high population states(large) and low population states(small)
Is it fair? Not entirely. The model made more accurate predictions for large populated states than for smaller states or territories, showing a higher error rate in less-populated areas. What's going on? The dataset contains far more survey responses from large states than from small states or territories. Because the model had less data to learn from for smaller regions, its predictions were likely to be less accurate there. 

    Limitations: BRFSS data relies on self-reported survey responses, which can make personal reporting biased.
With another week: I would pull in more socio-economic data like median household income and healthcare coverage percentages to create more graphs and see its effect on the different health topics. What not to claim: This model predicts broad state-level health trends; it cannot be used to diagnose individuals or assess an individual person's health risk.

Steps to run:
1. Open my notebook in Google Colab.

2. Click Runtime > Run all in the top menu. 

3. Files needed: None. 

4. Estimated Runtime: 2 to 3 minutes from start to finish.

My Team:

Jiya: Analyzed days of poor health and mental health metrics for 2022, 2023, 2024

Nirali: Conducted research on financial barriers of 2021, 2020, 2019

Arya: Distribution of Topicsfor Demographics, Woman's Health, Asthma, Cardiovascular disease, and Physical Activity for years 2011, 2012, 2013

Aditii: Analyzed all the Heath Status Classes and Compared for 2014, 2015, 2016

Nirvi: 2017, 2018
