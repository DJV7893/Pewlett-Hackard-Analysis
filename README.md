# Pewlett-Hackard-Analysis
---
## Overview
---
### Purpose:

  The Human Resources Department of Pewlett Hackard (PH) tasked us with creating an employee database with SQL from several CSV files to prepare to fill substantial vacancies created by retiring baby boomers and offer retirement packages to those who qualify. After submitting our retirement lists to management to begin their future-proofing preparation, we have been tasked with providing additional lists in order to support the creation of a mentorship program.  Retiring employees who are identified as experienced and successful will be offered the option of stepping back part-time and mentor newly hired folks. The lists we will create will determine the number of retiring employees per title and identify employees who are eligible to participate in the mentorship program.

---
## Analysis
---
### Results:

Our new SQL Queries returned the following results into four separate tables:

  1. Table of Retiring Employees:

  * Includes: Employee Number, First Name, Last Name, Title, From-Date and To-Date for employees born between 1952 and 1955.
  * The query returns 133,776 rows of data.
  * The table displays a list of employees who will retire in the next few years, comprising the silver tsunami wave described by PH.
  * This is an initial list that will be further analyzed because we have repeats of certain employee as a result of them changing positions in their time     at PH.

<img width="735" alt="Retirement_Titles" src="https://user-images.githubusercontent.com/99817571/162268474-3bd43fc5-2628-47a6-8895-7254865f9f20.png">

  2. Table of Unique Titles:
  
  * Our new list of retiring employees that removed the duplicates from our Retiring Employees list by only including the most recent title for each           employee.
  * Includes: Employee Number, First Name, Last Name, Title, From-Date and To-Date.
  * The query returns 72,458 records of employees.
  * This table is more capable of being analyzed as it lists the most recent titles that potential retiree hold.
  * From this revised table we can further analyze how to handle the silver tsunami.
 
 <img width="552" alt="Unique_Titles" src="https://user-images.githubusercontent.com/99817571/162268912-3a2188ab-fbc4-4023-96a9-b38afa61dd9d.png">

  3. Table of Retiring Titles:
  
  * With our list of unique titles we can summarize the thousands of rows by grouping employees by their title and counting how many of them there are in       each corresponding sub-field.
  * This table includes Retirement Employees’ Titles and their Count.
  * The query returns 7 rows each corresponding to the unique retirement titles: Senior Engineer, Senior Staff, Engineer, Staff, Technique Leader,             Assistant Engineer, and Manager.
  * From this table we can quickly see the impacts retiring employees may have on the organization based on current title, especially those in senior           positions.
  
  <img width="242" alt="Retiring_Titles" src="https://user-images.githubusercontent.com/99817571/162269312-4a398b40-6da7-4d05-b947-a0290693017b.png">

  4. Table of Mentorship Eligibility:
  
  * Our final list further analyzes our Retirement List by selecting those who might be eligible for a mentorship program by
    gathering employees who are eligible for a mentorship program based on the condition that their birth date is in the year of 1965.
  * The query returns 1549 records of employees.
  * Includes Employee Number, First Name, Last Name, Title, Birth Date, From-Date and To-Date.
  * The table provides a clear list to management of those who can help lessen the impact of the silver tsunami by offering their services during the           transition period in the mentorship program.

<img width="740" alt="Mentorship_Eligibility" src="https://user-images.githubusercontent.com/99817571/162269771-1060d45a-c211-46d1-ac49-a0a3d333e3a8.png">

---
## Summary
---
### Recommendations

  Our new queries indicate that the silver tsunami will have a significant impact on PH in the upcoming years. The total amount of positions that will have to be filled in the seven different position types: senior engineer, senior staff, engineer, staff, technique leader, assistant engineer, and manager will be 72,458. Furthermore, the biggest blow will be dealt to senior level positions in PH as future vacancies in Senior Engineer and Staff comprise of 70 percent of retirements (50,842/72,458). The staggering number of vacancies will overwhelm the mentorship program as currently constructed because there are only 1,549 retirement ready employees who can qualify for the program. That would mean that 1,549 individuals would have to handle the transition period and mentorship of several hires at once, turning it into more than a part-time position. Accordingly, we need to further assess how to improve the mentorship program in order to handle the onslaught of retirees in the upcoming years by conducting new queries.

  One query we could create would be a table that would show retirement eligible employees by most recent department and title in order to understand which departments are hit hardest. The query would display a table similar to our Unique Titles table that would include another column with the employee’s department. From that table we could run another query that would count the number of retiring employees per department. From this information PH can refocus its mentorship program strategy.

   A second query we can conduct is to accept our mentorship eligibility is limited and expand the years eligible for the mentorship program by adding a successive year. We can run a similar query as in our final Mentorship Eligibility table and add inside of our Where clause we will expand the limits from just 1965 to include all the way to the end of 1966. From there once we count the total employees eligible, we can assess if that will help to lessen the impact of the silver tsunami and whether we should expand further the criteria.

---
## Resources
---
Data Source: retirement_titles.csv, unique_titles.csv, retiring_titles.csv, mentorship_eligibility.csv

Software: PostgreSQl 11.15, PgAdmin 6.7
