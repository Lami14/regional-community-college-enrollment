# 📊 Amazon QuickSight Project: Regional Community College Student Enrollment Data

## 🧠 Objective
This project demonstrates how to use **Amazon QuickSight** to create and analyze a student enrollment dataset.  
It includes steps for dataset setup, calculated fields, analysis, dashboard creation, Q&A configuration, and storytelling.

All data sources and email addresses in this project are **fictional**, used only for demonstration purposes.

---

## 🧩 Project Overview

The project follows the sequence below:

1. **Create and Prepare the College Dataset**
   - Data Source Name: `Regional Community College Student Enrollment Data`
   - Manifest File: `s3://RegionalCommunityCollegeBucket/EnrollmentData/EnrollmentManifest.json`
   - Observe error (fictional S3 bucket), and cancel dataset creation.

2. **Create a New Sample Topic**
   - Topic: `Student Enrollment Statistics`
   - Wait for setup to complete (several minutes).

3. **Configure Dataset Refresh Schedule**
   - Timezone: Local timezone  
   - Start time: 12:00 AM on Sunday  
   - Frequency: Weekly  
   - Refresh on: Sunday  

4. **Configure Dataset Permissions**
   - Attempt to add fictional user: `admissions@regionalcommunity.edu`
   - Observe permission error.

5. **Dataset Enhancements**
   - Rename field: `HomeOfOrigin` ➝ `NationalOrigin`
   - Add description: “Country of Residence on admission application”
   - Add calculated field:
     ```plaintext
     ifelse({Age} < 30, 'Youth', 'Adult Continuing Education')
     ```

6. **Create an Analysis**
   - Add Visual: Number of students in each major by academic year  
   - Edit Title: “Student Majors by Year”  
   - Change format of Academic Year (remove commas)
   - Convert to Vertical Bar Chart
   - Add Pie Chart of Student Types
   - Edit Title: “Proportion of Student Types”
   - Rename Sheet: “Student Body Overview”

7. **Configure Q Topic**
   - Delete Sample Topic  
   - Create New Topic: `Regional Community College Student Data`  
   - Add Fields, Named Entities, and Verified Questions

8. **Create Dashboard**
   - Publish Analysis as `Student Enrollment Dashboard`
   - Enable Q&A
   - Test Q&A: Which Student Type has higher test scores?

9. **Create Scenario**
   - Scenario Name: `Improving Student Satisfaction Without Increasing Costs`
   - Starter Question: “How do we improve professor evaluations, while avoiding an increase in cost per course?”
   - Add Follow-up Questions

10. **Extend Analysis**
    - Add 4 visuals:
      - Professors with best average evaluations
      - Courses with best average evaluations
      - Professors with highest average course costs
      - Courses with highest average course costs

11. **Create Data Story**
    - Generate story explaining student satisfaction improvement theory
    - Add visuals, text blocks, and images
    - Change style and add your name to cover

---

## 📄 Project Deliverables

| Item | Description | Location |
|------|--------------|----------|
| 📄 Word Report | Full project report with screenshots | `docs/QuickSight_Project_Report.docx` |
| 📷 Screenshots | Labeled screenshots for each step | `screenshots/` |
| 🧾 Manifest File | Sample fictional S3 manifest | `data/EnrollmentManifest.json` |
| 🧭 README | This file | `README.md` |

---

## 🗂️ Repository Structure

```plaintext
quicksight-project/
│
├── README.md
├── docs/
│   └── QuickSight_Project_Report.docx
│
├── screenshots/
│   ├── 01_Create_Dataset_Error.png
│   ├── 02_Sample_Topic_Creation.png
│   ├── 03_Refresh_Schedule.png
│   ├── 04_Student_Majors_by_Year.png
│   ├── 05_Proportion_of_Student_Types.png
│   ├── 06_Dashboard_Overview.png
│   ├── 07_Scenario_Starter_Question.png
│   └── 08_Data_Story.png
│
├── data/
│   └── EnrollmentManifest.json
│
└── summary/
    └── Project_Overview.md
