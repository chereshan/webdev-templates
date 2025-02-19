Middleware для аутентифицированного использования json-БД на стороне приложения. Упрощает разработку, т.к. снимает необходимость написания/хостинга для БД и API. 

# Настройка для Angular
1. Добавляем в папку проекта папку `projects/PROJECTNAME/app` файлы `data.js` и `authMiddleware.js`
2. Прописываем в package.json:
```
"scripts": {
    ...
    "json": "json-server projects/PROJECTNAME/data.js --port 3500 --middleware projects/PROJECTNAME/authMiddleware.js"
  },
```
