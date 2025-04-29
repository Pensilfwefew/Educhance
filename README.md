# Лабораторная работа 1. Web как источник данных
**Тема**: Парсер данных вузов с tabiturient.ru  

## Команда разработчиков
| Роль | ФИО | Вклад |
|------|-----|-------|
| Основной разработчик | Трофимов Д.С. | Реализация парсера, работа с БД |
| Второй разработчик | Андреева Я.А. | Поддержка кода, тестирование |

## Описание проекта
Система собирает актуальные данные о российских вузах с сайта [tabiturient.ru](https://tabiturient.ru) для анализа образовательных программ.

### Основной функционал
- Парсинг данных по городам и вузам
- Сбор информации о:
  - Проходных баллах
  - Направлениях подготовки
  - Учебных программах
  - Формах обучения
- Сохранение в PostgreSQL

## Техническая реализация
### Используемый стек
```python
# Основные технологии
from selenium import webdriver  # Автоматизация браузера
from bs4 import BeautifulSoup  # Парсинг HTML
import psycopg2  # Работа с PostgreSQL
import re  # Регулярные выражения
## Результаты парсинга
| Данные            | Количество |
|-------------------|------------|
| Баллы            | 84,627     |
| Направления      | 17,413     |
| Экзамены         | 69,963     |
| Институты        | 805        |
| Города           | 80         |
# Лабораторная работа 2. Сбор данных и проектирование приложения  
**Групповой трек**  
**Тема**: REST API для системы управления данными университетов  
## Команда разработчиков  
| Роль | ФИО | Вклад |  
|------|-----|-------|  
| Основной разработчик | Трофимов Д.С. | Реализация контроллеров, DTO моделей, валидации |  
| Второй разработчик | Андреева Я.А. | Поддержка кода, тестирование |

## Описание проекта  
API для работы с данными, собранными в ЛР1 (парсер tabiturient.ru), предоставляющее:  
- Полный CRUD-функционал  
- Документирование через OpenAPI

## Основной функционал  
### Сущности и методы  
**Города (Cities)**  
- `GET /api/university/cities` - Полный список городов   
- `GET /api/university/cities/{id}` - Получение города по ID 
- `POST /api/university/cities` - Создание города 
- `PUT /api/university/cities/{id}` - Полное обновление 
- `DELETE /api/university/cities/{id}` - Удаление города

**Институты (Institutes)**  
- `GET /api/university/institutes` - Список всех вузов  
- `GET /api/university/institutes/{id}` - Получение вуза по ID  
- `POST /api/university/institutes` - Добавление нового вуза  
- `PUT /api/university/institutes/{id}` - Обновление данных вуза  
- `DELETE /api/university/institutes/{id}` - Удаление вуза  

**Направления подготовки (Directions)**  
- `GET /api/university/directions` - Все направления  
- `GET /api/university/directions/{id}` - Направление по ID  
- `POST /api/university/directions` - Добавление направления  
- `PUT /api/university/directions/{id}` - Обновление направления  
- `DELETE /api/university/directions/{id}` - Удаление направления  

**Экзамены (Exams)**  
- `GET /api/university/directions/{id}/exams` - Экзамены по направлению  
- `POST /api/university/directions/{id}/exams` - Добавление экзамена  

**Проходные баллы (Scores)**  
- `GET /api/university/scores/{year}` - Баллы за конкретный год  
- `POST /api/university/directions/{id}/scores` - Добавление новых баллов

## Техническая реализация  
### Основные технологии  
```csharp
// Ядро API
Microsoft.AspNetCore.Mvc
Microsoft.EntityFrameworkCore
