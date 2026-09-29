# student_performance_pbi
An interactive dashboard on Student Performance made using Microsoft Power BI. 

1. Student Performance Dashboard
a. It is a data analytics project created using Microsoft Power BI to explore the factors associated with students' academic performance.
b. The dashboard is designed to help users explore academic outcomes, compare student groups, identify patterns in study and lifestyle behavior, and examine the relationships between different student characteristics and examination results.

2. Project Objectives -
a. Analyze overall student performance through key academic indicators and KPIs.
b. Examine the relationship between study methods, study consistency, revision habits, and examination scores.
c. Explore how sleep patterns, physical activity, stress, and motivation relate to academic outcomes.
d. Evaluate examination performance through scores, grades, pass status, and examination-related factors.
e. Enable student-level exploration through detailed academic, study, and lifestyle profiles.
f. Provide interactive filtering to compare students across different demographic and academic categories.

3. Tech Stack -
a. Microsoft Power BI	- Dashboard development, data modeling, interactive visualizations, and reporting.
b. Power Query - Data transformation, cleaning, and preparation.
c. DAX (Data Analysis Expressions) - Calculated measures, Calculated Columns. 
d. Kaggle - Source of the student performance dataset. Dataset Link: https://www.kaggle.com/datasets/mobeenfatimah/student-exam-performance-and-success-dataset
e. GitHub - Project documentation, version control, and project hosting.

4. Dataset Description -
a. The dataset was obtained from Kaggle and contains student-level academic, demographic, behavioral, lifestyle, and examination-related information. It consists of 44 columns.
b. Student Demographics - student_id, age, gender, education_level, school_type, family_income, parent_education, urban_rural.
c. Academic Attributes - previous_exam_score, previous_gpa, attendance_percentage, assignment_completion_rate, class_participation, private_tuition.
d. Study Habits - study_hours_per_day, self_study_hours, study_consistency, study_environment, study_method, revision_frequency, practice_tests_completed, notes_quality.
e. Lifestyle - sleep_hours, sleep_quality, daily_screen_time, physical_activity_hours, break_frequency, stress_level, motivation_level.
f. And many more important attributes.

5. DAX Measures Created -
a. Total Students - Counts the number of student records in the dataset. Total Students = COUNT(Student_Data[student_id])
b. Average Attendance - Calculates the average attendance percentage using the transformed attendance column. Average Attendance = AVERAGE(Student_Data[new_attendance_pct])
c. Average Assignment Completion - Calculates the average assignment completion rate and converts the percentage to a decimal for percentage formatting in Power BI. Avg Assignment Completion = AVERAGE(Student_Data[assignment_completion_rate]) / 100
d. Average Physical Activity - Calculates the average number of hours spent on physical activity. Avg Physical Activity = AVERAGE(Student_Data[physical_activity_hours])
e. Passing Rate - Calculates the proportion of students with a pass status among all student records in the current filter context. Passing Rate = VAR Pass_Count =
    CALCULATE(COUNTROWS(Student_Data), Student_Data[pass_status] = "pass" )
VAR Total_Stud = COUNT(Student_Data[student_id])
RETURN
    DIVIDE(Pass_Count, Total_Stud, 0)

6. Interactive Features -
a. Slicers to filter data by demographic, academic, study, and lifestyle characteristics.
b. Dynamic KPIs to recalculate aggregate measures according to the active filter context.
c. Student-level filtering to explore the academic, study, and lifestyle profiles of an individual student.

7. Future Enhancements -
a. Adding a dedicated student ranking and Top 50 performance view.
b. Introducing more detailed student comparison features.
c. Developing additional DAX measures for deeper academic analysis.
d. Improving visual tooltips to provide additional context without overcrowding charts.

8. Learning Outcomes -
a. Working with real-world tabular datasets.
b. Preparing and organizing data for business intelligence reporting.
c. Building interactive dashboards in Microsoft Power BI.
d. Creating DAX measures and understanding filter context.
e. Selecting suitable visualizations for different analytical questions.
f. Performing exploratory data analysis.
g. Designing multi-page analytical reports.

9. Snapshot - ![Dashboard Preview](https://github.com/AYUSHACK29/student_performance_pbi/blob/main/Student_Dashboard%20-%20Summary.png)
