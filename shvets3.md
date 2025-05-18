```mermaid
plantuml	
@startuml

package "Клієнтський інтерфейс (GUI)" {
  [Tkinter GUI] --> [Admin Panel]
}

package "Бізнес логіка" {
  [Admin Panel] --> [Student Controller]
  [Admin Panel] --> [Teacher Controller]
  [Admin Panel] --> [Schedule Controller]
}

package "Контролери" {
  [Student Controller] --> [User Service]
  [Teacher Controller] --> [User Service]
  [Schedule Controller] --> [Schedule Service]
}

package "Сервіси" {
  [User Service] --> [User Repository]
  [Schedule Service] --> [Schedule Repository]
}

package "База даних" {
  [User Repository] --> [users]
  [User Repository] --> [teachers]
  [User Repository] --> [student_groups]
  [Schedule Repository] --> [schedule]
  [Schedule Repository] --> [subjects]
  [Schedule Repository] --> [grades]
}

@enduml
```