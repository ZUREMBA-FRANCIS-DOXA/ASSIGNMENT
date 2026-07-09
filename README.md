# ASSIGNMENT
UMaT DATA COLLECTION
# UMaT Management System

A simple Python program demonstrating **object-oriented inheritance** by modeling different types of people on a university campus — `Student` and `Lecturer` — both derived from a common `Person` class.

## 📌 Overview

UMaT needs a basic system to manage people on campus. All people share common attributes (name, age), but each role has additional responsibilities:

- A **Student** has a `student_id` and can enroll in a course.
- A **Lecturer** has an `employee_id` and can teach a course.

This project demonstrates how inheritance can be used to avoid code duplication while still allowing each role to have its own unique behavior.

## 🗂️ Class Structure

### `Person` (Parent Class)
| Member | Type | Description |
|---|---|---|
| `name` | attribute | Person's name |
| `age` | attribute | Person's age |
| `display_info()` | method | Prints the person's name and age |

### `Student` (Child Class)
Inherits from `Person`.

| Member | Type | Description |
|---|---|---|
| `student_id` | attribute | Unique student identifier |
| `enroll_course(course_name)` | method | Enrolls the student in a course |
| `display_info()` | method | **Overridden** — calls `Person.display_info()` via `super()`, then adds the student ID |

### `Lecturer` (Child Class)
Inherits from `Person`.

| Member | Type | Description |
|---|---|---|
| `employee_id` | attribute | Unique employee identifier |
| `teach_course(course_name)` | method | Assigns the lecturer to teach a course |

*(Lecturer uses the inherited `display_info()` from `Person` without modification.)*

## 🧩 Key OOP Concepts Demonstrated

- **Inheritance** — `Student` and `Lecturer` both inherit from `Person`.
- **`super()`** — used in both child classes to initialize inherited attributes (`name`, `age`) from the parent constructor.
- **Method Overriding** — `Student.display_info()` overrides the parent method but still reuses it via `super().display_info()`, then extends it with additional information.
- **Polymorphism** — each object calls `display_info()`, but the output differs depending on the object's class.

## ▶️ How to Run

1. Make sure you have Python 3 installed.
2. Save the code as `umat_management_system.py`.
3. Run it from the terminal:

```bash
python umat_management_system.py
```

## 🖥️ Sample Output

```
---- Student Info ----
Name: ZUREMBA FRANCIS DOXA, Age: 20
Student ID: FOE.21.006.038.24
ZUREMBA FRANCIS DOXA (ID: FOE.21.006.038.24) has enrolled in OBJECT ORIENTED PROGRAMMING.

---- Lecturer Info ----
Name: PROF. BERNARD KUMI BOATENG, Age: 45
Dr. Kwame Boateng (Employee ID: UMaT/EMP/0123) is teaching Geological Engineering.
```

## 🚀 Possible Extensions

- Add a `Staff` class for administrative roles.
- Maintain a master list of all `Person` objects on campus.
- Add input validation (e.g., age must be positive).
- Store and retrieve records from a file or database.

## 📄 License

This project is for educational purposes as part of a UMaT case study activity on inheritance in object-oriented programming.
