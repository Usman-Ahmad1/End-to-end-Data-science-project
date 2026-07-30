# 🛒 Walmart Sales Analytics & Prediction

## 📌 Project Overview
Comprehensive analysis of Walmart sales data (10,000 transactions, $1.15M revenue) combining EDA, statistical testing, and ML to predict sales and drive business decisions.

## 🎯 Objectives
- Identify revenue drivers and customer behavior patterns
- Validate findings through statistical hypothesis testing
- Build ML models to predict sales with high accuracy
- Provide data-driven business recommendations

## 📊 Dataset

| Aspect | Details |
|--------|---------|
| **Records** | 10,000 transactions |
| **Time Period** | May 2019 – June 2023 |
| **Total Revenue** | $1,155,753.96 |
| **Variables** | 18 (numerical + categorical + time-based) |

## ⚙️ Methodology

### Data Cleaning
- Removed `$` from prices, imputed missing values
- Converted data types, removed duplicates
- Capped outliers using IQR method

### Feature Engineering
- Created `revenue`, `is_weekend`, `is_holiday`
- Extracted date components (year, month, week, day, quarter)

### Statistical Testing
- **Shapiro-Wilk**: Tested normality (all non-normal)
- **Mann-Whitney U**: Compared 2 groups
- **Kruskal-Wallis**: Compared 3+ groups
- **Chi-Square**: Tested categorical associations
- **Spearman Correlation**: Rank correlation analysis

### Machine Learning
- **Models**: Linear Regression, Decision Tree, Random Forest, Gradient Boosting
- **Regularization**: L1 (Lasso), L2 (Ridge), ElasticNet
- **Evaluation**: R², MAE, RMSE, Cross-Validation

## 📈 Key Insights

### Revenue & Performance

| Metric | Value |
|--------|-------|
| **Total Revenue** | $1,155,753.96 |
| **Average Transaction** | $115.58 |
| **Top Category** | Fashion accessories ($481,584.55) |
| **Top Branch** | WALM009 ($25,271.22) |
| **Most Used Payment** | Credit card (35.5%) |
| **Best Month** | February ($148.51 avg) |

### Statistical Findings
- All variables **non-normal** → used non-parametric tests
- Category & Branch **significantly affect** revenue (p < 0.05)
- Payment method & Category are **dependent** (p < 0.05)
- Rating has **weak but significant** correlation with revenue (ρ = 0.058)

- <img width="2016" height="1377" alt="output" src="https://github.com/user-attachments/assets/c800a5a4-ad59-4b12-bab8-c87ca6e28121" />

### Machine Learning Performance

| Model | R² | MAE | CV R² |
|-------|----|----|-------|
| **Random Forest** | **0.9999** | **$0.19** | **0.9998** |
| Decision Tree | 0.9998 | $0.22 | 0.9997 |
| Gradient Boosting | 0.9994 | $1.38 | 0.9992 |
| Linear Regression | 0.8896 | $18.73 | 0.8865 |

### Feature Importance (Random Forest)
1. **quantity** (58.8%) ← **Key driver**
2. unit_price (22.1%)
3. profit_margin (8.7%)
-<img width="1790" height="985" alt="output1" src="https://github.com/user-attachments/assets/4b2e7c8c-fd28-4c08-b816-bf73ee395642" />

## 💡 Business Recommendations

### Short-Term (0-3 Months)
- ✅ **Boost Fashion Accessories**: Increase inventory & marketing
- ✅ **Promote Credit Cards**: Launch rewards program
- ✅ **Fix Low Performers**: Revitalize Health & Beauty category

### Medium-Term (3-6 Months)
- ✅ **Branch Strategy**: Replicate top branch success
- ✅ **Customer Experience**: Improve ratings to 6.5/10

### Long-Term (6-12 Months)
- ✅ **ML Deployment**: Real-time sales forecasting
- ✅ **Seasonal Strategy**: Boost November sales
- ✅ **Dashboard**: Automated performance tracking

## 📌 Conclusion
The Random Forest model achieves **99.99% accuracy** with **$0.19 average error**, providing exceptional forecasting capability. **Quantity** is the most critical revenue driver (58.8% importance), and **Fashion accessories** is the top-performing category. These insights enable data-driven decisions for inventory, marketing, and growth strategies.

