# Frontend сборка лендинга Promo Italia с использованием Webpack

🔗 Готовый результат: [сайт Promo Italia](https://stormozov.github.io/promo-italia/)

## 🎯 Цель проекта

Создание временного лендинга для салона красоты, который будет служить эффективным инструментом для привлечения новых клиентов, информирования о предоставляемых услугах и существовании салона, а также сбора контактной информации для дальнейшего взаимодействия.

## 🎯 Задачи проекта

1. **Анализ целевой аудитории:** Определение потребностей и предпочтений потенциальных клиентов салона красоты.
2. **Разработка дизайна:** Создание привлекательного и интуитивно понятного дизайна, который будет соответствовать имиджу салона и привлекать внимание целевой аудитории.
3. **Верстка лендинга:** Реализация дизайна в виде адаптивного веб-интерфейса, который будет корректно отображаться на различных устройствах (ПК, планшеты, смартфоны).
4. **Интеграция сторонних скриптов:** Сторонний модуль онлайн-записи, Яндекс отзывы, Яндекс карта.
5. **Базовая SEO-оптимизация:** Базовая оптимизация контента и структуры лендинга для повышения видимости в поисковых системах.
6. **Тестирование и запуск:** Проведение тестирования функциональности и пользовательского опыта перед запуском лендинга.

## 📦 Начало работы

### Предварительные требования

- Node.js v14+
- npm v6+ или yarn v1.22+

### Установка

1. Клонирование репозитория:

```bash
git clone https://github.com/stormozov/promo-italia.git
cd promo-italia
```

2. Установка зависимостей:

```bash
npm install # или yarn install
```

## 🚀 Доступные команды

### Запуск сборки в режиме разработки с локальным сервером

```bash
npm run dev # или yarn dev
```

Эта команда запускает `Webpack Dev Server` с указанной конфигурацией для разработки. `Webpack Dev Server` предоставляет локальный сервер для разработки с поддержкой горячей перезагрузки (hot reloading), что позволяет обновлять страницу без полной перезагрузки при изменении кода.

### Запуск сборки в режиме продакшн

```bash
npm run production # или yarn production
```

Эта команда запускает Webpack с конфигурацией для продакшена в режиме production. В этом режиме Webpack оптимизирует код, минимизирует его и выполняет другие оптимизации для улучшения производительности.

Собирает оптимизированную версию проекта в директорию `dist/`

### Запуск build сборки для отладки

```bash
npm run build # или yarn build
```

### Запуск сборки с отслеживанием изменений

```bash
npm run watch # или yarn watch
```

Эта команда запускает Webpack сборку с конфигурацией для разработки, но с флагом `--watch`. Webpack будет следить за изменениями в файлах и автоматически пересобирать проект при каждом изменении, что удобно для разработки.

### Запуск подготовки окружения и начала разработки

```bash
npm run bundle # или yarn bundle
```

Эта команда сначала выполняет `npm install`, чтобы установить все зависимости, а затем запускает команду `watch`. Это полезно для подготовки окружения и начала разработки.

### Запуск тестов `link:sass`

```bash
npm run lint:sass # или yarn lint:sass
```

Эта команда запускает `sass-lint`, инструмент для проверки кода на наличие ошибок и несоответствий в стилях Sass.

### Запуск тестов `link:js`

```bash
npm run lint:js # или yarn lint:js
```

Эта команда запускает `eslint`, инструмент для статического анализа кода JavaScript, чтобы найти и исправить проблемы в коде. Она проверяет все файлы с расширением `.js` в папке `src/js/`.

### Запуск тестов `stats`

```bash
npm run stats # или yarn stats
```

Эта команда сначала запускает Webpack с конфигурацией для продакшена и генерирует JSON-отчет о сборке, который сохраняется в `dist/stats.json`. Затем она запускает `webpack-bundle-analyzer`, чтобы визуализировать размер и структуру бандлов, что помогает в оптимизации.

## ⚙️ Конфигурация Webpack

### Основные особенности конфигурации:

- Обработка `SCSS` → `CSS` с автопрефиксером
- Оптимизация изображений
- `Babel`
- Разделение вендорных скриптов

### Основные настройки
- Выходная директория: `dist/`
- `DevServer` настроен на порт `8080` с горячей перезагрузкой

## ⚠️ Примечания
- Все изменения в исходных файлах должны делаться в директории `src/`
- Готовая сборка создается в `dist/` *(не коммитить эту директорию)*
- Для кастомных настроек webpack редактируем файл `webpack.config.js`