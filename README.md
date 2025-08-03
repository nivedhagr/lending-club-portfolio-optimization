# 📈 Lending Club Portfolio Optimization

## 🎯 Project Overview

This project develops an intelligent portfolio optimization system for Lending Club peer-to-peer loans, combining machine learning predictions with mathematical optimization to maximize returns while managing risk through sophisticated clustering-based risk assessment.

**Academic Context:** Advanced coursework project demonstrating integration of predictive modeling, unsupervised learning, and mathematical optimization for financial applications.

## 🚀 Key Achievements

| Metric | Performance | Benchmark |
|--------|-------------|-----------|
| **Portfolio Return** | 9.17% average | Market-beating performance |
| **Risk Management** | 5.04 risk exposure | Controlled through clustering |
| **Model Accuracy** | XGBoost prediction | Outperformed logistic regression |
| **Scalability** | Up to 100+ loans | Tested across multiple budgets |

## 🛠️ Technical Architecture

### **Machine Learning Pipeline:**
1. **Predictive Modeling:** XGBoost for return prediction using application-time features
2. **Risk Clustering:** K-means clustering (20 clusters) based on borrower characteristics  
3. **Portfolio Optimization:** Mathematical optimization balancing return vs. risk
4. **Performance Validation:** Backtesting on 2014-2015 Lending Club data

### **Key Features:**
- **Explainable AI:** Cluster-based risk profiles with interpretable patterns
- **Scalable Design:** Works across different budget constraints ($150K-$300K)
- **Risk-Aware:** Portfolio risk derived from loan similarity, not arbitrary rules
- **Performance Tracking:** Multiple strategies tested and compared

## 📊 Business Problem & Solution

### **Challenge:**
Traditional loan selection relies on rigid rules (interest rates, grades) that ignore:
- Portfolio-level risk diversification
- Budget constraints and scalability
- Individual borrower risk profiles beyond simple grades

### **Our Solution:**
**Cluster-Based Portfolio Optimization** that:
- Groups loans by similar borrower characteristics (20 clusters)
- Predicts returns using advanced ML (XGBoost)
- Optimizes portfolio composition for maximum risk-adjusted returns
- Provides interpretable investment strategies

## 🎯 Methodology

### **Phase 1: Data Engineering**
- **Dataset:** 2014-2015 Lending Club loans
- **Feature Engineering:** 25 key features from borrower applications
- **Return Metrics:** Engineered 3 return types, selected intermediate return for realism

### **Phase 2: Predictive Modeling**
- **Models Compared:** Logistic Regression vs. XGBoost
- **Performance:** XGBoost selected for superior prediction accuracy
- **Features:** Application-time data only (no signal leakage)

### **Phase 3: Risk Clustering**
- **Method:** K-means clustering on borrower characteristics
- **Clusters:** 20 distinct borrower segments identified
- **Risk Assessment:** Each cluster has unique return/volatility profile

### **Phase 4: Portfolio Optimization**
- **Objective:** Maximize expected return
- **Constraints:** Budget limits, loan count limits, diversification requirements
- **Risk Model:** Cluster-based volatility aggregation

## 📈 Key Findings & Insights

### **Optimal Loan Characteristics:**
- **Grade Focus:** Primarily Grades B and C (sweet spot for risk/return)
- **Income Profile:** Annual income > $60K
- **Debt-to-Income:** DTI < 20%
- **Loan Terms:** 36-month terms preferred over 60-month
- **Credit Utilization:** Revolving utilization < 60%

### **Portfolio Performance:**
- **100 Loan Portfolio:** $166,500 investment, $15,266 expected return
- **Risk-Managed:** 5.04 total risk exposure through diversification
- **Scalability:** Performance maintained across different portfolio sizes
- **Robustness:** Consistent results across multiple optimization runs

### **Strategic Insights:**
1. **Quality over Quantity:** Focused selection outperforms broad approaches
2. **Risk Clustering:** More sophisticated than grade-based risk assessment
3. **Optimization Benefits:** Algorithmic selection beats simple rules
4. **Scalability:** Framework adapts to different investor preferences

## 🔬 Model Performance

### **Prediction Accuracy:**
- **XGBoost Model:** Superior performance vs. logistic regression
- **Key Predictors:** Loan term, DTI ratio, annual income
- **Validation:** Robust performance on holdout 2015 data

### **Portfolio Strategies Tested:**
1. **Custom Strategy 4:** 21.87% return, 0% defaults (best performer)
2. **Low-Default Strategy:** Conservative approach for risk-averse investors
3. **High-Return Strategy:** Aggressive approach for return maximization
4. **Hybrid Strategies:** Balanced approaches for different risk profiles

### **Scalability Results:**
| Portfolio Size | Budget | Avg Return | Total Risk | Feasibility |
|----------------|--------|------------|------------|-------------|
| 50 loans | $150K | 8.83% | 2.62 | ✅ Optimal |
| 75 loans | $250K | 8.56% | 3.91 | ✅ Balanced |
| 100 loans | $300K | 9.26% | 5.14 | ✅ High-return |
| 125 loans | $150K | — | — | ❌ Infeasible |

## 🎯 Business Applications

### **For Individual Investors:**
- **Risk Tolerance Matching:** Customizable β parameter for different risk preferences
- **Budget Optimization:** Works across various investment amounts
- **Performance Tracking:** Clear metrics for portfolio monitoring

### **For Investment Platforms:**
- **Automated Selection:** Scalable algorithm for loan recommendation
- **Risk Assessment:** Sophisticated alternative to simple grade-based systems
- **Portfolio Construction:** Mathematical optimization for better outcomes

## 🛠️ Technical Implementation

### **Core Technologies:**
- **Machine Learning:** XGBoost, scikit-learn clustering
- **Optimization:** Mathematical programming for portfolio construction
- **Data Processing:** Advanced feature engineering and validation
- **Visualization:** Performance tracking and risk analysis

### **Repository Structure:**
- `analysis/`: Core algorithms and model implementations
- `notebooks/`: Interactive development and analysis
- `presentations/`: Executive-level results and methodology
- `outputs/`: Results, metrics, and visualizations

## 🔄 Future Enhancements

### **Model Improvements:**
- **Dynamic Risk Assessment:** Time-varying cluster assignments
- **Macroeconomic Integration:** Economic indicators in risk modeling
- **Advanced ML:** Deep learning approaches for return prediction

### **Portfolio Features:**
- **Real-time Optimization:** Dynamic rebalancing capabilities
- **Multi-objective Optimization:** Simultaneous optimization of multiple goals
- **Interactive Dashboard:** User-friendly interface for investors

## 🎓 Academic Learning Outcomes

### **Technical Skills Demonstrated:**
- **Advanced Machine Learning:** XGBoost implementation and tuning
- **Unsupervised Learning:** K-means clustering for risk segmentation
- **Mathematical Optimization:** Portfolio construction under constraints
- **Financial Modeling:** Risk-return optimization in practice

### **Business Skills Applied:**
- **Investment Strategy:** Translating models into actionable strategies
- **Risk Management:** Sophisticated approach to portfolio risk
- **Performance Analysis:** Comprehensive backtesting and validation
- **Strategic Communication:** Executive-level presentation of complex models

---

*This project demonstrates advanced quantitative finance capabilities, combining machine learning, optimization, and strategic business thinking for real-world investment applications.*
