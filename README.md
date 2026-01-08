# CC105_DB_AguilaJohnAndrew
1. System Overview and Purpose

The Feedback System is designed to collect, store, and analyze student feedback for academic subjects.
It allows institutions to record feedback data such as academic year, semester, branch, section, subject, quantitative question ratings, and qualitative remarks.

Purpose:

Collect structured feedback from students

Store responses in a centralized MySQL database

Enable analysis of teaching quality and subject effectiveness

Support academic decision-making and reporting

2. Database Structure
Database Name

feedback_system

Main Table

feedback

3. Table Description:
4.  feedback
Column Name	Description
id	Primary key, unique identifier for each feedback entry
year	Academic year (e.g., 2025)
sem	Semester (e.g., 1st, 2nd)
date	Date when feedback was submitted
branch	Department or branch (e.g., Morning, Afternoon)
section	Section or class group
subject	Subject code (e.g., DC103, DC104)
ques1	Rating for Question 1
ques2i	Rating for Question 2 (Part i)
ques2ii	Rating for Question 2 (Part ii)
ques2iii	Rating for Question 2 (Part iii)
ques2iv	Rating for Question 2 (Part iv)
ques2v	Rating for Question 2 (Part v)
ques3	Rating for Question 3
ques4	Rating for Question 4
remarks	Textual feedback or comments

Ratings are typically numeric (e.g., 1–5), while remarks store qualitative feedback such as “very good”, “good”, or “not bad”.

4. Table Relationships

Currently, the feedback table is standalone

No foreign key relationships are defined

Future enhancements may include:

students table (linked via student_id)

subjects table (linked via subject_code)

faculty table (linked via faculty_id)

5. Sample Query
SELECT * 
FROM feedback_system.feedback;

6. Sample Output (Query Result)

The query returns multiple feedback records, including:

Academic year: 2025

Semester: 1st / 2nd

Subjects: DC101, DC103, DC104, CC105

Ratings ranging from 0 to 5

Remarks such as:

very good

good

not bad

A total of 5 rows were returned in the displayed result.

7. Screenshot of Query Result
