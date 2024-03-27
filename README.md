# HR-dashboard

## Problem Statement

This presents the design and implementation of a Human Resources (HR) dashboard using Power BI, a powerful data visualization tool. The HR dashboard serves as a comprehensive solution for organizations to effectively monitor and analyze key HR metrics, aiding decision-making processes and enhancing workforce management strategies. The dashboard encompasses various aspects of HR, including employee demographics, recruitment, retention, performance, and engagement metrics. Leveraging Power BI's interactive features and dynamic visualizations, users can gain valuable insights into workforce trends, identify areas for improvement, and track progress towards organizational goals. By centralizing HR data and presenting it in an intuitive and visually appealing manner, the HR dashboard empowers stakeholders at all levels to make informed decisions, optimize resource allocation, and foster a more productive and engaged workforce. This project outlines the development process, key features, and potential benefits of the HR dashboard, highlighting its significance as a strategic tool for modern HR management.

# Steps followed

Get Data:

I got the appropriate data sources for the HR data, the data was rough, in which it is CSV file.
Connected the data sources and imported relevant HR data tables into Power BI.

Transform Data:

Used the Power Query Editor to clean and transform the imported data as needed. This may involve tasks such as removing duplicates, renaming columns, changing data types, and merging/joining tables.
Perform data modeling tasks such as creating relationships between tables, defining calculated columns, and creating measures (aggregations) using DAX (Data Analysis Expressions) language.
FOR EXAMPLE:
created coloumns using conditional column and column from examples, for analysing the needed data like cab availability, job levels, employyes working,going to get retired.

Some used DAX formula:

Due for promotion = CALCULATE([Total Emp],'HR Analytics Data'[Promotion Status]="due for promotion")
Will be Retired = IF(ISBLANK(CALCULATE([Total Emp],'HR Analytics Data'[Retirement status]="Will be Retired")),0,CALCULATE([Total Emp],'HR Analytics Data'[Retirement status]="Will be Retired"))
On service = IF(ISBLANK(CALCULATE([Total Emp],'HR Analytics Data'[Retirement status]="on service")),0,CALCULATE([Total Emp],'HR Analytics Data'[Retirement status]="on service"))
% Not due = DIVIDE([Not due],[Total Emp],0)

like this used many DAX formula and created new measures for analysing the data and creating the HR dashboard.


Design Visualizations:

Navigate to the report view in Power BI Desktop.
Design the visualizations for  HR dashboard by dragging and dropping fields from your data tables onto the canvas.
Chosed appropriate visualization types (e.g., bar charts, line charts, pie charts, tables) to represent different HR metrics effectively.
Customized the appearance of visualizations by adjusting colors, fonts, sizes, and other formatting options.
Added interactivity to the dashboard by creating slicers, filters, and drill-through actions to enable users to explore the data dynamically.

Create Dashboard:

after designing individual visualizations, organize them into a cohesive dashboard layout.
Switch to the "Dashboard" view in Power BI Desktop.
Add visualizations to the dashboard canvas by selecting them from the "Visualizations" pane and dragging them onto the canvas.
Arrange the visualizations spatially on the dashboard canvas to create a logical flow and ensure ease of understanding for users.
Add additional elements such as text boxes, images, and shapes to provide context and enhance the dashboard's visual appeal.

types of informations used in the dashboard :

Total Employees,
male,
female,
job level,
cab availability,
on service,
will retire soon,
service year,
due for promotion,
not due.

created new measures using dax formula and made the hr dashboard dynmaic and interactive to the user. They can find all the requirement needed in the dashboard and check anything and work on it for the business insights, recession,opening jobs, hikes to the employess.



