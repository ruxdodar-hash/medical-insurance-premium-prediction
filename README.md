# Medical Insurance Premium Prediction

## Project Overview

This project applies predictive analytics and machine learning to understand the key drivers of medical insurance premium prices and to build accurate regression models for premium prediction. Using a dataset of 1,003 individuals with demographic and health-related features, I developed and compared three regression models to identify which factors most strongly influence insurance costs.

This project was completed as part of **ISOM 835: Predictive Analytics and Machine Learning** at Suffolk University's Sawyer Business School.

## Business Problem

Health insurance companies must set premiums that accurately reflect customer health risk while remaining fair and competitive. Mispriced premiums can lead to financial losses for insurers or unaffordable coverage for individuals. This project addresses two key questions:

1. **How do demographic and health factors influence individual medical insurance premium prices?**
2. **Can we build accurate regression models to predict premium prices, and which features are the most important predictors?**

## Dataset

- **Source:** Medical Insurance Premium Prediction dataset (`Medicalpremium.csv`)
- **Size:** 1,003 observations, 11 variables
- **Target Variable:** `PremiumPrice` (insurance premium amount)
- **Predictor Variables:**
  - Age
  - Diabetes (0/1)
  - Blood Pressure Problems (0/1)
  - Any Transplants (0/1)
  - Any Chronic Diseases (0/1)
  - Height
  - Weight
  - Known Allergies (0/1)
  - History of Cancer in Family (0/1)
  - Number of Major Surgeries

The dataset is clean with no missing values and all features are numeric.

## Methodology

### 1. Exploratory Data Analysis (EDA)
- Univariate analysis (distributions of key variables)
- Bivariate analysis (relationships between predictors and premium price)
- Correlation heatmap
- **6+ visualizations** including histograms, scatterplots, boxplots, and heatmaps

### 2. Data Preprocessing
- Train-test split (80/20)
- No missing values or feature engineering required

### 3. Model Development
Three regression models were implemented and compared:
- **Linear Regression** (baseline)
- **Decision Tree Regressor**
- **Random Forest Regressor**

### 4. Model Evaluation
Models were evaluated using:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² (Coefficient of Determination)

## Key Results

| Model              | MAE      | RMSE     | R²    |
|--------------------|----------|----------|-------|
| Linear Regression  | 2,923.46 | 4,289.27 | 0.625 |
| Decision Tree      | 2,070.48 | 3,625.07 | 0.732 |
| **Random Forest**  | **1,367.29** | **3,257.23** | **0.784** |

### Best Model: Random Forest Regressor
- Explains **78.4%** of the variance in premium prices
- Average prediction error of approximately **$1,367**
- Most important features:
  1. **Age** (66.6% importance)
  2. **Weight** (11.0% importance)
  3. **Any Transplants** (8.0% importance)

## Key Insights

1. **Age is the dominant cost driver:** Premium prices increase sharply with age, accounting for about two-thirds of the model's predictive power.

2. **Severe medical history significantly increases premiums:** Individuals with past transplants, chronic diseases, or multiple major surgeries face substantially higher premiums.

3. **Body weight is an important secondary factor:** Higher weight is associated with higher premiums, likely serving as a proxy for future health risk.

4. **Tree-based models outperform linear regression:** The Random Forest model captures nonlinear relationships and interactions that the linear model misses.


## Business Recommendations

1. **Use the model as decision support, not automatic pricing:** Combine model predictions with human judgment and regulatory considerations.

2. **Develop risk-based wellness programs:** Target older and higher-weight individuals with chronic disease management and preventive health initiatives.

3. **Segment customers based on risk factors:** Create differentiated pricing and service strategies for low-risk, moderate-risk, and high-risk segments.

4. **Monitor model performance over time:** Retrain regularly with new data as medical costs and population health trends evolve.

## Ethics & Responsible AI

The project includes a thorough discussion of:
- **Age and health-status discrimination concerns**
- **Privacy and data protection requirements** (e.g., HIPAA compliance)
- **Fairness mitigation strategies** (caps, subsidies, regular audits)
- **Transparency and explainability** for customer trust

## Repository Structure

```text
medical-insurance-premium-prediction/
├── data/
│   └── Medicalpremium.csv              # Dataset
├── notebook/
│   └── medical_premium_analysis.ipynb  # Google Colab notebook with full analysis
├── report/
│   └── FINAL_PROJECT_REPORT.pdf        # Complete written report 
└── README.md                           # This file

How to Run
Option 1: Open in Google Colab (Recommended)
Open the notebook file: notebook/medical_premium_analysis.ipynb in this repository.
Click "Open in Colab" (if available) or upload it manually to Colab.
Run all cells (Runtime → Run all).
Ensure the code cell that loads the data either:
Reads from this repository’s raw CSV URL, or
Reads from an uploaded Medicalpremium.csv file.

Option 2: Run Locally
Clone this repository:
git clone https://github.com/ruxdodar-hash/medical-insurance-premium-prediction.git
cd medical-insurance-premium-prediction
Install required packages:
pip install pandas numpy matplotlib seaborn scikit-learn
Open and run the Jupyter notebook:
jupyter notebook notebook/medical_premium_analysis.ipynb
Technologies Used
Python 3.x
pandas – data manipulation and analysis
NumPy – numerical computing
Matplotlib & Seaborn – data visualization
scikit-learn – machine learning models and evaluation
Google Colab – cloud-based notebook environment
GitHub – version control and project hosting

Project Deliverables
✅ Exploratory Data Analysis with 6+ visualizations
✅ Three regression models (Linear Regression, Decision Tree, Random Forest)
✅ Model comparison and evaluation
✅ Business insights and recommendations
✅ Ethics and Responsible AI discussion
✅ Complete written report (10–12 pages)
✅ Reproducible code in Google Colab
✅ Portfolio-ready GitHub repository

Author
Rutendo Darangwa
ISOM 835: Predictive Analytics and Machine Learning
Sawyer Business School, Suffolk University

License
This project is for educational purposes as part of a university course assignment.

Acknowledgments
Dataset: Medical Insurance Premium Prediction (Medicalpremium.csv), accessed from an open data source.
Course: ISOM 835, Suffolk University.
Tools: Python, scikit-learn, Google Colab, GitHub.
