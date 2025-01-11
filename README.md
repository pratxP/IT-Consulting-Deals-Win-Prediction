# IT Consulting Deals Win Prediction Model

This repository contains the implementation of a predictive model to forecast the likelihood of winning IT consulting deals. 
The model is built using historical data and machine learning techniques to assist in identifying high-probability opportunities and optimizing decision-making processes.

## Project Overview

### Executive Summary
The goal of this project is to leverage machine learning to predict the success (win or loss) of IT consulting deals. 
By using historical data, we aim to provide insights into factors that influence deal outcomes and guide strategic decisions for improving business performance.

### Key Benefits:
- **Improved deal closure rates** by focusing on high-probability opportunities.
- **Data-driven insights** into factors that impact deal success.
- **Enhanced strategic decision-making** for IT consulting services.

### Project Objectives:
1. **Predictive Accuracy**: Build a machine learning model to predict the win/loss outcome of each deal.
2. **Actionable Insights**: Identify key factors (e.g., client category, deal cost, solution type) that drive deal success.
3. **Strategic Value**: Enable sales and management teams to make informed, data-driven decisions.

---

## Datasets

This project utilizes two datasets: **Global Data** and **Indian Data**. Both datasets include detailed characteristics of consulting deals, such as client category, deal cost, contract length, sector, and deal status (won/lost).

### Global Data Dictionary:

| Column Name             | Data Type   | Description                                                | Example         |
|-------------------------|-------------|------------------------------------------------------------|-----------------|
| Deal_ID                 | Integer     | A unique identifier for each consulting deal.              | 2632            |
| VP_Name                 | String      | Name of the Vice President overseeing the deal.            | John Smith      |
| Manager_Name            | String      | Name of the manager responsible for executing the deal.    | David Lee       |
| Client_Category         | String      | Category of the client (Enterprise, Non-Profit, Start-up).  | Non-Profit      |
| Solution_Type           | String      | Type of solution offered (e.g., Data Analytics, ERP).      | Data Analytics  |
| Deal_Date               | String      | Date when the deal was registered (needs conversion).      | 2023-06-22      |
| Sector                  | String      | Industry sector of the client (e.g., Finance, Healthcare). | Finance         |
| Location                | String      | Geographic location of the client or project.              | Tokyo           |
| Deal_Cost               | Float       | Total cost associated with the deal in local currency.     | 1,332,011       |
| Deal_Won_Lost           | String      | Outcome of the deal ("Won" or "Lost").                     | Won             |
| Deal_Probability        | Float       | Probability of closing the deal (0 to 1).                  | 0.75            |
| Contract_Length_Months  | Integer     | Length of the contract (months) if won.                    | 24              |
| Client_Size             | String      | Size of the client: Small, Medium, or Large.               | Medium          |
| Client_Revenue          | Float       | Annual revenue of the client in local currency.            | 249,048,100     |
| Solution_Price          | Float       | Total price of the solution offered.                       | 5,027,846       |
| Client_Satisfaction_Score| Float      | Client satisfaction rating (1 to 10).                      | 8.5             |
| Deal_Risk_Factor        | String      | Risk assessment: Low, Medium, High.                        | High            |

### Indian Data Dictionary:

| Column Name             | Data Type   | Description                                                |
|-------------------------|-------------|------------------------------------------------------------|
| Client                  | Text        | Name of the client.                                        |
| Category                | Text        | Category of the client or deal.                            |
| Solution Type           | Text        | Type of solution being provided in the deal.               |
| Deal Date               | DateTime    | Date when the deal was made.                               |
| Sector                  | Text        | Industry sector related to the deal.                       |
| Location                | Text        | Location where the deal was made.                          |
| VP Name                 | Text        | Vice President responsible for the deal.                   |
| Manager Name            | Text        | Manager responsible for the deal.                          |
| Deal Cost               | Numeric     | Financial value of the deal.                               |
| Deal Status Code        | Text        | Outcome status of the deal: "Won" or "Lost".               |

---

## Data Challenges:

1. **Missing Data**:
   - Deal Cost: 395 missing values.
   - Deal Probability: 392 missing values.
   - Client Satisfaction Score: 392 missing values.
   
   *Solution*: Imputation techniques will be applied to handle missing data.

2. **Data Type Issues**:
   - Deal Date: Needs conversion from string to DateTime format.
   - Client Size & Deal Risk Factor: Requires encoding for categorical machine learning models.

3. **Imbalanced Data**:
   - Categories like "Deal Risk Factor" and "Client Size" need to be handled carefully to avoid bias in predictions.

4. **Outliers & Data Distribution**:
   - Large deviations in Deal Cost and Client Revenue may require normalization or outlier treatment.

5. **Redundancy or Data Leakage Risks**:
   - Variables like VP Name and Manager Name may introduce biases if there's a strong correlation with deal outcomes.

---

## Approach

1. **Data Preprocessing**:
   - Handle missing data, standardize formats, and encode categorical variables.

2. **Exploratory Data Analysis (EDA)**:
   - Visualize relationships between variables and deal outcomes.

3. **Feature Engineering**:
   - Create meaningful features for machine learning models.

4. **Model Training & Testing**:
   - Use Random Forest Classifier for predicting deal outcomes (Won or Lost).

5. **Model Optimization**:
   - Tune model hyperparameters for better accuracy.

6. **Delivery**:
   - Deploy and integrate with Power BI for analysis and visualization.

---

## Model Evaluation

The model's performance is evaluated using common metrics such as:

- **True Positives (TP)**: Deals correctly predicted as Won.
- **True Negatives (TN)**: Deals correctly predicted as Lost.
- **False Positives (FP)**: Deals incorrectly predicted as Won.
- **False Negatives (FN)**: Deals incorrectly predicted as Lost.

### Algorithm Used:
- **Random Forest Classifier**: An ensemble learning method combining multiple decision trees to improve accuracy and handle imbalanced datasets (SMOTE applied).

---

## Power BI Integration

For interactive data visualization and analysis, this model integrates with Power BI, allowing for:
- Visualizing key metrics and model predictions.
- Custom reports for different teams.
- Real-time updates for deal forecasting.

---

## Vizualization


![Screenshot 2025-01-11 181247](https://github.com/user-attachments/assets/14cfb9e1-1656-4ef2-bfee-6dff3908d66e)
![Screenshot 2025-01-11 181301](https://github.com/user-attachments/assets/40301d9f-fd53-4ef6-9088-ff3f05d53990)
![Screenshot 2025-01-11 181311](https://github.com/user-attachments/assets/1a36e152-41f7-4119-8661-331be61ce49a)
![Screenshot 2025-01-11 181320](https://github.com/user-attachments/assets/21a678eb-c890-40e0-ace9-32d13540fd04)

## Project Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/it-consulting-deals-prediction.git
