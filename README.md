# rosseti-innovation

Leaders Of Digital

## Запуск бэка
1. Перейти в ./rosseti-innovation-back
1. Установить docker-compose, docker
1. Запустить бэк командой 
   ```bash
   docker-compose -f "docker-compose.yml" up -d --build
   ```
1. Установить ngrok
1. Запустить ngrok 
   ```bash
   ngrok http http://localhost:9000  
   ```
1. Скопировать/записать/запомнить адрес, который будет выведен после запуска в формате https://XXXXXXXXXX.ngrok.io 
1. swagger http://localhost:9000/api/v1/swagger/index.html (не все методы есть в свагере)
  
Если нужно сменить порт для бэка, то:  
Перейти в ./rosseti-back
В файле variables.env в строке с параметром PUBLICHTTP_LISTEN изменить порт 9000 на произвольный

### Защита API
Практически весь API защищён, нужно передавать в запросах заголовок Authorization в следующем формате
"session PzcOiGMou6Mk1YjkskGjntcIcr7vIJ8Qu1hJTYak78nFwvmit5PZ9QQGkU4zy0K1zNvGvKSoaiWjR5xAYDyzB10L0KS7edXk1nJa"  
Для curl: -H \"Authorization: session PzcOiGMou6Mk1YjkskGjntcIcr7vIJ8Qu1hJTYak78nFwvmit5PZ9QQGkU4zy0K1zNvGvKSoaiWjR5xAYDyzB10L0KS7edXk1nJa\"

## Запуск фронта
1. Перейти в ./rosseti-innovation-front
1. Настроить адрес бэка в ./src/app/globals/config.ts
1. Запустить npm i
1. Выполнит sudo npm install -g @angular/cli
1. Выполнить ng build --prod
1. Выполнить cd  dist/rosseti-inn
1. Установить web-сервер sudo npm install --global http-server
1. Выполнить http-server -p 4200
1. Запустить ngrok 
   ```bash
   ngrok http http://localhost:4200 -host-header="localhost:4200"  
   ```
1. Обратиться к сервису по адресу, который будет выведен после запуска в формате https://XXXXXXXXXX.ngrok.io

## Тестовые креды
login/pass: +79169999999/123456789

