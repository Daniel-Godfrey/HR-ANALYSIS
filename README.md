# HR-ANALYSIS

**Project Overview**

This project presents an interactive HR Analytics Dashboard built with Power BI, designed to provide key insights into workforce data such as employee demographics, job satisfaction, department composition, service years, and job levels. It allows HR professionals to make data-driven decisions by exploring employee-related metrics at a glance.

**Features**

**Employee Demographics**
Breakdown of employees by gender, marital status, and education field. 

**Service Years Overview**
Visual distribution of employees based on years of service (1 to 10+ years).

**Job Level Distribution**
Count of employees across various job levels from Level 1 to Level 5.

**On-Service vs. Lay-Off Status**
Department-wise comparison of active vs. laid-off employees.

**Employee Distance Status**
Categorization based on proximity to the workplace (Very Close, Close, Very Far).

**Job Satisfaction by Role**
Insight into satisfaction levels across roles like Research Scientist, Sales Executive, Managers, etc.

**Education Field Analysis**
View of employee distribution by educational background.


**DAX Analysis**

Below are some key DAX measures used in the dashboard:

**•	Total Employee**

Total Employee = COUNTROWS('HR Analytics Data')


**•	Employee by Gender:**

Male = CALCULATE( 'HR Analytics Data'[Total Employee], 'HR Analytics Data'[Gender] = "Male")


Female = CALCULATE( 'HR Analytics Data'[Total Employee], 'HR Analytics Data'[Gender] = "Female")


**•	Percentage of Employee by Gender:**

% Male = DIVIDE([Male], 'HR Analytics Data'[Total Employee], 0)


% Female = DIVIDE([Female], 'HR Analytics Data'[Total Employee], 0)


**•	Employee on Service/Lay-off:**

On Service = CALCULATE([Total Employee], 'HR Analytics Data'[Retrenchment] = "On Service")


Lay-Off = CALCULATE([Total Employee], 'HR Analytics Data'[Retrenchment] = "Lay off")


**•	Percentage of Employee on Service/Lay-off:**

% On Service = DIVIDE( 'HR Analytics Data'[On Service], 'HR Analytics Data'[Total Employee], 0)


% Lay-off = DIVIDE( 'HR Analytics Data'[Lay-Off], 'HR Analytics Data'[Total Employee], 0)



**Visualizations**

•	Employee Service Year: A clustered bar chart visualization showing the total number of Employees and their Service year.

•	Employee Educational Level: A stacked column chart visualization showing the total number of Employees by their Educational Level.

•	Employees on Service and Lay-Off by Department: A clustered column chart visualization showing the total number of Employees on Service and Lay-Off by Department.

•	Employee Job role: A clustered column chart visualization showing the total number of Employees by their Job role.

•	Employee Job Level: A clustered column chart visualization showing the total number of Employees by their Job level.

•	Employee Distance Status: A donut chart visualizing the total number of employee by their distance status to work.

•	Slicer to filter data by Department and Marital Status.


**Getting Started**

To explore or modify the dashboard:

  1.  Open Power BI Desktop.

  2.  Load the .pbix file.

  3.  If working with raw data:

      •  Import the dataset via CSV.

      •  Recreate visualizations using Power BI.

**Use Cases**
•  HR Decision Making
•  Workforce Planning
•  Employee Satisfaction Monitoring
•  Recruitment and Retention Analysis
•  Internal Reporting

**Preview**
See attached HR ANALYSIS DASHBOARD.pdf for a snapshot of the dashboard visuals.

**Feedback & Contributions**
Feel free to fork the repo, raise issues, or contribute improvements. Feedback and suggestions are welcome!

