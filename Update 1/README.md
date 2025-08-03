# 📊 Update 1: Exploratory Data Analysis & Risk Clustering

**Phase 1 of Lending Club Portfolio Optimization: Data Understanding and Borrower Segmentation**

## 🎯 Phase Overview

This initial phase focuses on understanding the Lending Club dataset structure, identifying key patterns in borrower behavior, and developing a foundation for risk assessment through advanced clustering techniques. The analysis combines exploratory data analysis (EDA) with unsupervised learning to segment borrowers into meaningful risk categories.

## 🏆 Key Deliverables

### **Primary Objectives Achieved:**
- ✅ **Data Preprocessing:** Clean 145+ raw features down to 25 key investment-relevant variables
- ✅ **Risk Segmentation:** Identify 3 distinct borrower clusters using K-means analysis
- ✅ **Feature Engineering:** Create 3 return metrics (optimistic, pessimistic, intermediate)
- ✅ **Dimensionality Reduction:** Apply PCA to understand underlying data structure
- ✅ **Business Insights:** Establish foundation for risk-based investment strategies

## 📊 Dataset Analysis

### **Data Source & Scale:**
- **Platform:** Lending Club historical data (2014-2015)
- **Access Method:** Wayback Machine archives
- **Raw Features:** 145 variables per loan
- **Processed Dataset:** 25 key features selected for analysis
- **Focus:** Application-time variables only (no data leakage)

### **Feature Selection Criteria:**
- **Availability:** Features available at investment decision time
- **Relevance:** Direct impact on loan performance and risk assessment
- **Quality:** Minimal missing values and high data integrity
- **Business Logic:** Actionable variables for investment strategy

## 🔬 Technical Methodology

### **1. Data Preprocessing Pipeline**

#### **Feature Engineering:**
```python
# Three return metrics created:
# 1. Optimistic Return: Assumes full repayment
# 2. Pessimistic Return: Assumes no recovery after default  
# 3. Intermediate Return: Partial recovery + interest before default
