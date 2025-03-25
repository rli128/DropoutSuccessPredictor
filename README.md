# **Student Dropout Prediction and Fairness Analysis**

## **Overview**
This project analyzes student dropout risks using machine learning models while evaluating fairness across gender groups. Our dataset was compiled and used to recognize students that are more likely to droupout and giving them the additional support they need to make sure that they succeed. The study implements fairness interventions to reduce disparities in model performance. We realized that there was a lower classification of female students dropping out compared to male students so we balanced the model in order to easily identify both struggling males and females at an equal rate.

Here are the features we used from the dataset
- Marital status
- Application mode
- Previous qualification
- Previous qualification (grade)
- Mother's qualification
- Father's qualification
- Admission grade
- Scholarship holder
- Age at enrollment
- Curricular units 1st sem (grade)
- Curricular units 2nd sem (grade)
- Tuition fees up to date

## **Dataset**
- The dataset originates from a higher education institution and includes various student demographic and academic features.  
- The goal is to predict **student dropout vs. graduation** using classification models.  
- The sensitive attribute examined is **Gender (Male/Female)** to ensure fair outcomes across groups.  

## **Methodology**
- **Model Used:** Logistic Regression  
- **Performance Metrics:** Accuracy, True Positive Rate (TPR), False Positive Rate (FPR)  
- **Fairness Metrics Evaluated:**  
  - **Equal Opportunity**: Ensuring similar TPRs across genders.  
  - **Equalized Odds**: Ensuring similar TPRs and FPRs across genders.  

## **Key Findings & Interventions**
### **1. Baseline Model Results**
- Achieved **84.4% accuracy** but exhibited a **24.7% TPR disparity** between male and female students.  
- The model was significantly better at predicting graduation for female students.  

### **2. Fairness Interventions Implemented**
- **Synthetic Data Augmentation:** Increased the number of female dropout samples to balance training data.  
  - **Result:** Reduced TPR disparity to **4.8%** with minimal accuracy loss.  
- **Class Reweighting:** Adjusted the model to give **higher weight to male students** in training.  
- **Post-Processing Adjustments:** Modified decision thresholds to balance disparities further.  

## **Results Summary**
| Model Version       | Accuracy | TPR Disparity (Gender) | Fairness Intervention  |
|--------------------|----------|-----------------------|----------------------|
| **Baseline**      | 84.4%    | 24.7%                 | None                |
| **Augmented Data** | 83.9%    | 4.8%              | Synthetic Data       |
| **Reweighted Model** | 84.1%    | 6.2%                 | Class Reweighting    |
| **Post-Processing Intervention** | 80.2% | **2.5%** | Affirmative action |

## **Technologies Used**
- **Python:** Pandas, NumPy, Scikit-Learn  
- **Data Visualization:** Matplotlib, Seaborn  
- **Machine Learning:** Logistic Regression  

## **Video Walkthrough**
Watch the full project explanation here: [Insert Video Link]  
