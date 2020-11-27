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
   ngrok http http://localhost:9000 -host-header="localhost:9000"  
   ```
1. Скопировать/записать/запомнить адрес, который будет выведен после запуска в формате https://XXXXXXXXXX.ngrok.io 
  
Если нужно сменить порт для бэка, то:  
Перейти в ./rosseti-back
В файле variables.env в строке с параметром PUBLICHTTP_LISTEN изменить порт 9000 на произвольный

## Запуск фронта
1. Перейти в ./rosseti-innovation-front
1. Настроить адрес бэка в ./src/app/globals/config.ts
1. Запустить npm i
1. Выполнит sudo npm install -g @angular/cli
1. Выполнить ng serve
1. Запустить ngrok 
   ```bash
   ngrok http http://localhost:9000 -host-header="localhost:4200"  
   ```
1. Обратиться к сервису по адресу, который будет выведен после запуска в формате https://XXXXXXXXXX.ngrok.io

## Тестовые креды
login/pass: +79169999999/123456789

