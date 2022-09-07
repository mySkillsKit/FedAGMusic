# FedAGMusic

##Вариант 1 запуск с помощью Dockerfile (App)
Запускаем терминал в папке с приложением:
- Собираем jar архив с нашим spring webflux приложением: ```mvn clean -Dskiptest package```
- Создать образ из нашего Dockerfile, мы должны запустить: ```docker build --tag=fedagmusic:latest .```
- Запускаем Docker контейнер из нашего образа на порту 8080: ```docker run --rm -p8080:8080 -it fedagmusic```
- Проверяем c помощью postman: ```http://localhost:8080```
- Выход из приложения и автоматическое удаление Docker контейнера: в терминале нажать "Ctrl+C"

## Вариант 2 запуск с помощью файла docker-compose.yml (Dockerfile) (App + Postgres)
- Собираем jar архив с нашим spring webflux приложением: ```mvn clean -Dskiptest package```
- Запускаем терминал и выполнить команду: ```docker-compose up```
- Проверяем c помощью postman: ```http://localhost:8080```
- Выход из приложения: в терминале нажать "Ctrl+C" 
- Удаление Docker контейнера: ```docker-compose down```

