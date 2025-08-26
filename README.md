# -Mutual-Fund-Performance-Analysis-Dashboard

📌 Overview
This project ranks and visualizes 500+ mutual funds by combining Python-based analysis with a Power BI dashboard.
The goal was to create a data-driven fund selection system that balances returns, expense ratio, and risk-adjusted performance.

⚙️ Process

🔹 Python Analysis

Data Import & Exploration

1.Loaded mutual fund dataset (Mutual Fund.csv) using Pandas

2.Performed exploratory analysis with .head(), .describe(), .unique() to understand categories and distribution of financial metrics

Data Cleaning & Preprocessing

1.Identified and handled missing values using .isnull().sum()

2.Applied mean imputation for missing returns_3yr and returns_5yr values

3.Converted invalid entries ('-') into NaN and then numeric format

Feature Engineering & Normalization

1.Selected key financial metrics: expense_ratio, returns_1yr, returns_3yr, returns_5yr, sharpe, sortino, alpha, beta

2.Scaled values between 0 and 1 using MinMaxScaler for fair comparison

3.Inverted metrics where lower = better (expense_ratio, beta) to ensure consistent scoring

Composite Scoring System

1.Designed a weighted scoring algorithm assigning higher weights to returns and expense_ratio, while balancing risk-adjusted metrics (Sharpe, Sortino, Alpha, Beta)

2.Calculated composite score for each fund as a weighted sum of normalized features

Ranking & Output

1.Ranked funds using .rank(ascending=False) based on composite score

2.Sorted results and identified the Top 30 mutual funds

3.Automated export of ranked results into top_30_mutual_funds.xlsx for reporting

🔹 Power BI Dashboard

Data Connection & Integration

1.Imported the cleaned dataset (from Python/Excel output) into Power BI Desktop

2.Established relationships between fund categories, performance metrics, and time horizons

Data Transformation

1.Used Power Query Editor for additional data shaping (renaming columns, handling nulls, formatting numbers as %/decimal)

2.Ensured consistency between raw data and Python-generated scores

DAX Calculations & Measures

1.Created custom DAX measures for:

  Composite score calculation
  
  Rank assignment
  
  KPIs (Avg. 1Y Return, Avg. Expense Ratio, Risk Ratios)
  
2.Composite score calculation

Rank assignment

1.KPIs (Avg. 1Y Return, Avg. Expense Ratio, Risk Ratios)

2.Built calculated columns to categorize funds by risk-return profile

Dashboard Design

Designed an interactive dashboard with:

1.KPI cards → showing top metrics (returns, Sharpe, expense ratio)

2.Bar/column charts → fund ranking and category comparison

3.Scatter plots → visualizing risk vs return tradeoff

4.Tables with conditional formatting → highlighting Top 30 funds

5.Applied a clean, professional layout with filters for fund category, time horizon, and asset type

Interactivity & User Experience

1.Added slicers for fund category, AMC (fund house), and time horizon (1Y, 3Y, 5Y)

2.Enabled cross-filtering so that users can drill down into fund performance dynamically

3.Incorporated tooltips and conditional color coding for intuitive analysis

Insights & Outcomes

1.Helped identify top-performing mutual funds across categories

2.Provided a visual comparison of returns vs risk for better decision-making

3.Combined Python’s analytical rigor with Power BI’s business-friendly visuals to create a full-stack fund analysis solution

🔍 Mutual Fund Investment Insights

| Insight Category         | Summary                                      |
| ------------------------ | -------------------------------------------- |
| 💼 **Investment Trends** | Equity Funds lead with ₹1.35M Cr total size  |
| 👤 **Fund Manager**      | Vivek Sharma manages highest AUM: ₹7.3M Cr   |
| 📉 **Cost vs Return**    | Index Funds have lowest expense ratio: 0.26% |
| 🏦 **Best Return (1Y)**  | Bank of India Mutual Fund: 14.4%             |
| 🔄 **SIP vs Lumpsum**    | Avg. SIP: ₹528.50/month, Lumpsum Min: ₹3.05K |
| ⏳ **3-Year Returns**     | Equity Funds: 37.84%, Hybrid: 14.25%         |


🖼️ Dashboard Preview


<img width="763" height="500" alt="Screenshot (327)" src="https://github.com/user-attachments/assets/633894da-ba1f-4bcf-8ce5-ce2ef72abfad" />


🧠 Final Conclusion – See the Power of Investment


1.Through this project and dashboard, you can clearly see the power of investing in mutual funds when guided by data-driven insights.

2.By analyzing returns, expense ratios, risk levels, and fund manager performance, I’ve shown how even basic financial knowledge, supported by visual tools, can help improve financial decisions.

💡 This dashboard isn't just about numbers—it's about empowering people to make smarter, low-risk investments and take control of their financial future. Early and informed mutual fund investment leads to long-term wealth creation.

By combining:

Python for filtering,

Excel for cleaning,

Power BI for storytelling,

I created a tool that helps both beginners and experts make data-driven, low-risk, high-reward decisions.

🛠 Tools & Purpose

| Tool         | Purpose                                        |
| ------------ | ---------------------------------------------- |
| Python       | Data cleaning, scoring, filtering Top 30 funds |
| Excel        | Formatting, validation, supporting data        |
| Power BI     | Interactive dashboard and visual storytelling  |

✅ Feel free to fork, explore, and contribute!

🙌 Feedback Welcome

Thank you for exploring my Mutual Fund Analysis project!

I’m always open to suggestions, improvements, or collaboration ideas.

