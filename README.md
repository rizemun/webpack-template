# Webpack-template
Базовая сборка для разработки одностраничных приложений.
### Установка
Склонировать репозиторий:  
```bash
$ git clone https://github.com/rizemun/webpack-template.git
```
Установить зависимости:
```bash
$ npm i
```
### Использование
Сборка в режиме разработчика:
```bash
$ npm run dev
```
Сборка в продакшн:
```bash
$ npm run build
```
Автоматическое упорядочивание стилей:
```bash
$ csscomb src
```

### CI  
Для CI используется [travis](https://travis-ci.com/), нужно авторизоваться на сайте через гитхаб, синхронизировать аккаунт и перейти в настройки репозитория (`More options` > `Settings` > `Environment Variables`)  
В поле name нужно ввести `GITHUB_TOKEN` а для value нужно сгенерировать на гитхабе токен персонального доступа.  
На гитхабе заходим в `Settings` > `Developer Settings` > `Personal access tokens`.  
Генерируем новый токен с галочкой только рядом с `public_repo`. Полученное значение токена можно использовать для сборки всех публичных репозиториев, чтобы не генерировать каждый раз новый можно записать куда то этот ключ. Важно! Не оставлять ключ в репозитории или ненадежных местах.  
Полученый ключ записываем в поле `value` в тревисе.  
Теперь, если перейти во вкладку `current` можно увидеть что сборка пошла и через некоторое время результат окажется на github.pages  

Теперь при каждом пуше сборка на тревисе сама запустится и обработает изменения.
