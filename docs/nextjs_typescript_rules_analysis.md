# Анализ правил TypeScript/Next.js для Cursor

Этот документ содержит анализ и описание всех аспектов разработки с использованием TypeScript и Next.js, представленных в Cursor rules.

## 1. Общее руководство по разработке (nextjs-development-guide)

- **Ключевые принципы**:
  - Использование современного JavaScript и TypeScript
  - Предпочтение App Router вместо Pages Router
  - Компонентный дизайн на основе атомарной методологии
  - Разделение API-уровня и UI
  - Оптимизация производительности как приоритет
  - Подход к разработке через тестирование
  - Следование единым правилам форматирования кода
  - Использование типизированных констант и перечислений вместо строковых литералов
  - Чистая структура папок (без специальных символов)
  - Использование pnpm в качестве единственного пакетного менеджера

- **Технологический стек**:
  - Next.js 14+ с App Router
  - TypeScript для типобезопасности
  - Tailwind CSS v4 для стилизации
  - shadcn/ui для кастомизируемых UI-компонентов
  - Zustand для управления состоянием
  - TanStack Query для получения и кеширования данных
  - next-intl для интернационализации
  - Jest и React Testing Library для тестирования
  - ESLint и Prettier для качества кода и форматирования

## 2. Структура проекта (nextjs-project-structure)

- **Директории и файлы**:
  ```
  my-next-app/
  ├── .eslintrc.js           # ESLint конфигурация
  ├── .gitignore             # Git ignore файл
  ├── .prettierrc            # Prettier конфигурация
  ├── next.config.js         # Next.js конфигурация
  ├── package.json           # Зависимости и скрипты
  ├── tsconfig.json          # TypeScript конфигурация
  ├── public/                # Статические файлы
  ├── src/                   # Исходный код
  │   ├── app/               # App Router структура
  │   ├── components/        # UI компоненты
  │   │   ├── ui/            # shadcn/ui компоненты
  │   │   ├── atoms/         # Атомарные компоненты
  │   │   ├── molecules/     # Молекулярные компоненты
  │   │   ├── organisms/     # Организмы
  │   │   └── templates/     # Шаблоны страниц
  │   ├── hooks/             # React hooks
  │   ├── lib/               # Утилиты и общий код
  │   ├── services/          # API сервисы
  │   ├── store/             # Zustand состояние
  │   ├── styles/            # Стили
  │   └── tests/             # Тесты
  ```

- **Организация маршрутизации App Router**:
  - File-system based подход
  - Запрет на использование специальных символов в именах папок (кроме @ для параллельных маршрутов)
  - Логическая иерархия маршрутов

- **Соглашения об именовании**:
  - Маршруты: kebab-case
  - Компоненты: PascalCase
  - Утилиты: camelCase
  - Константы: UPPER_SNAKE_CASE
  - Специальные файлы Next.js: стандартные имена (layout.tsx, loading.tsx, и т.д.)

- **Организация компонентов**:
  - Атомарный дизайн (atoms, molecules, organisms, templates)
  - Интеграция с shadcn/ui

## 3. Уровень API и сервисы (nextjs-api-service-layer)

- **Структура сервисного слоя**:
  ```
  services/
  ├── api-client.ts          # Базовый API клиент
  ├── endpoints.ts           # Константы API эндпоинтов
  ├── types.ts               # Общие API типы
  ├── auth-service.ts        # Сервис аутентификации
  ├── user-service.ts        # Сервис пользователей
  └── mock/                  # Моковые данные
  ```

- **API клиент**:
  - Типизированный с использованием TypeScript
  - Обработка ошибок
  - Поддержка аутентификации

- **Эндпоинты**:
  - Типобезопасные константы и перечисления
  - Функции для создания динамических эндпоинтов

- **Моковые данные**:
  - Структурированные JSON файлы для разработки
  - Имитация API поведения

## 4. TypeScript (nextjs-typescript)

- **Конфигурация TypeScript**:
  - Строгая типизация (strict: true)
  - Алиасы путей для удобства импорта

- **Определения типов**:
  - Центральное место для общих типов
  - Типизированные props компонентов
  - Типы для функций

- **Типобезопасность с App Router**:
  - Типизация параметров и props страниц
  - Типизация обработчиков маршрутов

- **Управление состоянием с TypeScript**:
  - Типизация Zustand хранилищ
  - Типизация хуков

## 5. Тестирование (nextjs-testing)

- **Настройка тестирования**:
  - Jest и React Testing Library
  - Конфигурация для Next.js

- **Организация тестов**:
  - Совместное размещение (co-located) тестов с компонентами
  - Или отдельная директория для тестов

- **Категории тестов**:
  - Юнит-тесты
  - Интеграционные тесты
  - Тесты страниц
  - Тесты API маршрутов

## 6. Storybook (nextjs-storybook)

- **Настройка Storybook**:
  - Интеграция с Tailwind CSS
  - Поддержка TypeScript
  - Предотвращение сбоев при синтаксических ошибках

- **Организация историй**:
  - Структура файлов
  - Формат историй (CSF)
  - Использование аргументов и параметров

- **Интеграция с Tailwind CSS v4**
  - Обновленная конфигурация для поддержки последней версии

## 7. Интернационализация (nextjs-internationalization)

- **Настройка next-intl**:
  - Файлы переводов
  - Конфигурация middleware
  - Настройка App Router

- **Использование переводов**:
  - В серверных компонентах
  - В клиентских компонентах
  - Параметризированные переводы

## 8. Линтинг и форматирование (nextjs-linting)

- **ESLint конфигурация**:
  - Расширенный набор правил для Next.js и TypeScript
  - Правила импорта
  - Кастомные правила для проекта

- **Prettier конфигурация**:
  - Единый стиль кода
  - Интеграция с ESLint

- **Интеграция с VS Code**:
  - Настройки редактора
  - Рекомендуемые расширения

- **Git интеграция**:
  - Husky для пре-коммит хуков
  - lint-staged для проверки только измененных файлов

## 9. Процесс разработки фичей (nextjs-feature-development)

- **Рабочий процесс**:
  - Анализ требований
  - Инкрементальная разработка
  - Пост-имплементационный чеклист

- **Чеклист**:
  - Юнит-тестирование
  - Storybook документирование
  - Интернационализация
  - Моковые сервисы
  - Линтинг и форматирование
  - Тестирование
  - Проверка соответствия требованиям
  - Обновление документации

## 10. Управление пакетами (nextjs-package-management)

- **pnpm как эксклюзивный пакетный менеджер**:
  - Настройка проекта
  - Ежедневное использование
  - CI/CD конфигурация
  - Миграция с npm или yarn

- **Конфигурация**:
  - .npmrc файл
  - package.json настройки
  - Глобальная конфигурация

## 11. Tailwind CSS v4 (nextjs-tailwind-v4)

- **Настройка Tailwind CSS v4**:
  - Установка
  - Конфигурация PostCSS
  - Конфигурация Tailwind CSS

- **Использование**:
  - Базовое использование
  - Кастомные утилиты с @utility
  - Респонсив дизайн
  - Темная тема

- **Интеграция с Next.js App Router**:
  - Импорт CSS в корневом layout
  - Конфигурация темы

## 12. Миграция на Tailwind CSS v4 (nextjs-tailwind-v4-migration)

- **Автоматическая миграция**:
  - Использование официального инструмента обновления
  - Совместимость с другими инструментами

- **Ручная миграция**:
  - Обновление зависимостей
  - Обновление PostCSS конфигурации
  - Обновление Tailwind конфигурации
  - Обновление CSS файлов
  - Обновление кастомных утилит
  - Обновление названий классов
  - Обновление плагинов

## 13. shadcn/ui (nextjs-shadcn-ui)

- **Введение в shadcn/ui**:
  - Отличие от традиционных библиотек компонентов
  - Ключевые преимущества

- **Настройка**:
  - В новых проектах
  - В существующих проектах
  - Интеграция в существующую структуру проекта

- **Структура проекта с shadcn/ui**:
  - Организация компонентов
  - Интеграция с атомарным дизайном

- **Стратегии интеграции**:
  - Прямое использование
  - Паттерн расширения
  - Композиция
  - Кастомизация темы 