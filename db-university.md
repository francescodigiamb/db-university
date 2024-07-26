# University 

table: departments
- id BIGINT PK AUTO NOTNULL UNIQUE
- name VARCHAR (30) NOTNULL
- year YEAR NOTNULL
- address VARCHAR (50) NULL
- phone_number SMALLINT NOTNULL
- mail_address VARCHAR (30) NOTNULL
- info TEXT NULL
- degree_courses_id FK NOTNULL

table: degree_courses
- id BIGINT PK AUTO NOTNULL UNIQUE
- name VARCHAR (30) NOTNULL
- type VARCHAR (30) NOTNULL
- years_study TINYINT NOTNULL
- exams TINYINT NOTNULL
- info TEXT NULL
- courses_id FK NOTNULL
- students_id FK NOTNULL

table: courses
- id BIGINT PK AUTO NOTNULL UNIQUE
- name VARCHAR (30) NOTNULL     
- matter VARCHAR (20) NOTNULL 
- place_avaiable TINYINT NOTNULL
- academic_year TINYINT NOTNULL
- frequency VARCHAR (5) NOTNULL
- info TEXT NULL

table: students
- id BIGINT PK AUTO NOTNULL UNIQUE
- name VARCHAR (30) NOTNULL 
- surname VARCHAR (30) NOTNULL 
- email VARCHAR (10) NOTNULL
- age DATE NOTNULL
- qualification VARCHAR (20) NULL
- valutation VARCHAR (10) NULL

table: teachers
- id BIGINT PK AUTO NOTNULL UNIQUE
- name VARCHAR (30) NOTNULL
- surname VARCHAR (30) NOTNULL
- email VARCHAR (10) NOTNULL
- matter VARCHAR (10) NOTNULL
- courses_id FK NOTNULL

table: exams
- id BIGINT PK AUTO NOTNULL UNIQUE
- name VARCHAR (30) NOTNULL
- type VARCHAR (10) NOTNULL
- registration ?
- appeal DATE NOTNULL
- courses_id FK NOTNULL