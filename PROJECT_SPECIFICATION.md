# Спецификация проекта: Система для изучения английского языка

## Обзор проекта
Данное приложение представляет собой интерактивную платформу для изучения английского языка, ориентированную на русскоговорящих пользователей. Система построена на современном технологическом стеке и использует интеллектуальные алгоритмы для персонализации обучения.

## Целевая аудитория
- Русскоговорящие пользователи, желающие изучать английский язык
- Начинающие и продвинутые ученики (уровни от A1 до C2 по шкале CEFR)
- Индивидуальные пользователи, занимающиеся самостоятельно

## Ключевые ценности продукта
- **Эффективное обучение**: Система интервального повторения обеспечивает долгосрочное запоминание
- **Персонализация**: Контент адаптируется под уровень и прогресс ученика
- **Простота использования**: Минималистичный интерфейс с фокусом на практику
- **Практический подход**: Обучение через активный перевод предложений
- **Подробная обратная связь**: Анализ переводов с рекомендациями на русском языке

## Технологическая база
- **Бэкенд**: NestJS с PostgreSQL
- **Интеграция ИИ**: OpenAI API для анализа переводов и генерации контента
- **Инфраструктура**: Docker, CI/CD через GitHub Actions

## Функциональность MVP

### Основной процесс обучения
1. Пользователь получает предложение на английском для перевода на русский
2. Система анализирует перевод на нескольких уровнях:
   - Правильность использования ключевого слова
   - Корректное применение грамматической темы
   - Общая точность и естественность перевода
3. Пользователь получает подробную обратную связь на русском языке
4. Система планирует повторение материала на основе результатов

### Учет прогресса пользователя
- Отслеживание освоения словарного запаса
- Мониторинг прогресса по грамматическим темам
- Адаптивный выбор сложности материала
- Серия дней обучения (streak) и ежедневные цели

### Административные функции
- Управление пользователями (создание, редактирование, удаление)
- Модерация и добавление учебного контента
- Роли пользователей: USER, MODERATOR, ADMIN
- Мониторинг использования системы

## Модели данных

### Основные сущности
- **Пользователи**: Профили учащихся с учетными данными и настройками
- **Слова**: Словарный запас с переводами и примерами
- **Грамматические темы**: Структурированные правила с объяснениями
- **Предложения**: Практические примеры с ключевыми словами и грамматикой

### Прогресс обучения
- **Прогресс по словам**: Отслеживание изученных слов с применением интервального повторения
- **Прогресс по грамматике**: Мониторинг освоения грамматических тем
- **Прогресс по предложениям**: История переводов с оценкой правильности
- **Сессии обучения**: Отслеживание активности пользователя

## Пользовательский путь

### Регистрация и настройка
1. Регистрация с email и паролем
2. Определение начального уровня владения языком (CEFR)
3. Установка ежедневных целей обучения

### Ежедневное использование
1. Получение адаптированных упражнений на перевод
2. Отправка переводов и получение обратной связи
3. Отслеживание дневного прогресса и серии дней
4. Доступ к личной статистике и аналитике

## API и интеграции

### Основные API-эндпоинты
- Аутентификация и управление пользователями
- Получение и проверка упражнений
- Доступ к статистике и прогрессу
- Управление учебным контентом

### Внешние интеграции
- OpenAI API для генерации контента и проверки переводов
- Email-сервис для восстановления пароля

## Безопасность и соответствие требованиям
- Защищенная аутентификация через JWT
- Хеширование паролей
- Защита от основных уязвимостей веб-приложений
- Разграничение доступа на основе ролей

## Расширения для будущих версий

### Расширение учебного опыта
- Различные форматы упражнений (множественный выбор, заполнение пропусков)
- Тематические категории для контекстного обучения
- Персонализированные учебные пути на основе интересов

### Геймификация и мотивация
- Система достижений и наград
- Виртуальная валюта и поощрения
- Еженедельные вызовы и цели для поддержания вовлеченности

### Социальные элементы
- Лидерборды по различным категориям
- Добавление друзей и отслеживание их прогресса
- Групповые вызовы и соревнования

### Аналитика для пользователей
- Визуализация прогресса по темам и уровням
- Идентификация слабых мест и рекомендации
- Прогнозирование готовности к повышению уровня CEFR

## Метрики успеха
- Удержание пользователей (DAU, WAU, MAU)
- Средняя продолжительность сессии
- Непрерывность обучения (длина серий)
- Прогресс пользователей по уровням CEFR
- Количество выполненных упражнений

## График реализации
1. **Фаза 1 (MVP)**: Базовая функциональность перевода предложений
2. **Фаза 2**: Расширенная аналитика и геймификация
3. **Фаза 3**: Социальные функции и дополнительные форматы упражнений
4. **Фаза 4**: Мобильные приложения и расширенные интеграции

## Команда проекта
- Руководитель проекта
- Бэкенд-разработчики (NestJS)
- Фронтенд-разработчики
- Специалист по UX/UI
- Лингвист (методолог)
- QA-инженеры

## Риски и их снижение
- **Стоимость OpenAI API**: Оптимизация запросов, кэширование, лимиты
- **Качество обратной связи**: Тщательное тестирование промптов, регулярные улучшения
- **Удержание пользователей**: Геймификация, уведомления, качественный контент
- **Масштабирование**: Модульная архитектура, горизонтальное масштабирование

## Заключение
Данный проект представляет инновационный подход к изучению английского языка через активную практику и интеллектуальный анализ. Система предлагает эффективный способ обучения с использованием современных технологий и методик, обеспечивая персонализированный опыт для каждого пользователя. 