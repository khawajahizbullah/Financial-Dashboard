# Financial-Dashboard
This project focuses on building a Financial Performance Dashboard in Power BI that visualizes and compares Actuals vs Budget vs Forecast across departments, countries, and business areas. It helps organizations identify cost overruns, track profitability, and optimize budget allocation through data-driven insights.

💡 Project Story

Managing budgets effectively is one of the toughest challenges for any organization. This project was inspired by the need to monitor financial efficiency in real-time — understanding where money is spent, saved, or exceeded.
By integrating multiple financial datasets, this dashboard transforms scattered numbers into a comprehensive visual story of an organization’s fiscal health.

🧩 Datasets Used

The project includes multiple relational tables that form the foundation of financial reporting:

Table	Key Columns	Description
Actuals	Date, IT Department, Cost Element, Country, Actual	Actual spend across departments
Budget	Date, IT Department, Cost Element, Country, Budget	Planned budgets for departments
Forecast	Date, IT Department, Cost Element, Country, Forecast	Predicted future expenses
Calendar	Date	Enables time intelligence
CostElements	CAPEX, Cost Element Group, Business Area	Categorizes cost types
Departments	IT Department, IT Area, Dept., Manager	Departmental hierarchy
Regions	Country, Region	Regional mapping
Dim Tables	Cost Element, Business Area, Country, Region, IT Department	Central dimension table for unified relationships
⚙️ Tools & Technologies

🧠 Power BI – Data modeling, relationships, and dashboard visualization

📊 DAX (Data Analysis Expressions) – For KPIs, calculations, and measures

📅 Calendar Table – Enables date-based analysis

🧹 Power Query – Data cleaning and transformation

🧮 Key DAX Measures
Total Actual = SUM('Actuals'[Actual])
Total Budget = SUM('Budget'[Budget])
Total Forecast = SUM('Forecast'[Forecast])
Budget Variance = [Total Actual] - [Total Budget]
Forecast Variance = [Total Forecast] - [Total Budget]
Variance % = DIVIDE([Budget Variance], [Total Budget], 0)
Profit_Loss = IF([Budget Variance] < 0, "Profit", "Loss")

📊 Key Visuals & Features

KPI Cards: Total Actual, Total Budget, Forecast, Variance %

Column Chart: Actual vs Budget by IT Department

Line Chart: Trend of Actual, Budget & Forecast over time

Treemap: Cost by Business Area or Cost Element Group

Donut Chart: Regional spend distribution

Conditional Table:

Displays Actual, Budget, Variance, Variance %

Red 🔴 for overspend, Green 🟢 for underspend using conditional formatting

Slicers: Country, Region, IT Department, Business Area, Date

📈 Insights & Takeaways

Clear visualization of Actual vs Budget vs Forecast performance.

Top departments identified for both overspending and savings.

Regional cost patterns highlight areas for optimization.

CAPEX costs identified as major variance contributors.

Enables data-driven budgeting and smarter decision-making for leadership.

✅ Final Takeaway:
This dashboard empowers organizations to monitor, compare, and act on financial performance with full transparency — transforming complex financial data into actionable insights.

🚀 Future Enhancements

Add Year-over-Year (YoY) growth visualizations

Integrate AI visuals for anomaly detection

Add drill-throughs for department-level financial summaries


🧑‍💼 About the Author

Khawaja Hizbullah
📍 Data & Business Analyst | Power BI | Python | SQL
📧 khawajahizbullah@gmail.com

🔗 LinkedIn
 | GitHub
