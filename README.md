# 📊 Bank Loan Data Analysis

This project provides a comprehensive analysis of a bank’s loan data using SQL queries. The dataset includes information such as loan status, interest rate, debt-to-income ratio (DTI), issued dates, loan purpose, and more. The analysis identifies trends, performance metrics, and insights from both a historical and current perspective.

---

## 📁 Dataset Overview

**File:** `financial_loan.csv`  
**Source:** Simulated bank loan data  
**Size:** 3,8577 records 

### 📌 Key Features in Dataset:

- `id`: Unique identifier for each loan application  
- `loan_status`: Status of the loan (`Fully Paid`, `Charged Off`, `Current`)  
- `loan_amount`: The amount funded  
- `total_payment`: Total amount received from borrower  
- `int_rate`: Interest rate  
- `dti`: Debt-to-income ratio  
- `term`: Loan duration  
- `emp_length`: Employment length of the borrower  
- `issue_date`: Date the loan was issued  
- `address_state`: State of the borrower  
- `purpose`: Purpose of the loan  
- `home_ownership`: Type of home ownership  

---

## 📊 KPIs and Analysis

### 🔹 General Metrics

| KPI | Description |
|-----|-------------|
| `Total_Loan_Applications` | Total number of loan applications |
| `Total_Funded_Amount` | Total amount funded by the bank |
| `Total_Amount_Received` | Total repayments received |
| `Avg_Interest_Rate` | Average interest rate charged |
| `Avg_DTI` | Average debt-to-income ratio |

### 🔹 Monthly Trends

- **MTD (Month-to-Date)** and **PMTD (Previous Month-to-Date)** comparisons for:
  - Number of loan applications
  - Total funded amount
  - Total amount received
  - Average interest rate
  - Average DTI

### 🔹 Loan Health Analysis

- **Good Loans**:
  - Criteria: `loan_status = Fully Paid` or `Current`
  - Metrics: Count, funded amount, and amount received

- **Bad Loans**:
  - Criteria: `loan_status = Charged Off`
  - Metrics: Count, funded amount, and amount received

- **Loan Health Ratios**:
  - Good Loan % = (Good Loans / Total Loans) × 100
  - Bad Loan % = (Bad Loans / Total Loans) × 100

### 🔹 Segment Analysis

Breakdown of loan data by:

- 📆 **Month** – Trends in loan issuance and payments
- 🗺 **State** – Geographic distribution of loan issuance
- ⌛ **Term** – Performance based on loan term (36 or 60 months)
- 🧑‍💼 **Employment Length** – How employment stability affects loan issuance
- 🏠 **Home Ownership** – Differences based on ownership status
- 🎯 **Purpose** – Categorization of loans based on usage (e.g., debt consolidation, home improvement)

---

## 🧠 SQL Queries Used

The SQL queries are designed to extract insights and are available in the `BankLoan Query Report.docx`. Examples include:

```sql
SELECT count(id) as Total_Loan_Applications FROM bank_loan_db;

SELECT 
    loan_status, 
    COUNT(id) AS LoanCount, 
    SUM(total_payment) AS Total_Amount_Received,
    SUM(loan_amount) AS Total_Funded_Amount,
    AVG(int_rate * 100) AS Interest_Rate,
    AVG(dti * 100) AS DTI
FROM bank_loan_db
GROUP BY loan_status;
```

> The queries cover over 20 unique KPIs and metrics to help understand the loan performance and risk.

---

## 📈 Insights & Use Cases

- Helps banks evaluate loan portfolio quality  
- Supports risk assessment for bad loans  
- Assists in targeting states or purposes with highest success rates  
- Helps monitor interest rate trends and borrower profiles  

---

## 🛠 Tools & Technologies

- **SQL** – For data querying and aggregation  
- **Excel / Google Sheets** – For visualization (optional)  
- **Python (Optional)** – Could be used for deeper analysis or dashboarding  
- **Power BI or Tableau (Optional)** – For visualization dashboards  

---

## 🚀 Future Work
 
- Use Python (Pandas & Matplotlib) for automation and deeper visual analysis  
- Perform predictive modeling for bad loan detection  
- Integrate real-time loan health monitoring  

---

## 👩‍💻 Author

**Kajal Ranka**  
BSc IT (Minor: BAF) | Passionate about Data Analytics & Stock Analysis  
📧 [rankakajal7@gmail.com]

---
