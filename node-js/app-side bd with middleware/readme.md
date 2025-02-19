Middleware для аутентифицированного использования json-БД на стороне приложения. Упрощает разработку, т.к. снимает необходимость написания/хостинга для БД и API. 
* use-case: Если нужно быстро развернусть mock-api для тестирования приложения и RESTFull API.

# Настройка для Angular
1. Добавляем в папку проекта папку `projects/PROJECTNAME/app` файлы `data.js` и `authMiddleware.js`
2. Устанавливаем json-сервер конкретно версии 0.17.4 (т.к. выше не поддерживает middleware): `npm install json-server@0.17.4`
3. Прописываем в package.json:
```
"scripts": {
    ...
    "json": "json-server projects/PROJECTNAME/data.js --port 3500 --middleware projects/PROJECTNAME/authMiddleware.js"
  },
```
4. Запускаем сервер: `npm run json`
