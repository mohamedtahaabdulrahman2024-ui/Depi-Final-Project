Employee Attrition Analysis

Why do employees leave, where does it happen, and what can the company do about it?

An end-to-end data analysis of an HR dataset (1,470 employees, 35 columns). The project cleans the data, finds the company's attrition problem, explains its root causes with visuals, and proposes a targeted retention plan.

Key Numbers
Metric	Value
Employees analyzed	1,470
Employees who left	237
Overall attrition rate	16.1% (about 1 in 6)
The Problem

Attrition is not random. It piles up in a few groups:

Group	Attrition rate
Sales Representatives	39.8%
First year at the company	34.9%
Works overtime	30.5% (vs 10.4% without overtime)
Monthly income under 3K	28.6%
Frequent business travel	24.9%
No stock options	24.4%
Entry-level + overtime	52.6%
No overtime + income 5K+	6.9%

When risks combine, more than half of the people leave. Staff with no overtime and a higher income almost never do.

These are patterns in the data (association), not proof of cause. Exit interviews should confirm them.

Recommended Solution
Control overtime: cap it, rotate it fairly, and compensate it.
Fix entry-level pay: run a market pay check for Level 1 and under-3K roles.
First-year program: 90-day onboarding, a mentor, and 30/60/90-day check-ins.
Build a stake: extend stock options to Levels 1-2 and reduce travel load for Sales Representatives.
Early-warning list: flag employees who work overtime and earn under 5K (205 people, 88 exits so far) and review them monthly.

Scenario: if the plan cuts attrition in that group by one third, about 29 fewer people leave and company attrition drops from 16.1% to about 14.1%. This is an estimate to track, not a guarantee.

Dataset
File: WA_Fn-UseC_-HR-Employee-Attrition.csv (public HR analytics sample dataset, available on Kaggle)
1,470 rows, 35 columns, one row per employee
Target column: Attrition (Yes = 237, No = 1,233)
Column groups: personal, job, pay, experience, satisfaction
Data Cleaning
Check: 0 missing values, 0 duplicate rows, 0 duplicate employee numbers.
Drop: 3 constant columns removed (EmployeeCount, Over18, StandardHours).
Label: numeric codes (1-4) converted into readable labels (Low, Medium, High, Very High).
Group: created bands for age, monthly income, tenure, and commute distance.
Outliers: checked with the IQR rule and kept, because they are real values.

Result: 1,470 rows x 44 columns, saved as HR_Attrition_Clean.csv.

Analysis Method
Baseline: attrition rate = leavers / headcount.
Compare groups: attrition rate by overtime, job role, income, tenure, level, travel, and more.
Rank drivers: correlation of each numeric column with leaving.
Combine factors: find the segment with the highest attrition rate.
Scenario: estimate the effect of reducing attrition in that segment.
