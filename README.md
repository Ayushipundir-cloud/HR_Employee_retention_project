# HR Analytics Dashboard | Power BI

An interactive **Power BI dashboard** built to analyze employee attrition, workforce demographics, compensation trends, and work-life balance — enabling HR teams and business leaders to make smarter, data-backed people decisions.

---

## 📸 Dashboard Preview
-[View Dashboard](https://github.com/Ayushipundir-cloud/HR_Employee_retention_project/blob/main/HR_Dashboard.pbix)

## 📌 Project Overview

Employee attrition is one of the costliest challenges for any organization. This dashboard transforms raw HR data into clear, actionable visuals — helping identify **who is leaving, why they might be leaving, and what patterns exist across departments and roles**.

Built on a dataset of **50,000 employees**, it tracks attrition trends, compensation benchmarks, promotion history, and work-life balance scores — all filterable in real time.

---

## 📊 Key KPI Cards

| KPI | Value |
|---|---|
| 👥 Total Employees | 50,000 |
| 📉 Attrition Count | 25,105 |
| 📊 Attrition Rate | 50.21% |
| 💰 Avg Hourly Rate | $114.45 |
| 🗓️ Avg Working Years | 20.50 years |
| ⚖️ Avg Work-Life Balance Score | 2.50 / 5 |

---

## 🔍 Visuals & What They Reveal

### 📈 Attrition Rate vs. Year Since Last Promotion *(Stacked Area Chart)*
Tracks how attrition changes based on how long it's been since an employee was last promoted.
> **Key Finding:** Attrition peaks at **50.96%** for employees with 20+ years since their last promotion — a clear signal that career stagnation drives exits more than compensation alone.

### 📉 Attrition Rate vs. Monthly Income *(Line Chart)*
Maps attrition percentage across monthly income brackets (<10K to 50K+).
> **Key Finding:** Employees earning **40K–50K** and **50K+** show the highest attrition (50.84%, 51.26%) — countering the assumption that higher pay always improves retention.

### 🥧 Attrition Rate by Department *(Pie Chart)*
Breaks down attrition share across departments: Software, Sales, Support, Hardware, Human Resources, Research & Development.
> Each slice is approximately **16–17%**, revealing attrition is distributed evenly — a systemic issue, not department-specific.

### 🍩 Avg Working Years by Department *(Donut Chart)*
Shows average employee tenure across departments.
> All departments cluster near **20 years**, indicating a seasoned but potentially stagnant workforce.

### 🗂️ Work-Life Balance by Job Role *(Treemap)*
Displays work-life balance scores for every job role: Research Scientist, Developer, Manager, Healthcare Representative, Sales Representative, HR, Manufacturing Director, and more.
> Score range: **2.47–2.51** — uniformly low across roles, suggesting a company-wide culture challenge rather than role-specific burnout.

### 📊 Avg Hourly Rate Male RS *(Gauge Chart)*
Visualizes the average hourly rate for male Research Scientists on a scale of 0–200.
> Current value: **$114.45** — useful for gender pay equity analysis when compared with female counterparts.

---

## 🎛️ Interactive Filters (Slicers)

| Slicer | Options |
|---|---|
| 🏢 Department | All / Software / Sales / Support / Hardware / Human Resources / Research & Dev |
| 👤 Gender | All / Male / Female |
| 💼 Job Role | All / Manager / Developer / Research Scientist / Sales Representative / HR / etc. |

All visuals update dynamically based on slicer selections — enabling deep-dive analysis at any combination level.

## 🛠️ Tools & Technologies

|TOOLS| PURPOSE|
|---|---|
| **Power BI Desktop** | Dashboard design, layout & publishing |
| **DAX (Data Analysis Expressions)** | Custom measures: `Attrition Rate %`, `Attrition Count`, `Average Hourly Rate Male RS`, `Avg Work Life Balance`, `Avg Working Years`, `Total Employees` |
| **Power Query (M Language)** | Data cleaning, transformation & custom column creation (`YearSinceLastPromotionCustom`, `Monthly Custom`) |
| **Excel / CSV** | Source data preparation & staging

## 📐 DAX Measures Used

* Attrition Rate %
Attrition Rate % = DIVIDE([Attrition Count], [Total Employees], 0)

* Attrition Count
Attrition Count = COUNTROWS(FILTER(HR_Data, HR_Data[Attrition] = "Yes"))

* Total Employees
Total Employees = COUNTROWS(HR_Data)

* Avg Work Life Balance
Avg Work Life Balance = AVERAGE(HR_Data[WorkLifeBalance])

* Avg Working Years
Avg Working Years = AVERAGE(HR_Data[TotalWorkingYears])

* Average Hourly Rate Male RS
Average Hourly Rate Male RS =
CALCULATE(
    AVERAGE(HR_Data[HourlyRate]),
    HR_Data[Gender] = "Male",
    HR_Data[JobRole] = "Research Scientist")

## 💡 Key Insights

1. **Career stagnation is the #1 attrition driver** — employees 20+ years without promotion have the highest exit rate (50.96%). Promotion pipelines need urgent review.

2. **Higher salaries don't guarantee retention** — attrition actually rises in the 40K–50K+ income bracket, pointing to engagement and growth issues beyond compensation.

3. **Attrition is a company-wide problem** — with ~16–17% per department, no single team is an outlier. This signals cultural or structural issues, not just management problems in one area.

4. **Work-life balance is universally low (2.47–2.51/5)** — every job role scores similarly, suggesting organization-wide policy changes are needed, not just role-specific fixes.

5. **Long-tenured workforce (avg. 20.5 years)** — experienced talent is walking out. The cost of replacing senior employees is significantly higher than junior 

## 🚀 How to Run

1. **Connect your data source**
   - Replace the existing source with your own HR dataset, or use the provided `hr_data.csv`
   - Ensure columns match: `Department`, `Gender`, `JobRole`, `Attrition`, `HourlyRate`, `WorkLifeBalance`, `TotalWorkingYears`, `YearsSinceLastPromotion`, `MonthlyIncome`

2. **Explore interactively**
   - Use the **Department**, **Gender**, and **Job Role** slicers to filter all visuals simultaneously

## 📈 Business Use Cases

- **HR Strategy & Planning** — Identify which departments or roles need retention programs
- **Compensation Benchmarking** — Compare hourly rates across genders and roles for pay equity audits
- **Promotion Policy Review** — Use promotion history vs. attrition data to redesign career ladders
- **Workforce Planning** — Anticipate headcount gaps based on attrition trends
- **Executive Reporting** — Clean, single-page summary for C-suite and CHRO reviews

- <img width="853" height="480" alt="Hr Recording" src="https://github.com/user-attachments/assets/7caca026-b668-418a-96c0-465f77eecd08" />


- 


