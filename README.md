[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![GitHub contributors](https://img.shields.io/github/contributors/Ornstein89/VserossHachathon_2022_Foxhound)

# FoxInt

Решение команды Foxhound на Всероссийском хакатоне (https://hackathon-rf.ru/), 9-12 декабря 2022 г. 

Кейс 1, задача "Определение местоположения БВС в условиях отсутствия GPS\ГЛОНАСС сигнала" (https://drive.google.com/file/d/1hKSvoX6HPj983NkXkuqmTxuvnFJjkpKd/view). 

Демоверсия развёрнута на https://foxhound-team.pro и доступна до 19 декабря 2022 г.

Документация к API доступна на https://foxhound-team.pro/docs

# Структура репозитория

`backend` - бекенд демоверсии на FastAPI.

`compose` - файлы автоматического развёртывания демоверсии в контейнерной инфраструктуре.

`frontend` - веб-страница демоверсии на Vuetify.

`research` - скрипты предварительной обработки данных, прототипирование алгоритмов на Python/Jupyter.

# Развертывание через docker-compose
1. Установить [docker](https://docs.docker.com/engine/install/ubuntu/)
2. В папке compose создать файл .env и [заполнить](#описание-переменных-окружения) его в соответствии с примерами
3. Запустить команду docker compose up -d с правами суперпользователя
```bash
sudo docker compose up -d
```
5. Настроить внешний nginx, который будет пересылать все запросы на порт приложения

## Описание переменных окружения

### HTTP_PORT
Файлы: .env

Тип: целое число

Назначение: порт на котором будет крутиться приложение


## Команды docker-compose 
Все команды необходимо выполнять в папке compose
- Остановить все контейнеры
```bash
sudo docker-compose stop
```
- Перезапустить контейнер
```bash
sudo docker-compose restart {container_name}
```
