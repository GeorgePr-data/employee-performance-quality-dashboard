##Employee Performance & Quality Monitoring Dashboard (Power BI)

##Overview

This Power BI dashboard evaluates employee performance across supervisors, focusing on workload, quality outcomes, and operational efficiency.
The objective is to provide a structured performance monitoring view that enables management to identify high-performing teams, detect quality risks, and assess clean output volume.


##Business Objective

The report answers the following questions:
Which supervisors lead the most efficient teams?
How does defect rate vary across employees and supervisors?
What is the volume of successful (clean) samples delivered?
Are there quality trends over time that require intervention?


##Data Model

The model follows a star-like structure:

##Fact Table:

Quality Data
Date
EmpID
AuditorID
Total Tasks
Samples
Defects
Fatal Errors
Dimension Tables:
Emp Master
EmpID
Employee Name
Supervisor
Work Location
Auditors
AuditorID
Auditor Name

Grain:
One record per Employee per Auditor per Date.


##Core KPIs

Workload Metrics
Total Tasks = SUM([Total Tasks])
Total Samples = SUM([Samples])
Sampling Rate % = Samples / Total Tasks

Quality Metrics
Defect % = Defects / Samples
Fatal Error % = Fatal Errors / Samples
Quality Score % = 1 − Defect %


##Extended KPI (Custom Metric)

Successful Samples
Successful Samples = Samples − Defects
This metric highlights clean output volume rather than only percentages, providing a clearer view of usable production performance per supervisor and employee.


##Key Features

Supervisor-level filtering and comparison
Hierarchical Employee → Supervisor performance view
Interactive cross-filtering between visuals
Monthly defect trend monitoring
Combined volume and quality analysis


##Tools Used

Power BI Desktop
DAX (SUM, DIVIDE, calculated measures)
Data modeling & relational structure design


##Impact
This dashboard demonstrates structured KPI design, hierarchical performance analysis, and quality monitoring logic suitable for operational and managerial decision-making environments.

## Author
George Proikas
