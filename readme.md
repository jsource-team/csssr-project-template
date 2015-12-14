# CSSSR Project Template
**Шаблон проекта для быстрого старта.**

## Старт проекта

* Склонируй репозиторий и перейди в папку проекта:

```
git clone git@github.com:CSSSR/csssr-project-template.git new-project && cd new-project
```

* Установи модули:

```
npm i
```

* Запусти шаблон

```
npm start
```

* Открой в браузере [`http://localhost:3000/`](http://localhost:3000/).

## Команды для запуска

* Запуск с отслеживанием изменений:

```
npm start
```

* Сборка в папку `dist`:

```
npm run build
```

* Локальный сервер на другом порте:

```
npm start -- --port=9000
```

* Уведомления об ошибках eslint
```
npm start -- --notify
```

* Воспроизводить звук при ошибках:

```
npm start -- --beep
```

* Расшарить локальный сервер:

```
npm start -- --tunnel
```

* Открыть ссылку в браузере по умолчанию:

```
npm start -- --open
```

* Собрать спрайты и CSS переменные из папок в `app/sprites`:

```
npm run sprite
```

* Собрать архив из папки `dist`:

```
npm run zip
```

* Очистка папки `dist`:

```
npm run clean
```

* Деплой всего содержимого папки `dist` в ветку `dist`:

```
npm run deploy
```

## Структура папок и файлов

```
├── app/                       # Исходники
│   ├── blocks/                # Блоки
│   │   └── block/             # Блок
│   │       ├── block.jade     # Разметка блока
│   │       ├── block.js       # Скрипт блока
│   │       └── block.styl     # Стили блока
│   ├── data/                  # Данные в формате JSON
│   ├── pages/                 # Страницы
│   │   └── index.jade         # Разметка страницы
│   ├── icons/                 # SVG иконки для генерации векторного спрайта
│   ├── sprites/               # PNG иконки для генерации растрового спрайта
│   ├── resources/             # Статические файлы для копирования в dist
│   ├── scripts/               # Скрипты
│   │   └── app.js             # Главный скрипт
│   └── styles/                # Стили
│       ├── helpers/           # Помощники
│       │   ├── fonts.styl     # Подключение шрифтов
│       │   ├── mixins.styl    # Примеси
│       │   ├── optimize.styl  # Сброс стилей и фиксы
│       │   ├── svg-size.styl  # Переменные с размерами SVG иконок (автосборка)
│       │   └── variables.styl # Переменные
│       ├── sprites/           # Переменные с данными PNG спрайтов (автосборка)
│       └── app.styl           # Главный стилевой файл
├── dist/                      # Сборка (автогенерация)
│   ├── assets/                # Подключаемые ресурсы
│   │   ├── fonts/             # Шрифты
│   │   ├── images/            # Изображения
│   │   │   └── sprites/       # Спрайты (автогенерация)
│   │   ├── scripts/           # Скрипты
│   │   └── styles/            # Стили
│   └── index.html             # Страница
├── gulp/                      # Подключаемые скрипты с задачами для gulpfile.babel.js
│   ├── copy.js                # Копирование
│   ├── default.js             # Итоговые списки задач по умолчанию
│   ├── deploy.js              # Деплой в ветку dist
│   ├── icons.js               # Сборка SVG иконок в один файл
│   ├── scripts.js             # Сборка ES2015 скриптов в Webpack
│   ├── semver.js              # Обновление версии шаблона
│   ├── server.js              # Запуск локального сервера
│   ├── sprite.js              # Сборка спрайтов и CSS переменных
│   ├── styles.js              # Сборка стилей
│   ├── templates.js           # Сборка страниц из Jade шаблонов
│   ├── watch.js               # Отслеживание изменений и запуск задач
│   └── zip.js                 # Архивация папки dist
├── .csscomb.json              # Конфигурация форматирования CSS
├── .eslintrc                  # Конфигурация проверки JavaScript в ESLint
├── .editorconfig              # Конфигурация настроек редактора кода
├── .gitignore                 # Список исключённых файлов из Git
├── browserlist                # Список версий браузеров для Autoprefixer
├── gulpfile.babel.js          # Файл для запуска Gulp.js
├── package.json               # Список модулей и прочей информации
└── readme.md                  # Документация шаблона
```
