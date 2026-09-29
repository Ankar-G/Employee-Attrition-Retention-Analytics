# HR Overview & Attrition Analytics — Power BI

An end-to-end HR analytics project analyzing employee attrition, retention, and the key drivers behind employee exits to support data-driven workforce decisions for HR and management teams.

## 📖 Project Overview

This project simulates a real-world HR analytics environment for a fictional company, **Nexus Global**. It uses Power BI to turn raw employee data into interactive dashboards that show who is leaving, when they leave, and why.

The analysis covers a workforce of 3,000 employees across departments, job roles, locations, and demographic groups. It looks at attrition from several angles: organizational structure, compensation, tenure, workload, satisfaction, career progression, and work-life balance.

The project reflects how a Data Analyst in an HR or People Analytics team might approach workforce reporting — starting from a clean employee dataset and ending with dashboards that answer real retention questions.

## ❓ Problem Statement

Employee attrition is costly. It drives up hiring and training expenses, disrupts teams, and erodes institutional knowledge. Without a structured analytics layer, HR teams struggle to answer basic but important questions:

- How many employees are leaving, and is the rate rising?
- Which departments and job roles are losing the most people?
- What factors (pay, workload, satisfaction, promotion, tenure) are linked to higher attrition?
- Which employees are at risk of leaving next?
- Where should retention efforts be focused?

This project addresses that gap by consolidating employee data into three clear, interactive Power BI dashboards.

## 🎯 Business Objectives

Develop an end-to-end HR Attrition Analytics solution to analyze:

- Overall attrition and retention rates
- Attrition trends over time
- Department and job-role attrition
- Demographic patterns (gender, age)
- Compensation and salary-band impact
- Tenure and promotion impact
- Overtime and workload impact
- Job satisfaction and performance impact
- Work-life balance and absenteeism
- Training and travel-frequency impact
- High-risk employee identification

The goal is to help HR leadership identify the root causes of attrition, prioritize retention initiatives, and support evidence-based people decisions.

## 🔄 Project Workflow

1. **Data Collection** — Organized employee-level data covering demographics, job details, compensation, performance, and exit status.
2. **Data Cleaning & Preparation** — Checked for duplicates, NULLs, and inconsistent values, and created grouped fields (salary band, tenure group, overtime group, age group, absence group).
3. **Data Modeling (Power BI)** — Loaded the cleaned data into Power BI and structured it for analysis.
4. **DAX Measures** — Created KPI and analytical measures for attrition, retention, tenure, and risk.
5. **Dashboard Development** — Designed three interactive dashboards: overview, attrition drivers, and retention insights.
6. **Insight Generation** — Interpreted the visuals to produce clear, business-relevant takeaways.

## 🗃️ Dataset & Data Model

The dataset contains **3,000 employee records**. The fields below are the ones used in the dashboards.

> **Note:** Column names are based on the fields used in the visuals. Update them to match your actual dataset if they differ.

| Category | Fields |
|---|---|
| **Employee Details** | Employee ID, Gender, Age, Age Group |
| **Job Details** | Department, Job Role, Job Level, Location |
| **Compensation** | Salary, Salary Band (A–E) |
| **Tenure & Career** | Tenure (Years), Tenure Group, Years Since Last Promotion |
| **Workload & Wellbeing** | Overtime Hours / Month, Work-Life Balance (1–5), Absence Days, Absence Group, Travel Frequency |
| **Performance & Engagement** | Performance Rating, Job Satisfaction (1–4), Training Status |
| **Attrition** | Attrition Flag (Yes/No), Attrition Type (Voluntary/Involuntary), Exit Month, Exit Reason |

## 🧹 Data Cleaning & Preparation

Before analysis, the data was validated and prepared for consistency:

- Verified the record count (3,000 employees).
- Checked for duplicate employee records.
- Identified and reviewed NULL values in critical fields.
- Standardized categorical values (department, job role, gender, location).
- Created grouped fields for analysis: salary bands, tenure groups, overtime-hour ranges, age groups, and absence-day groups.
- Prepared date fields to support the month-wise attrition trend.

## ⚙️ Feature Engineering / Calculated Measures

| Metric | Formula |
|---|---|
| **Total Employees** | Count of employee records |
| **Employees Left** | Count of employees where Attrition = Yes |
| **Attrition Rate %** | Employees Left ÷ Total Employees |
| **Retention Rate %** | 1 − Attrition Rate |
| **Voluntary Attrition** | Count of leavers with Attrition Type = Voluntary |
| **Average Tenure** | Average years of service |
| **Average Salary** | Average of Salary |
| **Average Job Satisfaction** | Average satisfaction score |
| **Average Overtime / Month** | Average monthly overtime hours |
| **Avg Years Since Promotion** | Average of years since last promotion |
| **Avg Absence Days** | Average absence days per employee |
| **High Risk Employees** | Count of employees flagged by the risk rule *(add your rule here)* |

## 📊 Business KPIs

- Total Employees
- Employees Left
- Attrition Rate %
- Retention Rate %
- Voluntary Attrition
- Average Tenure
- High Risk Employees
- Average Salary
- Average Job Satisfaction
- Average Overtime per Month
- Average Years Since Promotion
- Average Absence Days

## 📈 Power BI Dashboard Overview

Power BI was used to build the full reporting layer, including:

- Data modeling and DAX-based KPI development
- Interactive, filterable dashboards with page navigation tabs
- Slicers for **Department, Job Role, Location, and Gender**
- A **Reset All Filter** button for quick navigation
- Trend, distribution, and driver analysis visuals

Three dashboards were built, each focused on a specific area of workforce analysis.

---

## 🧭 Dashboard 1 — HR Overview & Attrition Analytics

**Purpose:** Provide a high-level view of workforce size, attrition, and where employees are leaving from.

**KPI Cards**

| KPI | Value |
|---|---|
| Total Employees | 3,000 |
| Employees Left | 569 |
| Attrition Rate | 18.97% |
| Average Tenure | 3.69 years |

**Main Visuals**

- Attrition Trend Over Time
- Attrition Rate by Department
- Top Job Roles by Leavers
- Headcount & Leavers by Job Level
- Attrition by Gender

**Key Insights**

- Out of 3,000 employees, **569 have left**, giving an overall attrition rate of **18.97%**.
- Monthly leavers rise sharply through the year, from **22 in January** to **136 in December**.
- **October to December accounts for 289 of the 569 exits (about 51%)**, so attrition is heavily concentrated in the final quarter.
- **Customer Support has the highest attrition rate at 22.02%**, followed by IT (19.04%) and Finance (18.84%).
- **Procurement (16.94%) and Marketing (17.34%)** have the lowest rates.
- **Software Engineer I** has the most leavers (34), followed by IT Support Engineer (29), QA Engineer (28), and Sales Executive (28).
- **Technical Support Associate** has a small headcount (54) but 25 leavers, a notably high attrition ratio compared with other roles.
- By gender, attrition is **19.51% for Male**, **18.34% for Female**, and **14.81% for Other**.

---

## ⚠️ Dashboard 2 — Attrition Drivers & Employee Risk

**Purpose:** Identify the factors most strongly associated with employee attrition and highlight at-risk employees.

**KPI Cards**

| KPI | Value |
|---|---|
| High Risk Employees | 1,752 |
| Average Salary | 95.32K |
| Average Job Satisfaction | 2.29 |
| Average Overtime / Month | 42.96 hours |

**Main Visuals**

- Attrition by Salary Band
- Attrition by Tenure Group
- Overtime Hours vs Attrition
- Job Satisfaction by Attrition
- Promotion Status vs Attrition
- Performance Rating vs Attrition
- Age Demographics & Attrition Rate

**Key Insights**

- **Salary:** Attrition falls steadily as salary band rises, from **27.23% in Band A (Entry)** to **10.00% in Band E (Director)**.
- **Tenure:** Employees in their first year are the most likely to leave, with **31.82% attrition in the 0–1 year group**, roughly double the rate of most other tenure groups.
- **Overtime:** Attrition climbs with workload, from **10.81% (1–20 hours)** to **30.94% (60+ hours)**.
- **Job satisfaction:** Attrition is **27.80% for low satisfaction** versus **9.83% for very high satisfaction**.
- **Promotion:** Attrition is highest among employees promoted less than a year ago (0.24) and lowest in the 3–4 year group (0.13).
- **Performance:** Lower-rated employees show higher attrition, with the rate falling from 0.27 (Medium) to 0.18 (Very High).
- **Age:** The youngest age group has the highest attrition rate (0.28), and the 46–55 group has the lowest (0.10).
- An average job satisfaction score of **2.29** and average overtime of about **43 hours per month** point to workload and engagement as key areas to watch.

---

## 🔁 Dashboard 3 — Retention & HR Insights

**Purpose:** Examine the retention side of the story and the employee-experience factors linked to exits.

**KPI Cards**

| KPI | Value |
|---|---|
| Retention Rate | 81.03% |
| Voluntary Attrition | 299 |
| Avg Years Since Promotion | 1.85 |
| Avg Absence Days | 6.61 |

**Main Visuals**

- Attrition by Training Status
- Attrition by Travel Frequency
- Attrition by Work-Life Balance
- Attrition by Absence Days Group
- Key Retention Insights (text summary)

**Key Insights**

- The overall **retention rate is 81.03%**, and **299 exits were voluntary**, which is more than half of all leavers.
- **Work-life balance** is one of the strongest signals: attrition falls from **30.77% at Level 1** to **5.41% at Level 5**.
- **Absence** is another clear signal: employees with **15+ absence days** have a **37.50%** attrition rate, versus about 18% for those with 1–10 absence days.
- **Travel frequency** shows a relatively small spread, with attrition ranging from about **17% to 21%** across groups.
- **Training status** shows little difference between employees who completed training (0.199) and those who did not (0.181).
- **Career growth and better opportunities** are among the major recorded reasons for employee exits.

---

## 💡 Key Insights

- The company lost **569 of 3,000 employees (18.97%)**, and exits accelerate sharply toward the end of the year.
- **Customer Support** is the highest-attrition department, while roles such as **Software Engineer I** and **IT Support Engineer** account for the most leavers.
- **Early-career, entry-level employees** are the most at risk, with high attrition in the 0–1 year tenure group, Band A salary group, and youngest age group.
- **Overtime above 60 hours per month** is linked to roughly three times the attrition of the lowest overtime group.
- **Low job satisfaction, poor work-life balance, and high absence** all correspond to significantly higher attrition.
- Attrition differences by gender, travel frequency, and training status are relatively small compared with the workload and engagement drivers.

## 🚀 Business Value

This project supports the kind of decisions HR and leadership teams regularly face:

- **Attrition monitoring** — track exits and retention over time.
- **Targeted retention planning** — focus on high-attrition departments and roles.
- **Compensation review** — assess the impact of pay levels on retention.
- **Workload management** — identify overtime levels that push people to leave.
- **Onboarding improvement** — address early-tenure attrition.
- **Employee engagement** — act on satisfaction, work-life balance, and absence signals.
- **Career development** — improve promotion and growth pathways.
- **Risk identification** — flag employees who may need proactive attention.

As a portfolio project, it demonstrates the analytical workflow and reporting structure of a real People Analytics function, using a simulated dataset.

## ❔ Business Questions Answered

1. What is the overall attrition and retention rate?
2. How does attrition change month by month?
3. Which departments have the highest attrition?
4. Which job roles lose the most employees?
5. How does attrition differ by gender and age?
6. How do salary band and tenure affect attrition?
7. Does overtime increase the likelihood of leaving?
8. How do job satisfaction, promotion, and performance relate to attrition?
9. How much do work-life balance and absenteeism matter?
10. Do training status and travel frequency influence attrition?
11. How many employees are at high risk of leaving?
12. Where should retention efforts be prioritized?

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Power BI | Interactive dashboard development |
| DAX | KPI and analytical measure development |
| Power Query | Data cleaning and transformation |
| Excel / CSV | Source data and preparation |

## 📁 Project Structure

```
hr-attrition-analytics/
│
├── Data/
│   └── HR_Employee_Data.csv
│
├── PowerBI/
│   └── hr-attrition-analytics.pbix
│
├── Screenshots/
│   ├── hr-overview-attrition-analytics.png
│   ├── attrition-drivers-employee-risk.png
│   └── retention-hr-insights.png
│
└── README.md
```

> **Note:** File and folder names above are placeholders. Update them to match your actual repository files if they differ.

## 🖼️ Dashboard Preview

### HR Overview & Attrition Analytics
![HR Overview & Attrition Analytics](https://github.com/Ankar-G/Employee-Attrition-Retention-Analytics/blob/main/Dashbaords%20Screenshots/Screenshot%202026-09-29%20120537.png)

### Attrition Drivers & Employee Risk
![Attrition Drivers & Employee Risk](https://github.com/Ankar-G/Employee-Attrition-Retention-Analytics/blob/main/Dashbaords%20Screenshots/Screenshot%202026-09-29%20120554.png)

### Retention & HR Insights
![Retention & HR Insights](https://github.com/Ankar-G/Employee-Attrition-Retention-Analytics/blob/main/Dashbaords%20Screenshots/Screenshot%202026-09-29%20123627.png)

## 📌 GitHub Image Path Setup

To ensure dashboard screenshots render correctly on GitHub:

1. Create a folder named `Screenshots/` in the root of the repository.
2. Add the three dashboard screenshots using the exact filenames listed above.
3. Keep the relative paths (`Screenshots/filename.png`) as used in this README — do not use absolute local file paths.
4. Preview the README on GitHub to confirm the images render before finalizing.

## 🤝 Connect With Me

If you have feedback on this project or would like to discuss it, feel free to reach out.

- **LinkedIn:** [Add your LinkedIn URL here]
- **Email:** [Add your email here]
- **Portfolio:** [Add your portfolio URL here]

⭐ If you found this project useful or interesting, consider giving the repository a star.
