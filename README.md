# yamdb_final

[![Django-app workflow](https://github.com/AnnaMolodova/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)](https://github.com/AnnaMolodova/yamdb_final/actions/workflows/yamdb_workflow.yml)

### _CI и CD проекта api_yamdb_
Настроено для приложения Continuous Integration и Continuous Deployment
Реализован:
- автоматический запуск тестов
- обновление образов на Docker Hub
- автоматический деплой на боевой сервер при пуше в главную ветку main

В workflow реализовано четыре задачи:
- проверка кода на соответствие стандарту PEP8
- сборка и доставка докер-образа для контейнера web на Docker Hub
- автоматический деплой проекта на боевой сервер
- отправка уведомления в Telegram о том, что процесс деплоя успешно завершился

### Подготовка сервера:
- Остановите службу nginx
```sh
sudo systemctl stop nginx
```
- Установите docker и docker-compose
```sh
sudo apt install docker.io
```
- Скопируйте файлы docker-compose.yaml и nginx/default.conf из вашего проекта на сервер в home/<ваш_username>/docker-compose.yaml и home/<ваш_username>/nginx/default.conf соответственно
- Добавьте в Secrets GitHub Actions переменные окружения для работы базы данных
