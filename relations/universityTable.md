# DB Schema

Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università.

## departments

- id BIGINT PK AI 
- name VARCHAR(100) NOT NULL UNIQUE
- description TEXT NOT NULL

## degree_course

- id BIGINT PK AI
- name VARCHAR(100) NOT NULL
- duration_year YEAR NOT NULL DEFAULT 3

## courses

- id BIGINT PK AI
- name VARCHAR(100) NOT NULL
- year_of_study YEAR NOT NULL

## teacher

- id BIGINT PK AI
- first_name VARCHAR(100) NOT NULL
- second_name VARCHAR(100) NOT NULL
- email VARCHAR(200) NOT NULL UNIQUE
- phone CHAR(10) NOT NULL UNIQUE

## exam session

- id BIGINT PK AI
- date DATE NOT NULL
- time TIME NOT NULL
- room VARCHAR(100) NOT NULL

## student

- id BIGINT PK AI
- first_name VARCHAR(100) NOT NULL
- second_name VARCHAR(100) NOT NULL
- email VARCHAR(200) NOT NULL UNIQUE
- phone CHAR(10) NOT NULL UNIQUE
