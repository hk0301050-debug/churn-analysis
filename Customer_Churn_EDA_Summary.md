# Customer Churn Analysis – Exploratory Data Analysis

## 📊 Project Overview

Customer churn represents a critical challenge for subscription-based businesses. Retaining existing customers is significantly more cost-effective than acquiring new ones, making churn prediction and prevention essential for business sustainability and growth.

**Objective:** Perform comprehensive Exploratory Data Analysis (EDA) to identify key factors influencing customer churn and derive actionable business insights.

**Goals:**
- Understand customer behavior patterns across different segments
- Identify primary churn-driving features
- Provide data-driven insights to support customer retention strategies

---

## 📁 Dataset Understanding

The dataset contains customer information for a telecommunications company, including:

**Key Features:**
- **Demographics:** Gender, SeniorCitizen, Partner, Dependents
- **Account Information:** Tenure, Contract type, Payment method, Billing preferences
- **Services:** Phone service, Internet service, Online security, Tech support, Streaming services
- **Financial Metrics:** Monthly charges, Total charges
- **Target Variable:** Churn (Yes/No)

**Dataset Characteristics:**
- Comprehensive customer profile data
- Mix of categorical and numerical features
- Binary classification target (Churn)

---

## 🧹 Data Cleaning & Preprocessing

### Data Quality Assessment
- **Missing Values:** Identified and handled appropriately
- **Data Types:** Verified and converted where necessary (e.g., TotalCharges to numeric)
- **Duplicates:** Checked for and removed any duplicate records
- **Outliers:** Analyzed for potential anomalies in numerical features

### Feature Engineering
- Prepared categorical variables for analysis
- Ensured numerical features are properly scaled for visualization
- Created meaningful groupings for better pattern recognition

---

## 📈 Univariate Analysis

### Churn Distribution
**Key Finding:** The dataset shows a class imbalance with churn representing approximately 26-27% of customers.

**Business Implication:** While the majority of customers are retained, the substantial churn percentage indicates significant revenue leakage and highlights the importance of retention strategies.

### Numerical Features
**Tenure:**
- Wide distribution from new customers to long-term subscribers
- Significant concentration of customers with short tenure (0-10 months)

**Monthly Charges:**
- Range from low-cost basic plans to premium service packages
- Multi-modal distribution suggests different customer segments with varying service levels

**Total Charges:**
- Strong correlation with tenure (as expected)
- Right-skewed distribution with concentration at lower values

### Categorical Features
**Demographics:**
- Relatively balanced gender distribution
- Lower proportion of senior citizens
- Mix of customers with and without partners/dependents

**Service Usage:**
- Varied adoption of value-added services
- Different contract types (month-to-month, one-year, two-year)
- Multiple payment methods and billing preferences

---

## 🔍 Bivariate Analysis – Churn Drivers

### 1. **Tenure – The Primary Churn Indicator**
**Key Insight:** Strong negative correlation with churn
- **High Risk:** Customers with 0-12 months tenure show dramatically elevated churn rates
- **Stabilization:** Churn rates decrease significantly after the first year
- **Loyalty:** Long-tenure customers (36+ months) exhibit minimal churn

**Business Takeaway:** The first year is critical. Early engagement and onboarding experiences are paramount to long-term retention.

### 2. **Contract Type – Commitment Matters**
**Critical Finding:**
- **Month-to-Month:** Highest churn rate (~42-45%)
- **One Year:** Moderate churn rate (~15-20%)
- **Two Year:** Lowest churn rate (~3-5%)

**Business Implication:** Long-term contracts create significant switching barriers. Incentivizing annual or multi-year commitments can dramatically reduce churn.

### 3. **Payment Method – Automation Reduces Churn**
**Key Pattern:**
- **Electronic Check:** Highest churn rate (~45%)
- **Automatic Payments (Bank Transfer/Credit Card):** Significantly lower churn (~15-18%)

**Insight:** Manual payment methods create friction and opportunities for customers to reconsider their subscription. Automated payments improve retention through convenience and reduced decision points.

### 4. **Paperless Billing – Unexpected Churn Correlation**
**Finding:** Customers using paperless billing show higher churn rates than those receiving paper bills.

**Hypothesis:** This counterintuitive result may indicate:
- Paperless billing users are more digitally savvy and comfortable switching providers
- Digital-only communication may reduce engagement compared to physical touchpoints
- Possible confounding with other variables (e.g., month-to-month contracts)

### 5. **Monthly Charges – Price Sensitivity**
**Pattern:** Positive correlation between monthly charges and churn
- Customers paying higher monthly fees are more likely to churn
- Price sensitivity is a significant factor in customer decisions

**Business Strategy:** High-value plans require exceptional service quality and clear value proposition to justify premium pricing.

### 6. **Total Charges – New Customer Risk**
**Observation:** Lower total charges (indicating newer customers or shorter relationships) correlate with higher churn.

**Interpretation:** Reinforces the tenure finding – newer customers represent the highest risk segment.

---

## 🏠 Categorical Feature Insights

### Partner & Dependents – Household Stability
**Pattern:**
- Customers **without** partners show higher churn
- Customers **without** dependents show higher churn

**Analysis:**
- Household stability reduces churn propensity
- Shared services create stronger retention through family usage
- Greater complexity in switching providers for multi-person households

**Strategy:** Target family-oriented bundles and multi-user plans to increase stickiness.

### Service Features
**Internet Service Type:**
- Fiber optic customers may show different churn patterns than DSL users
- Service quality and speed impact satisfaction and retention

**Value-Added Services:**
- Online security, tech support, and streaming services impact churn
- Customers with multiple bundled services show lower churn (increased switching costs)

---

## 📊 Correlation Analysis

### Key Correlations with Churn:
1. **Tenure:** Strong negative correlation (↓ churn with ↑ tenure)
2. **Contract Type:** Longer contracts = lower churn
3. **Monthly Charges:** Higher charges = higher churn (price sensitivity)
4. **Total Charges:** Lower total = higher churn (new customer risk)
5. **Payment Method:** Automatic payments = lower churn

### Multicollinearity Considerations:
- Tenure and Total Charges are highly correlated (expected)
- Contract type influences both payment method and billing preferences
- Service bundles correlate with monthly charges

---

## 💼 Business Takeaways

### High-Risk Customer Segments:
1. **New customers (0-12 months tenure)** – Require intensive onboarding and early engagement
2. **Month-to-month contracts** – Target for contract upgrade incentives
3. **Electronic check users** – Encourage migration to automatic payments
4. **High monthly charge customers** – Ensure value delivery matches premium pricing
5. **Customers without partners/dependents** – May need different retention strategies

### Retention Strategies:

**1. First-Year Focus:**
- Enhanced onboarding programs
- Regular check-ins during first 90 days
- Early value demonstration
- Proactive support for new customers

**2. Contract Incentivization:**
- Offer meaningful discounts for annual/multi-year commitments
- Reduce friction in upgrade process
- Highlight long-term value and stability

**3. Payment Method Optimization:**
- Incentivize automatic payment enrollment
- Reduce barriers to payment automation
- Consider discounts for auto-pay adoption

**4. Value Communication:**
- For high-charge customers, emphasize ROI and value received
- Regular service reviews and optimization recommendations
- Proactive feature adoption and education

**5. Service Bundling:**
- Cross-sell value-added services to increase switching costs
- Create attractive bundle packages
- Demonstrate integrated service value

**6. Segment-Specific Approaches:**
- Family plans for customers with dependents
- Flexible options for single customers
- Senior-specific services and support

---

## 🎯 Conclusion

This EDA reveals that customer churn is not random but follows clear, predictable patterns. The analysis identifies **tenure, contract type, and payment method** as the primary drivers of churn, with **new customers on month-to-month contracts using manual payment methods** representing the highest-risk segment.

The findings enable data-driven retention strategies:
- **Preventive:** Target high-risk segments before they churn
- **Proactive:** Improve early customer experience and engagement
- **Strategic:** Design products and pricing that naturally reduce churn

Understanding these patterns allows the business to allocate retention resources efficiently, focusing on interventions that will have the greatest impact on customer lifetime value.

---

## 🚀 Next Steps

### 1. Predictive Modeling
- Build machine learning models to predict individual customer churn probability
- Test algorithms: Logistic Regression, Random Forest, XGBoost, Neural Networks
- Implement proper cross-validation and handle class imbalance

### 2. Feature Engineering
- Create interaction features (e.g., tenure × contract type)
- Develop customer lifetime value (CLV) calculations
- Engineer temporal features for time-based patterns

### 3. Model Deployment
- Develop churn scoring system for production use
- Create customer risk dashboards
- Implement real-time churn alerts

### 4. A/B Testing
- Test retention interventions on high-risk segments
- Measure impact of contract incentives
- Validate payment method migration strategies

### 5. Advanced Analytics
- Cohort analysis for retention patterns over time
- Customer journey mapping
- Causal inference for intervention effectiveness

---

## 📚 Repository Structure

```
Customer-Churn-EDA/
├── customer_churn_analysis.ipynb      # Full EDA notebook
├── Customer_Churn_EDA_Summary.md      # This summary document
├── Customer_Churn_EDA_Summary.pdf     # Formal report version
├── README.md                          # Project overview
└── data/                              # Dataset (if shareable)
```

---

## 🛠️ Technologies Used

- **Python 3.x**
- **Libraries:** pandas, numpy, matplotlib, seaborn
- **Tools:** Jupyter Notebook, Google Colab
- **Analysis:** Statistical analysis, data visualization, pattern recognition

---

## 👤 Author

This analysis demonstrates proficiency in:
- Exploratory Data Analysis (EDA)
- Statistical thinking and hypothesis testing
- Business insight generation from data
- Data visualization and storytelling
- Strategic recommendation development

**Skills Highlighted:** Data Science, Business Analytics, Customer Analytics, Python, Statistical Analysis, Data Visualization

---

## 📝 License & Usage

This analysis is part of a data science portfolio showcasing analytical capabilities and business acumen. Feel free to explore the methodology and insights.

For questions or collaboration opportunities, please reach out!

---

*Last Updated: February 2026*
