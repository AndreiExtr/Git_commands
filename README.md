# 1. Настройка проекта Vue

Установите пакет gh-pages для деплоя:
```
npm install gh-pages --save-dev

```

# 2. Обновление package.json
```
"scripts": {
  "deploy": "gh-pages -d dist"
},
```

# 3. Настройка деплоя
В корне вашего проекта создайте (или обновите) файл vue.config.js:
```
module.exports = {
  publicPath: process.env.NODE_ENV === 'production'
    ? '/your-repo-name/'
    : '/'
}
```
# 4. Компиляция и деплой
- Скомпилируйте ваше приложение:
```
  npm run build
```
- Задеплойте приложение на GitHub Pages:
```
npm run deploy
```


