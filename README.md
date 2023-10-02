# Database Management Systems - ER Diagram Readme

## Name: Syed Muhammad Noor Ali Shah
## Registration Number: 2021-CE-36
## Course: Database Management Systems
## Submitted to: Sir Waseem
## Department of Computer Engineering
## University of Engineering & Technology, Lahore

This repository contains an Entity-Relationship (ER) Diagram for a database management system created as part of the course "Database Management Systems." The ER Diagram represents various entities and their relationships in a database system. Below, you will find details about the entities identified, relationships established, and constraints on the ER Diagram.

## Question 1 - Entities and Relationships

### Entities Identified:
1. **Campus** (Strong entity) - unique ID (key), name, address (composite), city, state, country, and URL.
2. **User** (Strong entity) - unique ID (key), first name, last name, email, phone (multivalued).
3. **College** - unique ID (key), name, phone, email, and URL.
4. **Course** - code (key), number, credit, and title.
5. **Student** - undergraduate or graduate?
6. **Faculty** - rank.
7. **Supervisor** - Office hours (derived).
8. **Tutor** - pay rate, list_of_courses.
9. **Non Academic Unit** - job description.

### Relationships:
1. Campus to College: 1:N (One campus can have multiple colleges).
2. Campus to Non-Academic Unit: 1:N (One campus can have multiple non-academic units).
3. College to Courses: 1:N (One college can offer multiple courses).
4. College to Tutor: N:(0,..N) (A college can have zero or more tutors).
5. Tutor to Courses: 1:(0,..N) (A tutor can teach zero or more courses).
6. Supervisor to Tutor: 1:(0,..N) (A supervisor can supervise zero or more tutors).
7. On-Call: 1:(0,..N) (Represents an on-call relationship, details not provided).
8. Appointment (tutor-student): 1:(0,..N) (Represents appointments between tutors and students, details not provided).
   
![img1](https://github.com/SyedNoorAliDev/DatabasesAssignment02/assets/96229280/bbb07ca7-8afe-4af4-81d4-3ded06c3c9c1)

## Question 2 - ER Diagram Screenshot

![img2](https://github.com/SyedNoorAliDev/DatabasesAssignment02/assets/96229280/0e5ec9e3-2900-4a2f-99a2-7647e5e8a7d4)

## Question 3 - ER Diagram Screenshot and Constraints
### a) Supply (min, max) constraints on the given diagram:

![img3](https://github.com/SyedNoorAliDev/DatabasesAssignment02/assets/96229280/b33e3a42-6334-4d46-a05c-55c10b8455bb)


### b) Under what conditions would the relationship "HAS PHONE" be redundant in this example?
The relationship "HAS PHONE" would become redundant if we can directly associate phones with employees through the "WORKS IN" relationship. If we remove the "HAS PHONE" relationship and still maintain the ability to determine which phones belong to which employees through their department assignments (i.e., "WORKS IN" relationship), then the "HAS PHONE" relationship is redundant. 

So, under normal conditions, the "HAS PHONE" relationship is not redundant, as it explicitly associates phones with employees, ensuring that each employee can have their assigned phones, which may not necessarily be the same as the department's phones.
