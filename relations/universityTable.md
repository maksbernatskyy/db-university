# DB Schema

Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università.

## department

- department_id BIGINT PK AI 
- name VARCHAR(100) NOT NULL UNIQUE
- description TEXT NOT NULL

## degree_course

- degree_course_id BIGINT PK AI
- department_id BIGINT FK AI
- name VARCHAR(100) NOT NULL
- duration_year YEAR NOT NULL DEFAULT 3

## course

- course_id BIGINT PK AI
- degree_course_id BIGINT FK AI
- name VARCHAR(100) NOT NULL
- year_of_study YEAR NOT NULL

## course_teacher

- course_id BIGINT PK AI
- teacher_id BIGINT PK AI

## teacher

- teacher_id BIGINT PK AI
- first_name VARCHAR(100) NOT NULL
- second_name VARCHAR(100) NOT NULL
- email VARCHAR(200) NOT NULL UNIQUE
- phone CHAR(10) NOT NULL UNIQUE

## exam session

- exam_session_id BIGINT PK AI
- course_id BIGINT FK AI
- date DATE NOT NULL
- time TIME NOT NULL
- room VARCHAR(100) NOT NULL

## exam_session_student

- exam_session_id BIGINT PK AI
- student_id BIGINT PK AI

## student

- student_id BIGINT PK AI
- degree_course_id BIGINT FK AI
- first_name VARCHAR(100) NOT NULL
- second_name VARCHAR(100) NOT NULL
- email VARCHAR(200) NOT NULL UNIQUE
- phone CHAR(10) NOT NULL UNIQUE
