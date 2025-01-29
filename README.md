# HR-ANALYSIS

**Project Overview**

This is a comprehensive Human Resource analysis carried out to help track, analyze, and interpret the organizational workforce data. It presents key metrics and trends in a visual and interactive format, allowing HR teams to make data-driven decisions about organization growth.

**Key Performance Indicators (KPIs)**

The analysis focuses on the following KPIs:

•	 Total Employee: Displays the total numbers of employees.

•	Total number of Male and Female Employee with their respective percentages. 


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



