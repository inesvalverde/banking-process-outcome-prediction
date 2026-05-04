# banking-process-outcome-prediction

## Description
This project focuses on predicting the **final outcome of business process requests** using machine learning techniques.

By analyzing historical process data (~45,000 requests), the goal is to generate **early predictions** that help improve operational efficiency, reduce delays, and support better decision-making within the organization.

The project follows the **CRISP-DM methodology**, ensuring a structured approach from business understanding to deployment.

---

## Features

- Predicts request outcomes at **multiple stages**:
  - At process start  
  - Near completion  

- Exploratory data analysis using **Power BI**

- Pattern discovery with **Market Basket Analysis**

- Multiple machine learning models tested:
  - Naive Bayes  
  - Neural Networks  

- Handles **imbalanced data** using appropriate evaluation metrics

- Designed for **real-time integration** with process mining tools (Celonis)

---

## Tech Stack

**Languages & Tools**
- Python  
- Power BI  

**Machine Learning**
- Scikit-learn (classification models)  
- Neural Networks  

**Methodology**
- CRISP-DM  

---

## How It Works

### 1. Business Understanding
- Defined goal: predict process outcomes  
- Conducted SWOT analysis to understand context and constraints  

### 2. Data Understanding
- ~45,000 requests analyzed  
- 9 activities, 19 actions  
- Identified key patterns:
  - 70% completed on time  
  - Activity 101 strongly linked to rejection  

### 3. Data Preparation
- Feature engineering applied  
- Created:
  - `rejected_flag` → identifies rejected requests  
- Addressed:
  - Missing/inconsistent data  
  - Imbalanced classes  

### 4. Modeling
- Built models for two prediction moments:
  - Early-stage prediction  
  - Late-stage prediction  

- Tested 6 models → best performers:
  - Naive Bayes  
  - Neural Networks  

### 5. Evaluation
- Used metrics suited for imbalance:
  - Accuracy  
  - Precision  
  - Recall  
  - F1-score  

- Proposed A/B testing for real-world validation  

---

## Results

The models achieved **moderate performance**, below initial expectations.

### Key Challenges:
- Highly **imbalanced target classes**  
- Limited information in early-stage predictions  
- Similar patterns across outcome classes  
- **Data quality issues** (inconsistent user data, masked fields)

### Insights:
- Requests passing through **Activity 101** are highly likely to be canceled  
- Certain activities strongly influence final outcomes  
- Late-stage predictions perform better than early-stage ones  

---

## What I Learned

- The importance of **data quality** in machine learning performance  
- How to properly evaluate models on **imbalanced datasets**  
- The challenge of making **early predictions with limited information**  
- The value of structured methodologies like **CRISP-DM**  
- That model performance is often constrained more by **data than algorithms**  
