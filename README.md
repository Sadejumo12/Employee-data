# Employee-Information Dataset
This data analysis project aims to provide insights into Employee information. By analyzing various aspects of Employee information, we seek to identify departmental trends, and gain a deeper understanding of the company's Employee details,no of employees in a department and Average Salaries.


## Data Sources
Employee Data: The primary dataset used for this analysis was created by me containing detailed information of employee in a company.

## Tools
SQL Postgres - Data Analysis

## Data Cleaning/Preparation
In the initial data preparation phase, we performed the following tasks:

1.Creation Of table.
2.Inserting information /values into the table.
3.Data cleaning and formatting.

## Exploratory Data Analysis
EDA involved exploring the Employee data to answer key questions, such as:

Employees Full Details?
Average salaries of employee?
Average salaries of employee with job id =6?
Top 3 department with high number of employee and average salary?
Department that has employee greater than 5?

## Data Analysis
Include some interesting syntax /features worked with

1. ### Employees Full Details?
select * from employees
![employee full detail](https://github.com/Sadejumo12/Employee-data/assets/113441381/e7df3b63-701e-459e-b069-5ef15d9f22fc)


2. ### Average salaries of employee?
select avg(salary) from employees

![select average](https://github.com/Sadejumo12/Employee-data/assets/113441381/4112bbfc-14eb-42c3-8845-7deaaf8524e7)


3. ### Average salaries of employee with job id =6
select avg(salary) from employees
where job_id =6

![select aveargw salary where employee job di =6](https://github.com/Sadejumo12/Employee-data/assets/113441381/d3584e25-3ad0-449d-866a-bc13d7878e05)

4. ### Top 3 department with high number of employee and average salary?
select D.department_name,department_id,Round(AVG(salary),2),count(employee_id)FROM employees E 
inner join departments D using (department_id)
group by E.department_id,department_name
order by AVG(salary) desc
limit 3
![Top 3 department with highest number of employees](https://github.com/Sadejumo12/Employee-data/assets/113441381/8a7f54e0-f092-40c1-b5dc-de650774b57b)

5. ### Department that has employee greater than 5?
select count(employee_id),D.department_name from employees E
inner join departments D using (department_id)
group by department_name
having count(employee_id)>5
order by count(employee_id) desc
![number of employee by department whose employee is greater than 5](https://github.com/Sadejumo12/Employee-data/assets/113441381/47f5109e-c3c9-4a8a-b5e0-aaa86d14eca1)



References

Career.insight

