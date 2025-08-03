# 📊 Dataset Information - Lending Club Loan Data

## 🔒 Data Privacy Notice
The actual Lending Club dataset used in this analysis is **not included** in this repository due to privacy considerations and data licensing restrictions. The analysis uses publicly available historical data for academic research purposes.

## 📋 Dataset Description

### **Source Information**
- **Platform:** Lending Club peer-to-peer lending platform
- **Time Period:** 2014-2015 loan originations
- **Data Type:** Historical loan performance and borrower characteristics
- **Purpose:** Portfolio optimization and risk assessment research

### **Dataset Scale**
- **Training Data:** 2014 loan cohort for model development
- **Validation Data:** 2015 loan cohort for performance testing
- **Features:** 25 key application-time variables selected from 100+ available
- **Loan Universe:** Grades A through G with varying risk profiles

## 📊 Feature Categories

### **Borrower Demographics**
- `annual_inc`: Annual income reported by borrower
- `emp_length`: Employment length in years
- `home_ownership`: Home ownership status (own, rent, mortgage)
- `verification_status`: Income verification level

### **Credit Profile**
- `fico_range_low/high`: FICO credit score ranges
- `dti`: Debt-to-income ratio
- `delinq_2yrs`: Delinquencies in past 2 years
- `open_acc`: Number of open credit accounts
- `revol_util`: Revolving credit utilization rate

### **Loan Characteristics**
- `loan_amnt`: Requested loan amount
- `term`: Loan term (36 or 60 months)
- `int_rate`: Interest rate assigned
- `grade`: Lending Club assigned grade (A-G)
- `purpose`: Stated loan purpose

### **Engineered Features**
- `ret_INTc`: Intermediate return metric (risk-adjusted)
- `default_flag`: Binary default indicator
- `risk_cluster`: Assigned risk cluster (1-20)

## 🧹 Data Preprocessing

### **Feature Engineering Steps:**
1. **Return Calculation:** Created multiple return metrics, selected intermediate for realism
2. **Risk Segmentation:** Applied K-means clustering to identify 20 borrower segments
3. **Missing Value Treatment:** Systematic handling of incomplete records
4. **Outlier Management:** Appropriate treatment for extreme values
5. **Categorical Encoding:** Proper handling of grade and purpose variables

### **Quality Assurance:**
- **Temporal Validation:** No future information leakage in features
- **Business Logic:** All features available at application time
- **Statistical Validation:** Distribution analysis and correlation checks

## 📈 Risk Clustering Results

### **Cluster Characteristics:**
- **20 Distinct Segments:** Each with unique risk/return profile
- **Interpretable Patterns:** Clusters show clear borrower characteristic patterns
- **Risk Differentiation:** Significant variance in default rates across clusters
- **Return Predictability:** Stable return patterns within clusters

### **Example Cluster Profiles:**
- **Low-Risk Cluster:** High income (>$60K), low DTI (<20%), Grade B-C
- **Moderate-Risk Cluster:** Medium income, stable employment, Grade C-D
- **High-Risk Cluster:** Lower income, higher DTI, Grade E-G

## 🎯 Target Variables

### **Return Metrics:**
- **ret_INTc:** Primary return metric balancing realism and optimization
- **Expected Return:** Predicted return from XGBoost model
- **Actual Return:** Historical performance for validation

### **Risk Measures:**
- **Cluster Volatility:** Standard deviation of returns within each cluster
- **Default Probability:** Binary default prediction
- **Portfolio Risk:** Aggregated risk across selected loans

## 📊 Data Access & Replication

### **Public Data Source:**
The Lending Club historical data is available through:
- **Lending Club:** Historical loan data (subject to terms of use)
- **Academic Access:** Available for research purposes with proper attribution
- **Kaggle Datasets:** Historical Lending Club data for analysis

### **Replication Guidelines:**
1. **Data Acquisition:** Obtain historical Lending Club data from official sources
2. **Feature Engineering:** Apply preprocessing steps outlined in analysis code
3. **Model Training:** Follow methodology documented in notebooks
4. **Validation:** Use 2014-2015 split for temporal validation

## ⚖️ Ethical Considerations

### **Responsible Lending:**
- Analysis focuses on risk assessment, not discriminatory practices
- All features are application-time and borrower-provided
- No use of protected characteristics for unfair discrimination

### **Data Usage:**
- Historical data used for academic research only
- No personal identifying information included
- Aggregate analysis respects individual privacy

### **Investment Guidance:**
- Results for educational and research purposes
- Not financial advice or investment recommendations
- Past performance does not guarantee future results

---

**Note:** This analysis demonstrates quantitative finance methodologies and can be adapted to similar lending or investment datasets with appropriate modifications to features and risk models.
