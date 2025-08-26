# Ejercicio---Normalizacion de Bases de Datos

## Tablas normalizadas

https://docs.google.com/spreadsheets/d/1uOAgw3A31Yyi5_l0Danste3LpwQ693TetADzrp6VTV0/edit?gid=0#gid=0

## Diagrama de Chen (No chabe)

<img width="589" height="381" alt="courses drawio" src="https://github.com/user-attachments/assets/f5b36a1e-ffa4-406d-a7e0-da4c0dae5a45" />

## Diagrama de patas de gallo

```mermaid
erDiagram
    students {
        int id_student PK
        string name_student
    }

    courses {
        int id_course PK
        string course_name
    }

    classrooms {
        int id_classroom PK
        string classroom_code
        string classroom_description
    }

    student_classroom {
        int id_student FK
        int id_classroom FK
    }

    classroom_course {
        int id_classroom FK
        int id_course FK
    }

    students ||--o{ student_classroom : "asiste"
    classrooms ||--o{ student_classroom : "contiene"
    classrooms ||--o{ classroom_course : "ofrece"
    courses ||--o{ classroom_course : "incluye"
```
