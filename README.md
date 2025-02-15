# HR-Analytics
I was tasked with utilizing employee data and performance survey results to support the decision-making process of the HR director and the Senior Management Team of Dover Insurance. 

## Introduction
The company has been experiencing issues with their employees ranging from high absence to concerning turnover rates, as with customer turnover and complaints. The new HR Director came up with new initiatives such as introducing a wellness app, and conducting a survey to determine employee satisfaction, and engagement at the company. 

I was provided with two datasets which include;
- Dashboard data, and;
- Regression data

## Overview of tasks
For this report, I will be focusing on the 'Dashboard Data' sheet

**Dashboard data:** 
- Develop a dashboard for the stakeholders to show how Dover Insurance is performing against key metrics
- Identify key findings in areas like inclusivity, availability of employees, patterns in viewing non-work content during working hours, usage of the wellness app, and employee satisfaction

**Tools used:**
Microsoft Power BI 

## Step 1: Data Preparation
- I downloaded 'Dashboard Data' as an .xlsx file and imported it into Power BI using the get data feature
- I checked for data quality by verifying each data type and correcting where necessary, and checking for missing values and outliers-- of which there were none. 

## Step 2: Build charts using identified key metrics + analysis
Having identified my key metrics previously, I started by building each relevant chart accordingly for my dashboard; 

- Distribution by gender <br>
The donut chart below highlights the gender distribution of employees at Dover Insurance, showcasing a near-equal representation with 56% male and 44% female employees. 

![image](https://github.com/user-attachments/assets/8204dcfc-c4eb-4cbe-8e63-75cdcbb45200)

- Distribution by Ethnicity <br>
The bar chart below reveals the employee distribution to have a significant majority (779) identifying as White. The underrepresentation of other ethnic groups highlights potential areas for improving diversity and fostering a more inclusive workplace.

![image](https://github.com/user-attachments/assets/12be2a19-796c-4355-b219-991b7a2fbde5)

- Employee distribution by Age Group<br>
This bar chart illustrates the employee distribution with the 18–29 age group making up the largest portion of the workforce. It highlights a younger workforce, providing opportunities to focus on career growth and retention strategies for this demographic.

![image](https://github.com/user-attachments/assets/84c731b3-b2f0-4bf4-a631-807dbb691eca)

- Absence days by division & position<br>
This cluster chart displays the average absence days by position and division, revealing a significant spike in absenteeism from senior management within the Commercial division. Such disparities suggest potential underlying issues that may need targeted interventions to improve attendance.

![image](https://github.com/user-attachments/assets/dbbdd7ea-7a7a-43a2-a4ed-66a59e5f316d)

- Percentage of hours spent viewing non-work content by age group <br>
The bar chart below highlights younger employees (18-29) leading at 11.3%, followed by a steady decline in usage across older age groups. This trend may suggest generational differences in online behavior or varying work habits across age groups.

![image](https://github.com/user-attachments/assets/fa837cc3-6539-4934-9618-f0096c5420e5)

- Average amount of hours spent on the wellness app<br>
The bar chart shows that employees aged 30-39 use the wellness app the most, followed closely by the 18-29 age group. Interestingly, engagement drops significantly in older age groups, highlighting a potential area to improve wellness app adoption among them.

![image](https://github.com/user-attachments/assets/41a10c60-71f8-4f80-94db-c97b776618bb)

- Employee satisfactions levels vs. Target <br>
To visualize this, I had to create a new table using the DAX formula below:
```
TargetScores = 
DATATABLE(
    "Metric Name", STRING,
    "Target Value", INTEGER,
    {
        {"Employees have a 'voice' in this Organisation", 7},
        {"My pay and benefits are fair for the work I do", 7},
        {"Everybody has an equal opportunity to progress in this organisation", 7},
        {"My work is stressful and pressurised", 3},
        {"My line manager cares about me as a person", 7},
        {"The purpose of the organisation makes my job feel important", 7}
    }
)
```
As seen above, I set the target score for each survey question at 7, except for 'My work is stressful and pressurized' which I set at 3. Next, I created a new table using DAX to point out the average score for each metric, and then I created a relationship between the Metric columns in both newly created tables. 

This bullet chart below highlights employee satisfaction levels across key areas compared to target benchmarks. While 'The purpose of the organization makes my job feel important' scores highest at 6.6, there's room for improvement in areas like concerning 'pay and benefits' and 'manager's interaction with employees'. Results for 'my work is stressful and pressurized' suggests higher stress levels than expected. 

![image](https://github.com/user-attachments/assets/5f5490fc-9fa2-4d59-8c2c-73489a24535c)

 ## [INTERACT WITH DASHBOARD](https://4h8nvq-my.sharepoint.com/:u:/g/personal/timi_4h8nvq_onmicrosoft_com/ETCpnRV_yy5PmdSjRTQbQwEBuVQgL7v_bSN8_IqxA04pgw?e=Y1sUfA)
![image](https://github.com/user-attachments/assets/730eb8f5-cfc4-420d-b25e-2e5ecc1035ee)

## Step 4: Actionable Insights
Based on the visuals above, here are some insights I was able to gather across relevant areas; 

- Inclusivity & career development:
Implement programs for underrepresented ethnicities, and ensure equal access to leadership positions and promotion

- Address absence issues:
Provide targeted support for high-absence divisions (e.g., stress management training), and review company policies for sick leave and flexible working conditions.

- Wellness app usage:
Fair usage across board, however features can be expanded as employees give feedback, and employees in the 55+ age group can be trained on how to use the app.

- Employee satisfaction
The visualization shows room for improvement or review for pay and incentives, and manager-employee relationship. High stress levels may also suggest a need for workload management, and support systems, especially across departments with high absence. 

## Conclusion 
The findings from this dashboard provide insights for the HR Director and Senior Management Team (SMT) to optimize workforce engagement, reduce absence rates, and enhance overall employee wellbeing. Implementing the recommended actions will improve productivity, inclusivity, and workplace satisfaction. 

___
Connect with me on [LinkedIn](https://www.linkedin.com/in/hellotimilehin/) or via [E-mail](hellotimilehin@gmail.com)











