# Online-course-dashboard
📊 Online Course Platform: Student Performance & Engagement Analysis

This project analyzes and visualizes student performance and engagement on an online course platform using **Excel** for data cleaning and **Power BI** for dashboard development. The dataset includes 1,200 records of student activity, feedback, and demographic information.

---

## 📁 Dataset Summary

- **Rows:** 1,200
- **Key Columns:**
  - `Student_ID`, `Name`, `Email`, `Gender`, `Country`, `Age`, `Enrollment_Date`
  - `Course_Name`, `Course_Category`
  - `Progress (%)`, `Time_Spent (hrs)`, `Completed`, `Feedback_Rating`
  - `Session_Attendance` (comma-separated session dates)

---

## 🧹 Part 1: Excel – Advanced Cleaning Tasks

### ✅ Data Cleaning & Feature Engineering

1. **Time Conversion**  
   - Normalized `Time_Spent` values (e.g., "30 mins", "1.5", "2 hrs") into consistent **hours** format.

2. **Age Imputation**  
   - Filled missing or invalid `Age` values using **median imputation**.

3. **Session Count Extraction**  
   - Extracted total number of sessions attended from `Session_Attendance` column.

4. **Email Cleanup**  
   - Identified and filtered **invalid or malformed** emails.
   - Checked and flagged **duplicate email entries**.

5. **High Performer Flag**  
   - Created `High_Performer` column for students who **completed** the course and gave a **rating ≥ 4**.

6. **New Derived Columns**  
   - `Experience_Level` based on `Age`:  
     - `<22`: Student  
     - `22–30`: Early Career  
     - `30–45`: Mid Career  
     - `45+`: Senior  
   - `Engagement_Level` based on `Time_Spent + Progress` thresholds:
     - High / Medium / Low

---

## 📊 Part 2: Power BI – Dashboard & Visual Insights

### 📁 Pages

#### 🔹 **Overview Page**
- KPIs:
  - Total Students
  - Average Progress
  - Average Feedback Rating
  - Course Completion Rate

#### 🔹 **Category Analysis**
- **Bar/Column Charts**:
  - Students by Course Category
  - Completion Rate by Country

#### 🔹 **Engagement Heatmap**
- Shows engagement intensity (Time Spent  by Course Category and experience level.

#### 🔹 **Matrix Table**
- Feedback Ratings distribution per Course (Course × Rating cross-tab)

#### 🔹 **Enrollment Trend**
- Line/Area chart for new enrollments by month.

### 🧠 Custom Measures (DAX)

- `Completion % by Category`
- `Average Time Spent per Category`
- `Progress vs. Rating Correlation` (scatter plot)

### 🔍 Drill-Through
- From KPI Cards or charts → Detailed view of individual student performance.

### 🔄 Slicers
- Filter dashboard using:
  - Course Category
  - Country
  - Experience Level

---

## 🚀 Getting Started

### Prerequisites
- Microsoft Excel
- Microsoft Power BI Desktop
