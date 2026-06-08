# Настройка

## Инициализация проекта

В терминале выполните:

```bash
npm init
```

## Установка библиотеки SASS

Установка последней версии:

```bash
npm install sass --save-dev
```

или сокращённо:

```bash
npm i sass -D
```

Установка конкретной версии:

```bash
npm install sass@1.80.6 --save-dev
```

или сокращённо:

```bash
npm i sass@1.80.6 -D
```

## Настройка запуска SASS

В файле `package.json` найдите раздел:

```json
"scripts": {
  "test": "echo \"Error: no test specified\" && exit 1"
}
```

и добавьте команду `sass-watch`:

```json
"scripts": {
  "test": "echo \"Error: no test specified\" && exit 1",
  "sass-watch": "sass --watch ."
}
```

Запустите отслеживание изменений:

```bash
npm run sass-watch
```

## Шрифты

### Папка `fonts`

1. Скачайте шрифты с Google Fonts.
2. Преобразуйте их в формат `woff2` с помощью Transfonter.
3. Поместите файлы шрифтов в папку `fonts`.

### Файл `styles/_fonts.scss`

Подключите шрифт через `@font-face`:

```scss
@font-face {
  font-family: 'Kumbh Sans';
  src: url('../fonts/KumbhSans-Regular.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}
```