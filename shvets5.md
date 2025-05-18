```mermaid
---
title: Діаграма компонентів — Розклад занять
---

graph TD

%% Клієнтський інтерфейс
GUI[Користувацький інтерфейс (Tkinter GUI)] --> AdminPanel[Admin Panel]

%% Бізнес логіка
AdminPanel --> StudentCtrl[Student Controller]
AdminPanel --> TeacherCtrl[Teacher Controller]
AdminPanel --> ScheduleCtrl[Schedule Controller]

%% Контролери -> сервіси
StudentCtrl --> UserService[User Service]
TeacherCtrl --> UserService
ScheduleCtrl --> ScheduleService[Schedule Service]

%% Сервіси -> репозиторії
UserService --> UserRepo[User Repository]
ScheduleService --> ScheduleRepo[Schedule Repository]

%% Репозиторії -> таблиці бази даних
UserRepo --> UsersTable[users]
UserRepo --> TeachersTable[teachers]
UserRepo --> GroupsTable[student_groups]

ScheduleRepo --> ScheduleTable[schedule]
ScheduleRepo --> SubjectsTable[subjects]
ScheduleRepo --> GradesTable[grades]
```