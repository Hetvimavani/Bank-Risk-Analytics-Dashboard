# Bank Risk Analytics Dashboard

## 1. Project Overview
This project demonstrates an end-to-end data analytics workflow designed for the **banking and financial services sector**.  
The goal is to analyze customer-level financial data to assess **loan and deposit risk**, understand repayment patterns, and provide actionable insights through an interactive Power BI dashboard connected directly to a MySQL database.

The project covers the complete lifecycle — from **data ingestion** and **exploratory data analysis (EDA)** in Python to **live visualization and reporting** in Power BI.

---

## 2. Problem Statement
Banks and financial institutions face significant risk when issuing loans or managing customer portfolios.  
This project aims to build a **risk analytics framework** that helps understand patterns of:
- Loan disbursement and repayment capacity  
- Deposit and savings behavior  
- Customer segmentation by income and relationship type  
- Overall on-time and in-full payment behavior  

By doing so, it minimizes the risk of **financial loss due to default** and supports **data-driven lending decisions**.

---

## 3. Objectives
- Develop a data-driven understanding of customer risk.  
- Conduct exploratory data analysis (EDA) using Python.  
- Design key metrics for **Loan Performance** and **Deposit Patterns**.  
- Build a professional Power BI dashboard connected to a **live MySQL database**.  
- Visualize customer insights through intuitive pages (Home, Loan, Deposit, Summary).

---

## 4. Data Architecture & Workflow

```text
               +----------------------+
               |   Excel Data Source  |
               | (Raw Bank Data File) |
               +----------+-----------+
                          |
                          v
               +----------------------+
               |     MySQL Database   |
               |  (banking_case DB)   |
               +----------+-----------+
                          |
                          v
               +----------------------+
               |   Python (EDA, EDA)  |
               |  Feature Engineering |
               +----------+-----------+
                          |
                          v
               +----------------------+
               |   Power BI Dashboard |
               | (Live DB Connection) |
               +----------------------+
```

## 5. Exploratory Data Analysis (Python)
Performed in Jupyter Notebook using Pandas, NumPy, Seaborn, and Matplotlib.

### Key Steps
1. **Data Loading** — via `pd.read_sql()` (MySQL) or `pd.read_csv()`  
2. **Data Cleaning** — handled missing values, validated column data types  
3. **Descriptive Statistics** — used `df.describe()` and quartile analysis  
4. **Feature Engineering:**
   - Income band classification using `pd.cut()`  
   - Extracted joining year from date column  
5. **Univariate & Bivariate Analysis:**  
   - `value_counts()`, `sns.countplot()`, histograms, and grouped analysis  
6. **Correlation Matrix & Heatmap:**  
   - Strong positive correlations among deposit-related accounts (checking, savings, foreign currency)  
   - Weak relationship between income and credit card balance  
7. **Insight Extraction:**  
   - Most customers belong to middle-income category  
   - Majority hold one credit card  
   - European customers dominate loan and deposit volume  


---

## 6. Dashboard Design (Power BI)

### 6.1 Home Page

![Home Page](image-1.png)  

---

### 6.2 Loan Analysis Page
![Loan Analysis](image-2.png)
---

### 6.3 Deposit Analysis Page

![Deposit Analysis](image-3.png) 

---

## 7. Business Insights & Key Findings
- **Customer Composition:** Majority customers fall in the middle-income category.  
- **Credit Usage:** Most customers maintain one credit card; very few have three or more.  
- **Deposit Behavior:** High correlation between checking and savings accounts, indicating multi-account customers.  
- **Loan Exposure:** Private banking and retail customers form the largest loan segments.  
- **Regional Distribution:** European customers dominate both loan and deposit volumes.  
- **Risk Behavior:** No significant link between income and credit utilization, suggesting independent credit usage trends.

---

## 8. Tools & Technologies
| Category | Tools Used |
|-----------|-------------|
| Programming | Python (Pandas, NumPy, Matplotlib, Seaborn) |
| Database | MySQL |
| Visualization | Power BI Desktop |
| Data Source | CSV → MySQL |
| Environment | Jupyter Notebook / VS Code |
| Design Tool | Canva (for dashboard layout background) |

---