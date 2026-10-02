# Corporate Travel Expenses

Модуль учёта и управления корпоративными командировочными расходами.

## Концепция системы

Система автоматизирует учёт командировочных расходов сотрудников: создание заявок на командировку, 
прикрепление чеков, маршрут согласования (сотрудник → руководитель → бухгалтерия), 
контроль лимитов по категориям и формирование отчётов. 
Целевая аудитория — бухгалтерия, HR и руководители подразделений.

## Технологический стек

| Компонент | Технология |
|-----------|------------|
| Язык | Java 17 (LTS) |
| Фреймворк | Spring Boot 3.2 |
| Веб | Spring MVC + Thymeleaf |
| Безопасность | Spring Security + JWT |
| ORM | Spring Data JPA / Hibernate |
| СУБД | PostgreSQL 16 |
| Миграции | Flyway |
| Сборка | Maven |
| Тесты | JUnit 5 + Mockito + Testcontainers |
| Документация API | SpringDoc OpenAPI (Swagger UI) |

## Структура папок проекта
corporate-travel-expenses/
├── src/
│ ├── main/
│ │ ├── java/com/example/travelexpenses/
│ │ │ ├── config/ # Конфигурация Spring
│ │ │ ├── controller/ # REST-контроллеры
│ │ │ ├── service/ # Бизнес-логика
│ │ │ ├── repository/ # Spring Data JPA
│ │ │ ├── entity/ # JPA-сущности
│ │ │ ├── dto/ # DTO
│ │ │ ├── mapper/ # MapStruct-мапперы
│ │ │ ├── security/ # JWT, аутентификация
│ │ │ ├── exception/ # Обработка ошибок
│ │ │ └── TravelExpensesApplication.java
│ │ └── resources/
│ │ ├── application.yml
│ │ ├── application-dev.yml
│ │ ├── db/migration/ # Flyway-скрипты
│ │ └── templates/ # Thymeleaf
│ └── test/
│ └── java/com/example/travelexpenses/
├── docs/ # Документация
├── .env.example
├── .gitignore
├── pom.xml
└── README.md

## Инструкции по развёртыванию

1. Клонировать репозиторий:
   ```bash
   git clone https://github.com/elizaveta18072008-dev/corporate-travel-expenses.git
   cd corporate-travel-expenses
