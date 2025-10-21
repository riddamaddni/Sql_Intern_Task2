SQL Developer Internship - Task 2: Advanced DML and Data Integrity

🎯 Objective

This project serves as a comprehensive demonstration of the core competencies required for a SQL Developer role. The primary goal is to showcase mastery over Data Manipulation Language (DML) commands (INSERT, UPDATE, DELETE) within a realistic, imperfect database environment. This involves not just executing commands, but strategically handling common data issues like NULL values and ensuring absolute data integrity through the precise use of WHERE clauses and a deep understanding of database constraints. The successful completion of these tasks is fundamental to maintaining the accuracy, reliability, and performance of any data-driven application, directly impacting business intelligence and operational efficiency.

Workflow and Logic

This solution was developed through a structured, multi-step process designed to address all aspects of the task thoroughly:

Schema Analysis: The first step was a careful review of the provided database schema. Understanding the relationships between tables, especially the FOREIGN KEY constraints, was crucial for planning safe DELETE operations and ensuring data integrity.

Realistic Data Population: A key decision was to modify the initial dataset to include NULL values. A real-world database is rarely complete, so introducing missing data (like a reporter's phone number or a patient's weight) made the subsequent DML exercises more practical and challenging.

Proactive Error Handling: Anticipating the common Error 1175: Safe Update Mode was a critical part of the workflow. The script was designed to proactively manage this client-side safety feature by temporarily disabling it, allowing the necessary bulk updates to run without manual intervention. This demonstrates foresight and an understanding of the development environment.

Crafting DML Scenarios: A variety of DML commands were written to showcase different skills:

INSERT: Both single-row and multi-row insertions were used to show efficiency.

UPDATE: Scenarios included single-row updates (by primary key), multi-row updates (based on broad conditions), and updating multiple columns simultaneously.

DELETE: Both "safe" deletions (on data with no dependencies) and a commented-out "unsafe" deletion were included to explain and demonstrate an understanding of referential integrity.

🗂️ Files in this Repository

task_2_complete_solution.sql: This is the complete, self-contained, and runnable SQL script. It is professionally structured to handle session configuration (disabling Safe Mode), perform schema creation (CREATE TABLE), populate the database with a realistic, "messy" dataset (INSERT), and then execute all the required DML practice commands in a single, seamless flow. Every block of code is commented to explain its logic and purpose.

README.md: This detailed guide, which you are currently reading. It serves as the project's main documentation, explaining its purpose, the development workflow, the key concepts demonstrated, and providing clear, in-depth answers to all task-related questions.

🚀 How to Run the Script

Prepare Your Environment: Open any standard MySQL-compatible database environment. This could be a local client like MySQL Workbench or a cloud-based tool like DB Fiddle, which allows for the execution of full SQL scripts.

Execute the Script: Copy the entire contents of the task_2_complete_solution.sql file. Paste this into your chosen tool's query editor and execute it. The script is designed to run from top to bottom without requiring any manual modifications or separate steps.

Automatic "Safe Mode" Handling: A key feature of this script is its built-in handling of a common client-side safety feature. It begins by temporarily disabling "Safe Update Mode" (SET SQL_SAFE_UPDATES = 0;), which would otherwise block broad UPDATE or DELETE commands and cause an Error 1175. This proactive step ensures the script runs smoothly and demonstrates an understanding of real-world development environments.

✅ Core Competencies Demonstrated

DML (INSERT, UPDATE, DELETE): Demonstrating fluent control over the fundamental commands for adding, modifying, and removing data. These operations are the cornerstone of daily database management and application interaction.

Null Handling (IS NULL / IS NOT NULL): Correctly managing records where data is missing is a critical skill. This project shows how to filter for, update, and handle NULL values without causing errors or data inconsistencies.

Conditional Logic (WHERE): Moving beyond simple queries to precisely target specific rows for manipulation. This involves using a variety of logical operators (=, AND, IN, LIKE) to ensure that DML operations are surgical and only affect the intended data.

Data Integrity and Constraints: Showing a deep respect for database rules like DEFAULT, NOT NULL, and FOREIGN KEY. This ensures the database remains healthy, consistent, and reliable, preventing data corruption and orphaned records.
