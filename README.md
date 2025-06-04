# Hands-on Lab: Using Views in MySQL with phpMyAdmin

This lab guides you through creating, updating, and dropping Views in MySQL using the phpMyAdmin interface. It uses a sample HR database to demonstrate how Views work with multiple tables.

---

## Table of Contents

- [Overview](#overview)  
- [Objectives](#objectives)  
- [Software and Database](#software-and-database)  
- [Setup Instructions](#setup-instructions)  
- [Lab Tasks](#lab-tasks)  
  - [Task 1: Create a View](#task-1-create-a-view)  
  - [Task 2: Update a View](#task-2-update-a-view)  
  - [Task 3: Drop a View](#task-3-drop-a-view)  
- [Practice Problems](#practice-problems)  
- [Conclusion](#conclusion)  
- [Authors](#authors)

---

## Overview

A **View** in SQL is a virtual table based on the result-set of an SQL statement. Views provide a way to simplify complex queries and combine data from multiple tables without storing the data physically.

---

## Objectives

By completing this lab, you will be able to:

- Create a View to show selected data from a table  
- Update a View to combine data from multiple tables  
- Drop a View when no longer needed  

---

## Software and Database

- **Software:** MySQL (using phpMyAdmin interface)  
- **Database:** Sample HR database with tables: `EMPLOYEES`, `JOB_HISTORY`, `JOBS`, `DEPARTMENTS`, and `LOCATIONS`.  

---

## Setup Instructions

1. Open the MySQL interface from the IBM Skills Network menu.  
2. Create a new database called `HR`.  
3. Load and execute the provided SQL script `HR_Database_Create_Tables_Script.sql` to create tables.  
4. Load CSV files to populate tables:  
   - `Departments.csv`  
   - `Employees.csv`  
   - `Jobs.csv`  
   - `Locations.csv`  
   - `JobsHistory.csv`

---

## Lab Tasks

### Task 1: Create a View

Create a view named `EMPSALARY` to display employee salary and sensitive data:

```sql
CREATE VIEW EMPSALARY AS
SELECT EMP_ID, F_NAME, L_NAME, B_DATE, SEX, SALARY
FROM EMPLOYEES;
