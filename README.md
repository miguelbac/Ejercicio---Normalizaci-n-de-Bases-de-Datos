# Ejercicio---Normalizacion de Bases de Datos

## Tablas normalizadas

https://docs.google.com/spreadsheets/d/1uOAgw3A31Yyi5_l0Danste3LpwQ693TetADzrp6VTV0/edit?gid=0#gid=0

## Diagrama de Chen

<img width="556" height="332" alt="Captura" src="https://github.com/user-attachments/assets/4b675e2b-8109-421e-9d1f-6e1735befa65" />

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
        int id_student PK, FK
        int id_classroom PK, FK
    }

    classroom_course {
        int id_classroom PK, FK
        int id_course PK, FK
    }

    students ||--o{ student_classroom : "asiste"
    classrooms ||--o{ student_classroom : "contiene"
    classrooms ||--o{ classroom_course : "ofrece"
    courses ||--o{ classroom_course : "incluye"

```
