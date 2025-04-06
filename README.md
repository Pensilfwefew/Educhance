# Парсер данных вузов с tabiturient.ru

## Исполнители
- **Трофимов Д.С.** - основной разработчик парсера
- **Андреева Я.А.** - второй разработчик проекта

## Описание проекта
Парсер собирает данные о вузах России с сайта tabiturient.ru, включая:
- Проходные баллы
- Направления подготовки
- Учебные программы
- Формы обучения

## Результаты парсинга
| Данные            | Количество |
|-------------------|------------|
| Баллы            | 84,627     |
| Направления      | 17,413     |
| Экзамены         | 69,963     |
| Институты        | 805        |
| Города           | 80         |

## Структура базы данных

-- Города
CREATE TABLE gorod (
    id_gorod SERIAL PRIMARY KEY,
    href TEXT,
    city TEXT
);

-- Институты
CREATE TABLE institutes (
    id_institutes SERIAL PRIMARY KEY,
    id_gorod INT REFERENCES gorod(id_gorod),
    full_name TEXT,
    name_small TEXT,
    href TEXT
);

-- Направления подготовки
CREATE TABLE directions (
    id_directions SERIAL PRIMARY KEY,
    id_institutes INT REFERENCES institutes(id_institutes),
    fac TEXT,
    direction TEXT,
    level_program TEXT,
    code_program TEXT,
    profile_program TEXT,
    form_study TEXT
);

-- Баллы
CREATE TABLE ball (
    id_ball SERIAL PRIMARY KEY,
    ball TEXT,
    year TEXT,
    id_directions INT REFERENCES directions(id_directions)
);

-- Экзамены
CREATE TABLE exam (
    id_exam SERIAL PRIMARY KEY,
    id_directions INT REFERENCES directions(id_directions),
    exam TEXT,
    view TEXT
);

## Используемые технологии
```python
# Основные библиотеки
from selenium import webdriver  # Автоматизация браузера
from bs4 import BeautifulSoup  # Парсинг HTML
import psycopg2  # Работа с PostgreSQL
import re  # Регулярные выражения
